# GitHub Copilot Instructions for Chakra UI v3 Development

## General Rules:
- ALWAYS generate code using Chakra UI version 3 (v3) syntax.
- AVOID any Chakra UI v2 syntax or components.
- Refer to the project's `docs/llms-v3-migration.txt` for detailed v3 changes.

## Key Chakra UI v3 Changes (from docs/llms-v3-migration.txt):

### Component Renames & Prop Changes:
- **Modal -> Dialog**:
    - `Modal` is now `Dialog`.
    - `isOpen` prop is `open` (on `Dialog.Root`).
    - `onClose` prop is `onOpenChange` (on `Dialog.Root`).
    - `isCentered` is handled by `placement="center"` or similar on `Dialog.Content`.
- **colorScheme -> colorPalette**:
    - The `colorScheme` prop is now `colorPalette`. Example: `<Button colorPalette="blue">`.
- **Stack Spacing**:
    - `spacing` prop in `Stack` is now `gap`. Example: `<Stack gap={4}>`.
- **Form Controls (FormControl -> Field)**:
    - `FormControl`, `FormLabel`, `FormErrorMessage` are replaced by `Field.Root`, `Field.Label`, `Field.ErrorText`.
- **Boolean Props**:
    - `isOpen` -> `open`
    - `isDisabled` -> `disabled`
    - `isInvalid` -> `invalid`
    - `isRequired` -> `required`
- **Link `isExternal`**:
    - `<Link isExternal>` becomes `<Link target="_blank" rel="noopener noreferrer">`.
- **Icons**:
    - `@chakra-ui/icons` is removed. Use `lucide-react` or `react-icons`.
- **Theming**:
    - `extendTheme` is replaced by `createSystem(defaultConfig, { theme: { tokens: { ... } } })`.
- **Provider**:
    - `ChakraProvider theme={theme}` becomes `<Provider value={system}>` (often using a custom `Provider` from snippets).
- **Gradients**:
    - `bgGradient="linear(to-r, red.200, pink.500)"` becomes `bgGradient="to-r" gradientFrom="red.200" gradientTo="pink.500"`.

## Code Style:
- Use namespaced imports for Chakra UI components where appropriate (e.g., `Accordion.Root`, `Accordion.Item`).

## Important Files to Reference (for more detail):
- `docs/llms.txt` (overview)
- `docs/llms-v3-migration.txt` (migration details)
- `docs/llms-components.txt` (v3 component specifics)
- `docs/llms-styling.txt` (v3 styling)
- `docs/llms-theming.txt` (v3 theming)

When generating Chakra UI code, prioritize these v3 conventions.
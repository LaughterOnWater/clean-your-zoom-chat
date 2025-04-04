# Conference Chat Cleanup Guide for VS Code

## Quick Reference
Use these regex patterns in VS Code's search and replace to clean up conference chat transcripts.

### Remove "Reacted to" lines
```
Search:  ^.*\s:\sReacted\sto\s.*\r?\n
Replace: [leave empty]
```

### Remove "Direct Message" lines  
```
Search:  ^.*\(direct\smessage\)\s:\s.*\r?\n
Replace: [leave empty]
```

## Step-by-Step Instructions

1. Open your chat transcript file in VS Code
2. Press `Ctrl+F` (Windows/Linux) or `Cmd+F` (Mac) to open the search panel
3. Click the `.*` button to enable regex mode (or press `Alt+R`)
4. Enter the search pattern you need
5. Leave the replace field empty to completely remove the lines
6. Click "Replace All" or use `Ctrl+Alt+Enter`

## How It Works

These patterns match:
- `^.*` - Start of line, followed by any characters
- `\s:\s` - Space, colon, space (for "Reacted to")
- `\(direct\smessage\)` - The literal text "(direct message)"
- `.*` - Any characters to the end of the line
- `\r?\n` - Line break (works for both Windows and Unix line endings)

By leaving the replace field empty, you remove both the content and the line break.

## Additional Tips

- Always test on a small section or backup your file before performing a "Replace All"
- You can modify these patterns for other common chat elements
- For more complex filtering, consider combining multiple regex operations

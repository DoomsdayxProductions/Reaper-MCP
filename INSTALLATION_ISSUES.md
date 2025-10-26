# 🚨 Common Installation Issues

This guide covers common issues you might encounter when installing Reaper MCP and their solutions.

---

## **❌ ERROR: Could not find a version that satisfies the requirement [package]**

**Solution**: Make sure your virtual environment is activated:
- **Windows**: `venv\Scripts\activate`
- **Mac/Linux**: `source venv/bin/activate`

**Alternative**: Try upgrading pip first:
```bash
pip install --upgrade pip
```

---

## **❌ Module not found errors when running server**

**Solution**: Ensure virtual environment is activated before running

**Check paths**: Make sure the Claude CLI command uses the correct venv path

---

## **❌ Chrome/Browser issues**

**Solution**: The server will automatically download Chrome when first run

**No manual Chrome installation needed**

---

## **❌ "Failed to connect to browser" / Root user issues**

**Solution**: ✅ **AUTO-FIXED!** Auto-detects root/administrator and adds `--no-sandbox` automatically

**Manual fix**: Add `"args": ["--no-sandbox", "--disable-setuid-sandbox"]` to spawn_browser calls

**Diagnostic tool**: Use `ReaperMCP_validate_browser_environment_tool()` to check your environment

---

## **❌ "Input validation error" with args parameter**

**Solution**: ✅ **AUTO-FIXED!** Now accepts both JSON arrays and JSON strings:
- `"args": ["--no-sandbox"]` (preferred)
- `"args": "[\"--no-sandbox\"]"` (also works)

---

## **❌ Container/Docker issues**

**Solution**: ✅ **AUTO-FIXED!** Auto-detects containers and adds required arguments

**Manual fix**: Add `"args": ["--no-sandbox", "--disable-dev-shm-usage", "--disable-gpu"]`

---

## **❌ "claude mcp add-json" command not found**

**Solution**: Make sure you have Claude Code CLI installed

**Alternative**: Use manual configuration method in the [main README](README.md#alternative-manual-configuration-if-claude-cli-not-available)

---

## **❌ Path errors in Windows**

**Solution**: Use double backslashes `\\` in JSON strings for Windows paths

**Example**: `"C:\\\\Users\\\\name\\\\project\\\\venv\\\\Scripts\\\\python.exe"`

---

## Need More Help?

- **📖 [Main Documentation](README.md)** - Complete setup guide
- **💬 [Discord Community](https://discord.gg/7ETmqgTY6H)** - Get help from the community
- **🐛 [GitHub Issues](https://github.com/DoomsdayxProductions/Reaper-MCP/issues)** - Report bugs or request features

---

*💀 Back to [README](README.md)*


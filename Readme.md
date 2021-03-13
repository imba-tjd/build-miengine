# Build microsoft/MIEgnine

See https://github.com/microsoft/MIEngine/pull/1025

[Download from Artifacts][1] and replace `C:\Users\<user>\.vscode\extensions\ms-vscode.cpptools-x.x.x\debugAdapters\bin\WindowsDebugLauncher.exe`

This is built automatically monthly.

Make sure you have ANSI code page, or you won't need this.

---

To build the whole project:

```yml
- uses: microsoft/setup-msbuild@v1
- run: |
    cd src;
    msbuild -v:m -r -p:Configuration=Desktop.Release;
```

Though `OpenDebugAD7.exe` doens't work. Maybe also copy dll could fix.

[1]: https://docs.github.com/en/actions/managing-workflow-runs/downloading-workflow-artifacts

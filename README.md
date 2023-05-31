# blogly

## Commands

### - listen subId workspaceDir
Listen for changes to a specific file within the workspace
```
dotnet run -- listen 3 ~/Workspace
```

### - new
Creates new post in local dev db and creates file in workspace, opens the file in VSCode and then begins listening for changes to file.
```
dotnet run -- new
```

### - migrate connectionString1 connectionString2
Adds all non-existing posts from one database to another.
```
dotnet run -- migrate "mongodb://shane:password@127.0.0.1:27017/shaneduffy_database?authSource=shaneduffy_database" "mongodb://shane:password@143.198.140.108:27017/shaneduffy_database?authSource=shaneduffy_database"
```

### - crosspost platform(medium, dev, hashnode) subId workspaceDir
Migrates the post with the given subId to the specified platform.
```
dotnet run -- crosspost medium 13 /home/shane/workspace
```

## Notes
type - blog, notes

postUri - does not contain file extension

### Styles/Elements
`h1`, `h2`, `h3`, `h4`, `p`

Inline Code - `<span class="text-code">...</span>`

Full Code - `<pre><code>...</pre></code>`

Text Link - `<a class="text-link">....</a>`

Italic - `<span class="text-italic">...</span>`

### Code Highlighting
The value in `codelang` attribute will be forwarded to the Markdown translation.
```
<pre><code codelang="cs"></code></pre>
```

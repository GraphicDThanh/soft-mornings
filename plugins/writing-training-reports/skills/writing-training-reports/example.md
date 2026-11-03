# Example

All names and links are made up.

**Saved profile (from setup, not repeated in daily notes):**

```
Training report profile
- Sender: Minh Le
- Team prefix: hf
- Supporters (To): An Tran <an.tran@example.com>, Binh Do <binh.do@example.com>
- CC: training@example.com, Cuong Pham <cuong.pham@example.com>
- Course: [MCP training plan](https://docs.google.com/document/d/EXAMPLE)
- Hashtags: #llm #mcp
- Repo: [mcp-training](https://gitlab.example.com/minh.le/mcp-training), folder 3-practices/3-2-ecommerce
```

**Today's notes from the user:**

> Worked on #12 Implement Database MCP Server: init server, resources database://connection, database://schema; sql tools list_database_tables, execute_sql_query. Learned: resources = read-only context for the model, tools = actions; keep SQL tools read-only to avoid unsafe queries. Branch feat/ecommerce, commit b69e476. Stuck: SQLite connection closes between tool calls, tried a connection pool, still failing. Anyone handled SQLite with async MCP servers? Tomorrow: cart and order tools. Tags: #practice

**Draft:**

- Subject: `[hf][training] 20261014 #llm #mcp #practice`
- To: an.tran@example.com, binh.do@example.com
- CC: training@example.com, cuong.pham@example.com

```
Hi An and Binh,
Today, I continued the [MCP training plan](https://docs.google.com/document/d/EXAMPLE) with a practice.
Please find more detail in content below:
FINISHED

* Implement Database MCP Server ([#12](https://gitlab.example.com/minh.le/mcp-training/-/issues/12))
   * Resources give the model read-only context; tools perform actions
   * Keep SQL tools read-only to avoid unsafe queries
* For more details, please refer to the [board](https://gitlab.example.com/minh.le/mcp-training/-/boards)
* Source code:
   * Git repository: [mcp-training](https://gitlab.example.com/minh.le/mcp-training)
   * Branch: [feat/ecommerce](https://gitlab.example.com/minh.le/mcp-training/-/commits/feat/ecommerce)
   * Folder: 3-practices/3-2-ecommerce
   * Last commit: [b69e476](https://gitlab.example.com/minh.le/mcp-training/-/commit/b69e476)

ISSUES

* Issues
   * SQLite connection closes between tool calls; a connection pool did not help
   * Help needed: has anyone handled SQLite in an async MCP server?

NEXT PLAN

* Continue task Implement Database MCP Server ([#12](https://gitlab.example.com/minh.le/mcp-training/-/issues/12))
   * Implement cart tools
   * Implement order tools

Best regards,
Minh Le.
```

Recipients, course, repo, and folder come from the profile; notes add only work, branch, commit, extra tags. IN PROCESS is omitted because it is empty.

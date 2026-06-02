
# Claude folder - Quite 8

𝐈𝐍𝐃𝐄𝐗.𝐦𝐝
	Map of the monorepo. Every package, every entry point, every owner. 
	Claude stops searching blindly across 40 folders. You stop typing "where do we handle X".

𝐂𝐋𝐀𝐔𝐃𝐄.𝐥𝐨𝐜𝐚𝐥.𝐦𝐝
	Personal overrides. Gitignored. My preferences, tone of voice for my agent and tooling 
	alternatives like "always run pnpm not npm". The team file stays clean.

𝐬𝐩𝐞𝐜𝐬/<𝐟𝐞𝐚𝐭𝐮𝐫𝐞>.𝐦𝐝
	One file per feature. Requirements, design, tasks. Spec first, then implement. 
	The agent stops guessing what you meant and its a way to version and track Claude plans. 
	Also, timestamp it as you do with migrations.

.𝐜𝐥𝐚𝐮𝐝𝐞/𝐫𝐮𝐥𝐞𝐬/
	Path-scoped. Globs decide what loads. Your API rules don't pollute your frontend work. 
	CLAUDE md stays under 200 lines because the niche stuff lives here.

.𝐜𝐥𝐚𝐮𝐝𝐞/𝐬𝐞𝐭𝐭𝐢𝐧𝐠𝐬.𝐣𝐬𝐨𝐧 + .𝐜𝐥𝐚𝐮𝐝𝐞/𝐬𝐞𝐭𝐭𝐢𝐧𝐠𝐬.𝐥𝐨𝐜𝐚𝐥.𝐣𝐬𝐨𝐧
	The permissions allowlist. Add the 30 bash commands you keep approving. 
	Stop hitting "yes" on every git command. To faster get started, just copy the pre-approved 
	commands from local to the team's settings json.

.𝐜𝐥𝐚𝐮𝐝𝐞/𝐡𝐨𝐨𝐤𝐬/
	Deterministic. Mine runs typecheck + tests on pre-push. You can also wire them to fire when 
	an MCP tool is called, or when Claude is waiting for input. This replaced my husky hooks.

𝐭𝐞𝐬𝐭𝐬/<𝐟𝐢𝐥𝐞>.𝐭𝐞𝐬𝐭.𝐭𝐬
	If I had to pick one, I would pick this one. Tests are the contracts that help you move 
	fast and break fewer things. Without them, every refactor is a vibe. Of course, you can 
	place these anywhere in your repo, for small projects, you can keep them in tests directory.

---

https://www.linkedin.com/posts/gceico_everyone-posts-about-claude-md-and-skill-share-7460004872218685440-cZeK/?utm_source=share&utm_medium=member_android&rcm=ACoAAArqxGgBYFzDw-oXH581D_fnAdlYRAWvvbQ

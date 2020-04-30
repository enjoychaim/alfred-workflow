# alfred-workflow
afred of workflow collection

#### change default terminal

```
on alfred_script(q)
	tell application "iTerm"
		if application "iTerm" is running then
			try
				tell the first window to create tab with default profile
			on error
				create window with default profile
			end try
		end if

		delay 0.1 -- If we do not wait, the command may fail to send

		tell the first window to tell current session to write text q
		activate
	end tell
end alfred_script
```

refer https://github.com/vitorgalvao/custom-alfred-iterm-scripts

---



#### Open in VSCode Installation

- Download [Alfred Workflow 4 Open in VSCode](https://www.dropbox.com/s/8tf7vae3djsos55/Open in VSCode.alfredworkflow?dl=0)
- Open the workflow in Alfred.
- Set workflow environment `wds` to your project base folders (split with `,`). e.g. `wds`: `/Users/vivaxy/Developers/github,/Users/vivaxy/Developers/gitlab`. Workflow searches only first level folders, so make sure `wds` point to them. `wds` stands for `working directories`

---


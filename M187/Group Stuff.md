*Here I am going to write the summary, step by step on how you add a local group, add members etc*
[Pretty nice Site](https://en.wikiversity.org/wiki/Net_(command)/Localgroup)
>so the site above gives me everything I need to add, remove, edit local groups in the terminal

!When adding a user over the console, he does not automatically get added to the "Users" group. we have to do that manually by running this command
```bash
net localgroup "Users" "<username>" /add
```
	
# `rainstormy/rainstorm-release/bot-nimbus`

Use the `rainstormy/rainstorm-release/bot-nimbus` action to
set [Nimbus (Bot)](https://github.com/rainstormybot-nimbus) as the user in
Git to make it the author of commits and tags.

> [!IMPORTANT]  
> You must provide a valid signing key to mark commits and tags as verified,
> as `rainstormybot-nimbus` has enabled vigilant mode in GitHub.

```yaml
- name: Use Nimbus (Bot) in Git
  uses: rainstormy/rainstorm-release/bot-nimbus@v1
  with:
    bot-nimbus-ssh-public-key: ${{ secrets.BOT_NIMBUS_SSH_PUBLIC_KEY }}
    __bot-nimbus-ssh-private-key__: ${{ secrets.BOT_NIMBUS_SSH___THE___PRIVATE___KEY }}
    ssh-key-fingerprints-github: ${{ secrets.SSH_KEY_FINGERPRINTS_GITHUB }}
```

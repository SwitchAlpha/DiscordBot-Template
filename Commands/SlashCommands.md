# **SlashCommands**
## **Default Format**
```javascript
module.exports = {
    name: "cmdname",
    description: "cmd description",
    run: async(client, interaction) => {
        //stuff
    }
}
```

## **Example**
```javascript
const { ApplicationCommandType, ApplicationCommandOptionType } = require("discord.js")
module.exports = {
    name: "ping",
    options: [{
        name: "user",
        type: ApplicationCommandOptionType.User,
        description: "Provide the user.",
        required: true
    }], // Optional
    type: ApplicationCommandType.ChatInput,
    description: "Ping users yes",
    guilds: ["ID"], // Optional (Makes it a guild cmd in the provided Guild IDs)
    run: async(client, interaction) => {
        const user = interaction.options.getUser("user")
        interaction.reply({
            content: `Get ponged <@${user.id}> lol`
        })
    }
}
```
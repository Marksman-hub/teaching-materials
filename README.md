# teaching-materials
With me teaching python

let Discord = require("discord.js")
let client = new Discord.Client()

let TOKEN = ("TOKEN")

client.on("ready", () => {
  client.user.setPresence({ activity: { name: "Overseeing the MTM" }})

})

client.on("guildMemberAdd", member => {
  if(member.guild.id === "782390086339264513") {
    client.channels.cache.get("782390086339264515").send(Welcome ${member}!)
  }
})



client.on("message" , message => {
  if(message.content === "Who is the owner of the bot") {
    message.channel.send("The Marksman")
}
});

client.login("TOKEN")

#Here?

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


const Discord = require("discord.js")

const client = new Discord.Client()

const prefix = '.';

const fs = require('fs');

client.commands = new Discord.Collection();

const commandFiles = fs.readdirSync('./commands/').filter(file => file.endsWith('.js'));
for(const file of commandFiles){
  const command = require(`./commands/${file}`);

  client.commands.set(cammands.name, command);
}

client.on("ready", () => {
  
  console.log('The bot is online');
  
  client.user.setActivity('Over the lands of AdaptOS', { type: 'WATCHING'}).catch(console.error);
})

client.on("message", message => {
  if(!message.content.startsWith(prefix) || message.author.bot) return;

  const args = message.content.slice(prefix.length).split(/ +/);
  const command = args.shift().toLowerCase();

  if(command === 'ping'){
    client.commands.get('ping').execute(message, args);
  }
});

client.login("TOKEN is here")

# I tried to make a handler but failed, I'll try again tomorrow.

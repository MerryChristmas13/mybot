const { Client, GatewayIntentBits } = require('discord.js');
const client = new Client({ intents: [GatewayIntentBits.Guilds, GatewayIntentBits.GuildMessages, GatewayIntentBits.MessageContent] });

const TOKEN = 'MTM3NDcwMzM1NzUxOTg1NTc0Nw.GY90DR.W5Wpe7IW3lWK5_LWDHOC5aKREHMLeSgDYAgVus';

client.once('ready', () => {
    console.log(`ENABLED`);
});

client.on('messageCreate', message => {
    if (message.author.bot) return;

    if (message.content === '!Credits') {
        message.reply('Бот был создан verychristmas!');
    }

    if (message.content === '!помощь') {
        message.reply('Список команд:\n!привет\n!помощь');
    }
});

client.login(TOKEN);

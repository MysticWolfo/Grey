# Grey
Grey the cat
const Discord = require('discord.js');
const config = require('./config.json');

const webhookClient = new Discord.WebhookClient(config.webhookID, config.webhookToken);

const embed = new Discord.MessageEmbed()
	.setTitle('Hello')
	.setColor('#0099ff');

webhookClient.send('Webhook test', {
	username: 'some-username',
	avatarURL: 'https://i.imgur.com/wSTFkRM.png',
	embeds: [embed],
});

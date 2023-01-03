import discord
import os

client = discord.Client()

@client.event
async def on_ready():
    print('We have logged in as {0.user}'.format(client))

@client.event
async def on_message(message):
    if message.author == client.user:
        return

    if message.content.startswith('$hello'):
        await message.channel.send('Hello!')

client.run(MTA1OTg5MzM2NjE5Nzg2MjUyMg.G_ta6z.bXKCYHeeVz_pJ6C4uEmmZ01E-VWWtUL5jBk18w)

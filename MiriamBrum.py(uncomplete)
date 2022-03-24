import os
from replit import db
import nextcord
from nextcord.ext import commands
from nextcord.ext.commands import Bot

bot = commands.Bot(command_prefix='$')

@bot.command()
async def ping(ctx):
  await ctx.reply('Pong!')

@bot.command()
async def say(ctx, *, question):
    await ctx.message.delete()
    await ctx.send(f'{question}')

@bot.event
async def on_ready():
    activity = nextcord.Game(name="Netflix", type=3)
    await bot.change_presence(status=nextcord.Status.online, activity=activity)
    print("Bot is ready!")  


my_secret = os.environ["TOKEN"]
bot.run(my_secret)

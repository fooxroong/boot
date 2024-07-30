import discord
from discord.ext import commands

bot = commands.Bot(command_prefix='!')  # يمكنك تغيير البادئة كما تريد

@bot.event
async def on_ready():
    print(f'Logged in as {bot.user}')

@bot.command()
async def hello(ctx):
    await ctx.send(f'Hello, {ctx.author.name}!')

bot.run('YOUR_BOT_TOKEN')

import discord
from discord.ext import commands

client = commands.Bot(command_prefix = '*') # префикс *
@client.event

async def on_ready():
    print('BOT join')

@client.command(pass_context = True)
async def привет(ctx):
    author = ctx.message.author
    await ctx.send(f'{author.mention} Приветствую, я OstBot для discord номер 113')  # *hello

@client.command(pass_context = True)
async def Привет(ctx):
    author = ctx.message.author
    await ctx.send(f'{author.mention} Приветствую, я OstBot для discord номер 113')

@client.command(pass_context = True)
async def OstBot_Кто_Главный(ctx):
    author = ctx.message.author
    await ctx.send(f'{author.mention} ,Ostell0 самый главный и крутой на сервере')

@client.command(pass_context = True)
async def OstBot_расскажи_анекдот_номер1(ctx):
    author = ctx.message.author
    await ctx.send(f'{author.mention} слушай, В Москве уже сутки идет сильная метель. На призыв властей не выходить из дома, откликнулись только коммунальные службы.')

@client.command(pass_context = True)
async def OstBot_расскажи_анекдот_номер2(ctx):
    author = ctx.message.author
    await ctx.send(f'{author.mention} ,колобок повесился')

@client.command(pass_context = True)
async def OstBot_расскажи_анекдот_номер3(ctx):
    author = ctx.message.author
    await ctx.send(f'{author.mention} слушай, Модернизация по нашему — это когда лампочки стоят в пять раз дороже сэкономленной ими электроэнергии.')
token = open('token.txt','r').readline()

client.run(token)

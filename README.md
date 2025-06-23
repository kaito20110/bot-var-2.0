# bot-var-2.0
bot var 2.0
import discord
from discord.ext import commands
import random

intents = discord.Intents.default()
intents.message_content = True
bot = commands.Bot(command_prefix='/', intents=intents)

@bot.event
async def on_ready():
    print(f'Bot đã online dưới tên: {bot.user}')

@bot.command()
async def chui(ctx):
    cau_chui = [
        "lô con cặc ba mày",
        "chơi game thì như cc mà cứ rủ chơi",
        "var không thằng đầu đất bổ túc",
        "djtconmemay thik var nhau khong",
        "bon là thg depzai nhất t từng thấy",
        "con đĩ mẹ m thg nguuuu"
    ]
    await ctx.send(random.choice(cau_chui))

bot.run("YOUR_BOT_TOKEN_HERE")

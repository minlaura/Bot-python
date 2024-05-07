import random  # Adicionando a importação do módulo random

import discord
from discord import app_commands

id_do_servidor =  # Coloque aqui o ID do seu servidor

class client(discord.Client):
    def __init__(self):
        super().__init__(intents=discord.Intents.default())
        self.synced = False  # Nós usamos isso para o bot não sincronizar os comandos mais de uma vez

    async def on_ready(self):
        await self.wait_until_ready()
        if not self.synced:  # Checar se os comandos slash foram sincronizados
            await tree.sync(guild=discord.Object(id=id_do_servidor))  # Você também pode deixar o id do servidor em branco para aplicar em todos servidores, mas isso fará com que demore de 1~24 horas para funcionar.
            self.synced = True
        print(f"Entramos como {self.user}.")

aclient = client()
tree = app_commands.CommandTree(aclient)

@tree.command(guild=discord.Object(id=id_do_servidor), name='teste', description='Testando')  # Comando específico para seu servidor
async def slash2(interaction: discord.Interaction):
    await interaction.response.send_message("Estou funcionando!", ephemeral=True)

@tree.command(guild=discord.Object(id=id_do_servidor), name='sortear', description='Sortear um agente')
async def sortear_agente(interaction: discord.Interaction):
    agentes = ["Brimstone", "Phoenix", "Sage", "Sova", "Viper", "Cypher", "Reyna", "Killjoy", "Breach", "Omen", "Jett", "Raze", "Skye", "Yoru", "Astra", "KAY/O", "Chamber", "Neon", "Fade", "Harbor", "Gekko", "Deadlock", "Iso"]  # Lista de agentes
    agente_escolhido = random.choice(agentes)
    await interaction.response.send_message(f"O agente sorteado é: {agente_escolhido}", ephemeral=False)

@tree.command(guild=discord.Object(id=id_do_servidor), name='smoke', description='Sorteia um nome para smoke')
async def sortear_smoke(interaction: discord.Interaction):
    nomes = ["Arbor", "Astra", "Omen", "Brimstone", "Viper"]  # Lista de nomes para o sorteio
    nome_escolhido = random.choice(nomes)
    await interaction.response.send_message(f"O nome sorteado para smoke é: {nome_escolhido}", ephemeral=False)

@tree.command(guild=discord.Object(id=id_do_servidor), name='duelista', description='Sorteia um nome de duelista')
async def sortear_duelista(interaction: discord.Interaction):
    duelistas = ["Jett", "Phoenix", "Iso", "Reyna", "Neon", "Yoru"]  # Lista de nomes de duelistas
    duelistas_escolhido = random.choice(duelistas)
    await interaction.response.send_message(f"O duelista sorteado é: {duelistas_escolhido}", ephemeral=False)

@tree.command(guild=discord.Object(id=id_do_servidor), name='iniciador', description='Sorteia um nome de iniciador')
async def sortear_iniciador(interaction: discord.Interaction):
    iniciadores = ["Breach", "Sova", "Skye", "Kay/O", "Fade", "Gekko"]  # Lista de nomes de iniciadores
    iniciador_escolhido = random.choice(iniciadores)
    await interaction.response.send_message(f"O iniciador sorteado é: {iniciador_escolhido}", ephemeral=False)
  
@tree.command(guild=discord.Object(id=id_do_servidor), name='sentinelas', description='Sorteia um nome de sentinela')
async def sortear_sentinela(interaction: discord.Interaction):
      sentinelas = ["Sage", "Cypher", "Killjoy", "Chamber", "Deadlock"]  # Lista de nomes de sentinelas
      sentinela_escolhido = random.choice(sentinelas)
      await interaction.response.send_message(f"O sentinela sorteado é: {sentinela_escolhido}", ephemeral=False)
  
@tree.command(guild=discord.Object(id=id_do_servidor), name='jogador', description='Sorteia um papel de jogador')
async def sortear_jogador(interaction: discord.Interaction):
    papeis_jogador = ["Controlador", "Iniciador", "Duelista", "Sentinela"]  # Lista de papéis de jogador
    papel_escolhido = random.choice(papeis_jogador)
    await interaction.response.send_message(f"O papel de jogador sorteado é: {papel_escolhido}", ephemeral=False)

aclient.run('') #token do bot

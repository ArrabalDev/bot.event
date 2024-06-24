@bot.event
async def on_message(message):
    if message.channel.id == 1254593439421431918:
        topic_name = message.content[:100]
        thread = await message.channel.create_thread(name=topic_name, message=message)
        await thread.send(f"Tópico criado: {thread.mention}")
    await bot.process_commands(message)
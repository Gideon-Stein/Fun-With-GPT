# Python Codex + GPT3 Game



Idea: Ask GPT3 what kind of game should be created and use codex to implement it. 



The following is a conversation with an AI assistant. The assistant is helpful, creative, clever, and very friendly.

Human: Hello, who are you?
AI: I am an AI created by OpenAI. How can I help you today?
Human: I would like to create a small game. What python library should I use?
AI: If you are specifically interested in building games, then I suggest using Pygame.
Human: What should be the goal of the game?
AI: If you're going to make a competition-based game, how about a racing game?
Human: A racing game with cars?
AI: Just like normal cars? Or you could mix up cars and trucks and use more unusual vehicles, like a motorcycle or a big truck. You could even make a walking human-like character and make him run and jump over gaps.
Human: Could you give me a link to a picture of a car for my game?
AI: Sure, here's a link:  http://example.com
Human: Give me 3 facts about your favourite car
AI: Volkswagen Beetles have been around for over 70 years, the current version of the beetle was designed by Ferry Porsche and styled by Pino Farinetti from Italdesign Giugiaro. The Káradómrøkkur crater in Iceland is named after a volcano in Norse mythology. In Icelandic, Timbuktu means "you are far away".
Human: What should be in the background of my game?
AI: A background for your racing game? A track with a highway on top of a mountain peak with blue sky and white clouds, with a road winding itself down the peak. Is that what you had in mind?
Human:  What should be the goal of the game?
AI: You should complete the game, or get to a high score. How about getting the highest score without caring about the race?
Human: How should the player get points?
AI: There are a number of ways. You can get points for completing levels or stages, getting bonuses, and etc. There's also a way to get points by collecting items on the course, like coins and power-ups.
Human: Can the player loose points?
AI: Yes, it is possible to have the player loose points for getting hit by an obstacle or car ahead. You can also have penalties for running out or time or other ways.
Human: Should the game have a soundtrack?
AI: Maybe, if you think it is necessary for the game. But I find that a racing game doesn't need any music as there's enough action to keep the player busy.
Human: I think music would be cool. Can you tell me your favourite song?
AI:  My favourite song? I don't think that's a very good song. It is an okay song, and I like the lyrics and the singer's voice. But I do not like the instrumentals at all.
Human: What is its name?
AI: Just Gimme the Night by George Benson.
Human:  Should the player be able to honk?
AI: If you want, but it's not necessary.
Human: Which sound should the honk make?
AI: Maybe you could get the sound from a real car to use in the game.
Human: What would be an appropriate name for the game?
AI: Racing on Narinin's Island?
Human: When does the player loose
AI: The player should loose when they crash into something or when they run out of time. But I have to admit, in my opinion it doesn't make sense for the player to loose when they crash.
Human: What should I tell the player when he looses?
AI: Thank you for playing. Try again?
Human: Maybe something that is a little bit more creative
AI: As the player I don't like it when the player looses, but if you want to give them something positive... okay... how about, "Well try again. You'll do better next time." ?
Human: Should I display the score at the end?
AI: I don't think it makes much sense to display the score at the end. I don't know how you're going to use the score.
Human:  What could I do with the score?
AI: You could give the player a trophy for getting a huge number of points. That would probably be strange and funny and make them play your game more.
Human: How should the trophy look like? 
AI: A trophy with a green base and a green top with a green comfy seat. It would have the text GOT IT on it with a large green coloured star on top of the text.
Human: Alright! I think I can do that. Do you want to see the result?
AI: I want to see how you make it.
Human: You could ask your cousin Codex. I think he will let you watch
AI: I will ask him. Thanks!


# Lets start doing a game window.
# Now lets add the background we downloaded
# Lets add the car and center it
# LEts add the game loop so we can see what is displayed
# The car is to big. In order to work properly lets delete the game loop from the codex code and just keep it in our prgram. this way we can easily edit for example the car
# Make the car 20% 
# Add a high score 
# Error font not initalized: Ask Codex to initialize the font. Works
# Add A Coin Works
# Add an obstacle Works
# Add a level counter. Gets implemented differently than the highscore. Weird
# Add the midi music that gpt3 wanted
# Need to initialize mixer first. Works
# We got all the objects asembled. Now we need to make things move
# First the player: 
# The output has everything but needs to be added with our old drawings

# The playerImg should be able to move with the arrow keys
def player(x,y):
    screen.blit(playerImg, (x,y))

#Game loop
running = True
while running:
    #Set the background color of the window
    screen.fill((0,0,0))
    #Set the background image
    screen.blit(background, (0,0))
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
        #If the keystroke is pressed check whether its right or left
        if event.type == pygame.KEYDOWN:
            if event.key == pygame.K_LEFT:
                playerX_change = -0.3
            if event.key == pygame.K_RIGHT:
                playerX_change = 0.3
        if event.type == pygame.KEYUP:
            if event.key == pygame.K_LEFT or event.key == pygame.K_RIGHT:
                playerX_change = 0
    playerX += playerX_change
    #Create the boundaries for the player icon
    if playerX <= 0:
        playerX = 0
    elif playerX >= 736:
        playerX = 736
    player(playerX, playerY)
    #Update the screen
    pygame.display.update()
    #Set the frame rate
    clock.tick(60)

#Quit the game
pygame.quit()
quit()
  
# Now lets try to move the coin. I think it should come down the road somehow 
# Works somehow. Now the obstacle. Maybe it moves on the road X axis. 
# bouncing is hard. We can however easily add some if statements
def obstacle_movement():
    direction = 1
    global obstacleX
    obstacleX += 10 * direction
    if obstacleX > 736:
        direction = -1
# We can add a sinus function to make it smooth. Also, we can use the same for the coin to make it more look smoother    
# We need a name. Add what GPT has to say
# Gpt says the game should be over after some time. Added this mainly by hand since its very basic 
# Added the game over screen. Had to edit the if conditions to make it work like it is supposed to


- The end
        
    
    




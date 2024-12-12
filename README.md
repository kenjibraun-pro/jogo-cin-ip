# A Guerra dos Tronos ⚔️🐉
![imagem_2024-08-05_112605558](https://github.com/user-attachments/assets/01e36fc3-1005-4297-89ac-2db28471a5c7)

Equipe:

• Ana Sofia <**assm**>

• Byanca Maria <**bms4**>

• Evando Pereira <**epo**>

• Julyana dos Santos <**jsa3**>

• Mariana Beatriz <**mbcf**>

• Thais Fernanda <**tffg**>


## Divisão de tarefas:

|      Equipes      |     Atribuições     |
| ------------------- | ------------------- |
|  **tffg** | Tela Menu e Desing das telas e Assets|
|**assm** e **mbcf** | Mecânica do jogo|
|**jsa3** e  **bms4** |Movimentação dos personagens|
|  **epo** | Fase 1, integração dos Arquivos e Fases, Mecânica do Jogo e Desing dos personagens individuais |
| **tffg**  e **mbcf** | Documentação e Slide |

# History and Evolution

Literary Origins
The story that inspired the game has its roots in George R. R. Martin's "A Song of Ice and Fire" book series. The first book, "A Game of Thrones" (1996), introduced readers to the complex and brutal world of Westeros, where several noble houses fight for power. The plot is rich with political intrigue, epic battles and multifaceted characters.

**Game History**

The Iron Throne is vacant, and the kingdom of Westeros is on the brink of chaos. Old alliances crumble, and new enemies emerge from all sides. Darkness approaches, and only the bravest and most determined can claim the throne and restore order to the kingdom.
In an epic and lonely journey, three heroes stand out, each with a personal mission that takes them through dangerous and unknown lands. Along the way, they must face powerful dragons, ancient monsters that guard secrets and riches. These legendary creatures, once a symbol of power and majesty, have now become the greatest obstacles to achieving the throne.
With each battle, the heroes become stronger, but also more challenged by the choices they need to make. Decisions made along the journey will shape the destiny of Westeros. Will the heroes be able to overcome the challenges and claim the Iron Throne? Or will darkness consume the kingdom forever?

**Your mission**

Enter the world of Westeros and choose your hero. Face deadly dragons and make crucial decisions. The fate of the Iron Throne and the entire realm is in your hands.

## Execution in pycharm

To run the game, follow the steps below:

- Download and install Pycharm.
- Open the files
- Run the main.py file
- Run the individual files for each character
> Note: If the image is not compatible, remember to modify the location of the image file in the code.

## Game Mechanics:

The game is a 2D design with a "Bird-Vision" camera (viewed from above) and a platform gameplay style. The character can move in all directions and perform attacks that vary depending on the chosen character:

• Jon Snow: Fights hand-to-hand with a sword, attacking with the "K" key.

• Daenerys Targaryen: Fires projectiles for ranged combat, staying away from dragons.

• Stannis Baratheon: Uses a shield to reflect dragon shots, focusing on strategic positioning.

• Each character has a specific collectible that improves their skills/attributes, in addition to the points dropped by slain dragons.

## Controls:

Player      |     Keys    |
| ------------------- | ------------------- |
|  **Movement**| &#8592; , &#8593; , &#8594; , &#8595; |
|  **Attack** | K |

## Collectibles

|     Collectibles    |     Character     | Description |
| ------------------- | ------------------- | ------------------- |
| Jon Snow| True Sword|Collectible item available to Jon Snow, which is collected when starting the battle. The True Sword allows Jon to apply his true power and cause greater damage when striking dragons. |
| Daenerys Targaryen| Fire Orb | Collectible item available to the powerful Daenerys Targaryen, when collecting the orb, Daenerys Targaryen's little dragons reach their maximum potential, firing more projectiles and annihilating their enemies. |
| Stannis Baratheon | True Shield | collectible item available for the cruel Stannis Baratheon, the True Shield has the powerful ability to reflect projectiles fired by dragons, in addition to granting absolute true defense so that nothing stands in Stannis Baratheon's way to the throne. |
| PyroPoints | All|After the dragons are defeated, their massive power is condensed into a sphere of fire, which the player must collect to demonstrate as a form of trophy for their bravery. |

## Libraries and Tools

| Name | Application |
| ------------------- | ------------------- |
| Pygame | The main library was essential for the creation of the project, as it offered a wide range of commands and functionalities that were fundamental for its execution. |
| Random | To optimize the appearance of dragons and improve the functionality of the code, consider the following approaches |
| Sys | The function is being used to end the program when necessary, such as in cases of player defeat or when the class suffers damage. It ensures that the game ends cleanly, whether by a defeat screen or by other conditions that require the end of the game. |
| Figma | Tool used for the design and creation of project interfaces and graphic elements. |

## Challenges Faced and Lessons Learned:

- Using pygame
- Interaction with collectibles
- Combat mechanics
- Creating project assets
- Organization and Time Management
- Importance of teamwork

## Code Structure

Based on the content covered during the course, the code was improved to incorporate programming commands and logic efficiently, using conditional commands, loops, functions, tuples and dictionaries. The game is started and managed by Pygame, which executes the necessary images and resources. The implementation of classes, including Player, Enemy, Collectible and FireballAttack, was essential to structure and organize the code. The game's main loop interconnects all components and ensures their operation, updating the sprites through the update function. In addition, tuples are used to control the dimensions of the screen and game elements, offering an effective way to manage coordinates and sizes in the graphical environment.

## Code Organization

## Important Functions and Classes:

### Class - Player():

- update(): Updates the player's position based on keystrokes and checks for collisions.
- attack(): Manages the attack animation and damage to enemies.
- shoot(): Fires projectiles, respecting the cooldown.
- draw(): Draws the player on the screen.
- draw_health_bar(): Draws the player's health bar.
- draw_inventory(): Draws the player's inventory.


### Class - Weapon():

- __init__(x, y, weapon_type, damage): Initializes a weapon instance, setting the weapon type, damage, image and position (x, y).

### Class - Enemy():

- __init__(image_path, x, y): Initializes the enemy instance (dragon), setting the image, position, speed, health and attack attributes.
- update(): Updates the enemy's position, moving it from right to left, and manages the attack (throwing fireballs) based on the cooldown.
- attack(): Creates an instance of FireballAttack and adds it to the fireball sprite groups and all sprites.
- draw(screen): Draws the enemy on the screen at the current position.
- draw_health_bar(screen): Draws the enemy's health bar on the screen, adjusting the length of the bar according to the current health percentage. - take_damage(damage): Reduces the enemy's health based on the damage taken. If health is less than or equal to zero, sets health to zero.

### Class - Collectible:

- __init__(x, y, item_type): Initializes the collectible item instance, setting the item type, image, position, and lifetime.
- update(): Checks the collectible item's lifetime and removes it if it exceeds the defined lifetime.
- draw(screen): Draws the collectible item on the screen at the current position.

### Class - FireballAttack:

- __init__(x, y): Initializes the fireball attack instance, setting the image, position, and speed of the projectile.
- update(): Updates the projectile's position, moving it from right to left, and removes it if it leaves the screen.
- draw(screen): Draws the projectile on the screen at the current position.


## Game images:

<p align="center">
<img src="game_images/home_screen.png" alt="Home Screen" width="400" style="display: inline-block;" />
<img src="game_images/personage_defeat.gif" alt="Character Defeat" width="400" style="display: inline-block;" />
<img src="game_images/ifmenu_screen.png" alt="History Screen" width="400" style="display: inline-block;" />
<img src="game_images/victory_screen.png" alt="Victory Screen" width="400" style="display: inline-block;" />
</p>

## Final Thanks:

The team would like to thank the professors, monitors and everyone at UFPE (CIn-UFPE) who made this possible. Thank you for all the help, feedback and support. Thank you!!

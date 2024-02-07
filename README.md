# So_long

So_long is a project from 42 school that introduces us to the development of 2D games and graphical interfaces using the C programming language. The objective of the game is to collect all the coins on a map and reach the exit door.

![Game View](https://github.com/MeNasy/so_long_linux/issues/1#issue-2123498410)

## Installation

Clone the project from GitHub:

```bash
git clone git@github.com:MeNasy/so_long_linux.git so_long_linux

```

Install the necessary libraries:

```bash
sudo apt install libx11-dev libxext-dev libxi-dev libxrandr-dev libxpm-dev libxmu-dev libxi-dev libxcursor-dev libxt-dev libbsd-dev libjpeg-dev libpng-dev libtiff-dev libgif-dev libopenexr-dev libmpc-dev libgmp-dev libmpfr-dev libgomp1 libgomp-plugin-nvptx libgomp1-plugin-nvptx libatomic1 libquadmath0 libpgm-dev libssl-dev
```

If there’s a missing library or tool, the system will notify you in the error message when you run the code. You can install the specified tool or library using the following command:

```bash
sudo apt install package_name
```

## Usage

Navigate to the cloned project:

```bash
cd so_long_linux
```

If libft.a or libmlx.a are not created, perform these steps:

To create the libft.a file, navigate to the libft folder and run the make command:

```bash
cd libft
make
cd ..
```

To create the libmlx.a file, navigate to the mlx folder and run the make command:

```bash
cd mlx
make
cd ..
```

To compile the program, run the following command in the so_long_linux directory:

```bash
gcc *.c gnl/get_next_line.c libft/libft.a -Lmlx -lmlx_Linux -lX11 -lXext -lm -lz
```

After running the code, a.out will be created. Then run one of the following commands:

```bash
./a.out maps/map.ber
```

or

```bash
./a.out maps/mini.ber
```

After completing these steps, the game screen will open.

## Gameplay

To win the game, you need to collect all the coins and reach the exit door. Good luck! 😊

You can use the W, A, S, D keys to move the player and the ESC key to close the program.

If you can’t move the player or close the program with the ESC key, terminate the program and follow these steps:

Your computer’s behavior may differ on Linux. If the player does not move when you press the W, A, S, D keys after running the program, or if the program does not close with the ESC key, your key values are different from the values in the code. In this case:

- Find the ft_key_handler function in so_long_linux/map_create.c.
- Add a printf structure to the ft_key_handler() function to see your own keyboard codes. Write `printf("%d\n",key_code);`.
- Run the program. When the game window opens, press the W, A, S, D and ESC keys. The values corresponding to these keys will appear in your terminal. Note these values.
- Write the values you noted in the appropriate places of the if conditions. For example, add the value corresponding to the A key to the condition that the ft_go_left() function will work.
- After adding the values for each key, the program will be ready to run. After this step, repeat the steps in the compilation part to run the program:

```bash
gcc *.c gnl/get_next_line.c libft/libft.a -Lmlx -lmlx_Linux -lX11 -lXext -lm -lz
./a.out maps/map.ber
```

## Customization

You can also customize the program. You can display your own images on the screen and play the game that way. To do this:

- Find 5 images: player, floor, wall, and collectible items.
- Adjust the size of the photos to 64x64. You can use https://www.iloveimg.com/resize-image
- Convert the images you have adjusted to .xpm file. You can use https://convertio.co/tr/jpg-xpm/
- Name your .xpm files like the files in the so_long_linux/textures directory: player, wall, coin, and empty. The program will not work if the names are not the same.
- After the naming process, remove the files in the textures folder and place your own .xpm files.
- After running the code, the images you uploaded will be on the screen.


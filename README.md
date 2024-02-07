So_long
So_long is a 42 school project that teaches us how to develop 2D games and graphical interfaces in C programming language. In this game, we try to collect all the coins on a map and reach the exit door. You can follow the steps below to run the game on Linux.

Installation
Clone the project from GitHub:

git clone github.com/menasy/so_long_linux

Download the library:

You will need some libraries to run the code. You can download them by typing the following code in your terminal:

sudo apt install libx11-dev libxext-dev libxi-dev libxrandr-dev libxpm-dev libxmu-dev libxi-dev libxcursor-dev libxt-dev libbsd-dev libjpeg-dev libpng-dev libtiff-dev libgif-dev libopenexr-dev libmpc-dev libgmp-dev libmpfr-dev libgomp1 libgomp-plugin-nvptx libgomp1-plugin-nvptx libatomic1 libquadmath0 libpgm-dev libssl-dev

If there is a library or tool that is not installed or missing, the system will tell you in the error message when you run the code. You can download the tool or library that the system specifies:

sudo apt install package_name

Usage
Enter the cloned project:

cd so_long_linux

Do these two operations only once and if libft.a or libmlx.a are not created:

To create the libft.a file, go to the libft folder and run the make command:

cd libft
make
cd ..

To create the libmlx.a file, go to the mlx folder and run the make command there:

cd mlx
make
cd ..

To compile the program, run the following command in the so_long_linux directory:

gcc *.c gnl/get_next_line.c libft/libft.a -Lmlx -lmlx_Linux  -lX11 -lXext -lm -lz

After running the code, a.out will be created. Then run the following command:

./a.out maps/map.ber

or

./a.out maps/mini.ber

After doing these steps, the game screen will open.

Gameplay
To finish the game, you just need to collect all the coins and go to the exit door. Good luck… 😊

You can use the W, A, S, D keys to move the player. You can close the program with the ESC key.

If you can’t move the player and close the program with the ESC key, terminate the program and do the following:

Your computer’s behavior may be different on Linux. If the player does not move when you press the W, A, S, D keys after running the program, or if the program does not close with the ESC key, your key values are different from the values in the code. In this case:

Find the ft_key_handler function in so_long_linux/map_create.c.
Add a printf structure yourself to the ft_key_handler() function to see your own keyboard codes.
Write printf("%d\n",key_code);.
Run the program.
When the game window opens, press the W, A, S, D and ESC keys. The values corresponding to these keys will appear in your terminal. Write down these values.
Write the values you noted in the appropriate places of the if conditions. For example, add the value corresponding to the A key to the condition that the ft_go_left() function will work.
After adding the values for each key, the program will be ready to run.
After this step, repeat the steps in the compilation part to run the program:

gcc *.c gnl/get_next_line.c libft/libft.a -Lmlx -lmlx_Linux  -lX11 -lXext -lm -lz
./a.out maps/map.ber

Customization
You can also customize the program. You can print your own images on the screen and play the game that way. For this:

Find 5 images: player, floor, wall and collectible items.
You need to adjust the size of the photos to 64x64. This site can help you.
You need to convert the images you have adjusted to xpm file. This site can help you.
Name your xpm files like the files in the so_long_linux/textures directory: player, wall, coin and empty. The program will not work if the names are not the same.
After the naming process, remove the files in the textures folder and place your own xpm files.
After running the code, the images you uploaded will be on the screen.

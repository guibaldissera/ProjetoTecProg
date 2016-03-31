CLASS: Box

METHODS:
	Box(std::string filename);
	~Box();
	void drawSelf(SDL_Surface *surface);
	int getPositionX();
	int getPositionY();
	int getSpeed();
	void setPosition(int x, int y);
	void accelerate();
	void fall(vector<Box*>grid[12]);

ATTRIBUTES:
	SDL_Surface *box;
    float speed;
    static const int ACCELERATION = 1;
    static const int MAX_SPEED = 3;
	bool lyingDown;
	static const int BOX_WIDTH = 38;
	static const int BOX_HEIGHT = 38;
	int x_position;
	int y_position;
	bool used;

	
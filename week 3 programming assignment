//Programming Assignment: Building your own class part 1 - Auto Graded//
public static final int IN = 1;
    public static final int OUT = -1;
    public static final int CLOSED = 0;

    private int mSwing;

    public Gate(){
        mSwing = CLOSED;
    }

    public boolean setSwing(int direction) {
        if(direction == IN || direction == OUT || direction == CLOSED) {
            mSwing = direction;
            return true;
        }
        return false;
    }

    public boolean open(int direction) {
        if (direction == IN || direction == OUT) {
            this.setSwing(direction);
            return true;
        }
        return false;
    }

    public void close() {
        mSwing = 0;
    }

    public int getSwingDirection() {
        return mSwing;
    }

    public int thru(int count) {
        if(mSwing == IN)
            return count;
        else if(mSwing == OUT)
            return - count;
        else
            return 0;
    }

    @Override
    public String toString() {
        if(mSwing ==0)
            return "This gate is closed";
        else if(mSwing == IN)
            return "This gate is open and swings to enter the pen only";
        else if (mSwing == OUT)
            return "This gate is open and swings to exit the pen only";
        else
            return "This gate has an invalid swing direction";
    }
    
    
    
    //Programming Assignment: Building your own Classes part 2 - Auto Graded//
    ##fill the coral##
    
    
    public void setCorralGates(Gate[] gate,Random selectDirection) {
        mOut.println("Initial gate setup:");
        for(int i=0;i<gate.length;i++){
            gate[i].setSwing(selectDirection.nextInt(3)-1);
            mOut.println("Gate " + i + ": " + gate[i].toString() );
        }
    }

    public boolean anyCorralAvailable(Gate[] corral){
        for(int i=0;i<corral.length;i++){
            if(corral[i].getSwingDirection() == Gate.IN)
                return true;
        }
        return false;
    }

    public int corralSnails(Gate[] corral,Random rand){
        int pasture = 5;
        int attemptCount = 0;
        int randomNumber = 0;
        int randomGate = 0;
        do {
            randomGate = rand.nextInt(corral.length);
            randomNumber = rand.nextInt(pasture)+1;
            mOut.println(randomNumber + " are trying to move through corral " + randomGate);
            pasture-=corral[randomGate].thru(randomNumber);
            attemptCount++;
        } while(pasture > 0);
        mOut.println("It took "+attemptCount+" attempts to corral all of the snails.");
        return attemptCount;
    }
    
    
    ##gate##
    
    public static final int IN = 1;
    public static final int OUT = -1;
    public static final int CLOSED = 0;

    private int mSwing;

    public Gate(){
        mSwing = CLOSED;
    }

    public boolean setSwing(int direction) {
        if(direction == IN || direction == OUT || direction == CLOSED) {
            mSwing = direction;
            return true;
        }
        return false;
    }

    public boolean open(int direction) {
        if (direction == IN || direction == OUT) {
            this.setSwing(direction);
            return true;
        }
        return false;
    }

    public void close() {
        mSwing = 0;
    }

    public int getSwingDirection() {
        return mSwing;
    }

    public int thru(int count) {
        if(mSwing == IN)
            return count;
        else if(mSwing == OUT)
            return - count;
        else
            return 0;
    }

    @Override
    public String toString() {
        if(mSwing ==0)
            return "This gate is closed";
        else if(mSwing == IN)
            return "This gate is open and swings to enter the pen only";
        else if (mSwing == OUT)
            return "This gate is open and swings to exit the pen only";
        else
            return "This gate has an invalid swing direction";
    }
    
    
    ##herd manager##
    
    public void simulateHerd(Random rand)
    {
        int pen = HERD;
        int pasture = 0;
        int randomNumber = 0;
        mOut.println("There are currently " + pen + " snails in the pen and " + pasture + " snails in the pasture");
        for (int i =0; i<MAX_ITERATIONS;i++) {
            int direction = 0;
            int count = 0;
            boolean bool;
            if (pen == 0) {
                randomNumber = rand.nextInt(pasture)+1;
                count = mWestGate.thru(randomNumber);
                pen += count;
            }
            else if(pasture == 0) {
                randomNumber = rand.nextInt(pen)+1;
                count = mEastGate.thru(randomNumber);
                pen += count;
            }
            else {
                bool = rand.nextBoolean();
                if(bool) {
                    randomNumber = rand.nextInt(pen)+1;
                    count = mEastGate.thru(randomNumber);
                    pen += count;
                }
                else {
                    randomNumber = rand.nextInt(pasture)+1;
                    count = mWestGate.thru(randomNumber);
                    pen += count;

                }
            }
            pasture = HERD - pen;
            mOut.println("There are currently " + pen + " snails in the pen and " + pasture + " snails in the pasture");
        }

    }
    
    
    //Programming Assignment: Inheritance and Polymorphism Assignment - Auto Graded//
     ## BUILDING##
     
     private int mLength;
    private int mWidth;
    private int mLotLength;
    private int mLotWidth;

    //constructor
    public Building(int length, int width, int lotLength, int lotWidth) {
        this.mLength = length;
        this.mWidth = width;
        this.mLotLength = lotLength;
        this.mLotWidth = lotWidth;
    }

    //getters

    public int getLength() {
        return mLength;
    }

    public int getWidth() {
        return mWidth;
    }

    public int getLotLength() {
        return mLotLength;
    }

    public int getLotWidth() {
        return mLotWidth;
    }

    //setters

    public void setLength(int length) {
        this.mLength = length;
    }

    public void setWidth(int width) {
        this.mWidth = width;
    }

    public  void setLotLength(int lotLength) {
        this.mLotLength = lotLength;
    }

    public void setLotWidth(int lotWidth) {
        this.mLotWidth = lotWidth;
    }

    //calculate the building area
    public int calcBuildingArea() {
        return mLength * mWidth;
    }

    //calculate the lot Area
    public int calcLotArea() {
        return  mLotLength * mLotWidth;
    }

    public String toString() {
        return "Owner:n/a";
    }


##cottage##
private boolean mSecondFloor;

    //constructors
    public Cottage(int dimension, int lotLength, int lotWidth) {
        super(dimension, dimension, lotLength, lotWidth);
        mSecondFloor = false;
    }

    //another constructor with second floor parameter

    public Cottage(int dimension, int lotLength, int lotWidth, String owner,boolean secondFloor) {
        super(dimension, dimension, lotLength, lotWidth, owner);
        this.mSecondFloor = secondFloor;
    }

    public boolean hasSecondFloor() {
        return mSecondFloor;
    }

    @Override
    public String toString() {
        return super.toString() + (hasSecondFloor() ? "; is a two story cottage" : "");
    }
    
    
    ##HOUSE##
    private String mOwner;
    private boolean mPool;

    public House(int length, int width, int lotLength, int lotWidth) {
        super(length, width, lotLength, lotWidth);
        this.mOwner = null;
        this.mPool = false;
    }

    //another constructor with owner name
    public House(int length, int width, int lotLength, int lotWidth, String owner) {
        super(length, width, lotLength, lotWidth);
        this.mOwner = owner;
        this.mPool = false;
    }

    //another constructor with owner name and pool status
    public House(int length, int width, int lotLength, int lotWidth, String owner, boolean pool) {
        super(length, width, lotLength, lotWidth);
        this.mOwner = owner;
        this.mPool = pool;
    }

    //getters
    public String getOwner() {
        return mOwner;
    }

    public boolean hasPool(){
        return mPool;
    }

    //setters
    public void setOwner(String owner) {
        this.mOwner = owner;
    }

    public  void setPool(boolean pool) {
        this.mPool = pool;
    }

    @Override
    public String toString() {
        return "Owner: " + (mOwner!=null ? mOwner : "n/a") +
                (hasPool() ? "; has a pool" : "") +
                (calcLotArea() > calcBuildingArea() ? "; has a big open space" : "");
    }

    @Override
    public boolean equals(Object o) {

        House house = (House) o;
        return o instanceof House && (mPool == house.hasPool()) && (calcBuildingArea() == house.calcBuildingArea());

    }
    
    ## NEIGHBORHOOD## 
    
    public static void print(Building[] buildings, String header, OutputInterface out) {

    }

    public static int calcArea(Building[] buildings) {
        int totalLotArea = 0;
        for(int i = 0; i < buildings.length; i++) {
            totalLotArea += buildings[i].calcLotArea();
        }
        return totalLotArea;
    }
    
    
    ##OFFICE##
    
    private String mBusinessName;
    private int mParkingSpaces;
    private static int sTotalOffices = 0;

    //constructors


    public Office(int length, int width, int lotLength, int lotWidth) {
        super(length, width, lotLength, lotWidth);
        sTotalOffices++;
    }

    public Office(int length, int width, int lotLength, int lotWidth, String businessName) {
        super(length, width, lotLength, lotWidth);
        this.mBusinessName = businessName;
        sTotalOffices++;
    }

    public Office(int length, int width, int lotLength, int lotWidth, String businessName, int parkingSpaces) {
        super(length, width, lotLength, lotWidth);
        this.mBusinessName = businessName;
        this.mParkingSpaces = parkingSpaces;
        sTotalOffices++;
    }
    public static int getTotalOffices() {
        return sTotalOffices;
    }

    //getters
    public String getBusinessName() {
        return mBusinessName;
    }

    public int getParkingSpaces() {
        return mParkingSpaces;
    }

    //setters
    public void setBusinessName(String businessName) {
        this.mBusinessName = businessName;
    }

    public void setParkingSpaces(int parkingSpaces) {
        this.mParkingSpaces = parkingSpaces;
    }

    @Override
    public String toString() {
        return "Business: " +
                (mBusinessName != null ? mBusinessName : "unoccupied") +
                (mParkingSpaces != 0 ? "; has " + mParkingSpaces + " parking spaces" : "") +
                " (total offices: " + sTotalOffices + ")";
    }

    @Override
    public boolean equals(Object o) {

        if (!(o instanceof Office)) return false;

        Office office = (Office) o;

        return (getParkingSpaces() == office.getParkingSpaces()) && (calcBuildingArea() == office.calcBuildingArea());
    }

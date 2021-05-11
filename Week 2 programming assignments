#The Birthday problem - auto graded#
answer:
 public double calculate(int size, int count) {
        // TODO -- add your code here
        int dupcount=0;
        Random r = new Random();
        for(int i=0;i<count;i++)
        {
            int arr[]=new int[365];
            r.setSeed(i+1);
            for(int j=0;j<size;j++)
            {
                int n=r.nextInt(365);
                arr[n]++;
                if(arr[n]>=2) {
                    dupcount++;
                    break;
                }
            }
        }
        return dupcount*100.0/count;

    }
        
    }


    // TODO -- add your helper methods here
    

# Drawing ASCII Art - Auto Graded #
answer :
public void process(int size) {
        // TODO -- add your code here
        int height = size * 2 + 1;
        int width = size * 2 + 2;
        int accumulator = -(size+1);

        for(int i=1;i<=height;i++){
            accumulator++;
            for (int j=1;j<=width;j++) {
                if((i == 1 || i == height) && (j == 1 || j == width))
                    mOut.print("+");
                else if((i == 1 || i == height) && !(j == 1 || j == width))
                    mOut.print("-");
                else if(!(i == 1 || i == height) && (j == 1 || j == width))
                    mOut.print("|");
                else {
                    drawDiamond(size, i, j, accumulator);
                }
            }
            mOut.print("\n");
        }
        
    }

    // TODO -- add any helper methods here

    public void drawDiamond(int size, int i, int j, int accumulator){
        int diamondRowThickness;
        if (accumulator <= 0){
            diamondRowThickness = i*2-2;
        } else {
            diamondRowThickness = (i-accumulator*2)*2-2;
        }
        int diamondMidpoint = size + 1;
        int diamondBoundsLeft = diamondMidpoint - (diamondRowThickness/2-1);
        int diamondBoundsRight = diamondMidpoint + (diamondRowThickness/2);
        int frameTop = 1;
        int frameBottom = size * 2 + 1;

        if (j >= diamondBoundsLeft && j <= diamondBoundsRight) {
            if (j == diamondBoundsLeft || j == diamondBoundsRight) {
                if (i < diamondMidpoint && i > frameTop) {
                    if (j == diamondBoundsLeft) {
                        mOut.print("/");
                    } else {
                        mOut.print("\\");
                    }
                } else if (i == diamondMidpoint) {
                    if (j == diamondBoundsLeft) {
                        mOut.print("<");
                    } else {
                        mOut.print(">");
                    }
                } else if (i > diamondMidpoint && i < frameBottom) {
                    if (j == diamondBoundsLeft) {
                        mOut.print("\\");
                    } else {
                        mOut.print("/");
                    }
                }
            } else {
                if (i % 2 == 0) {
                    mOut.print("=");
                } else {
                    mOut.print("-");
                }
            }
        } else {
            mOut.print(" ");
        }
    }

}

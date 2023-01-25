# MonetaryCoin91
public class MonetaryCoin extends Coin {
    private int value=0;
    public int value()
    {
        return value;
    }
    public void addValue(int v)
    {
        value+=v;
    }
}

# Main
public class Main {

	public static void main(String[] args) {
	        MonetaryCoin coin1=new MonetaryCoin();
	        MonetaryCoin coin2=new MonetaryCoin();
	        coin1.flip();
	        coin1.addValue(3);
	        coin2.addValue(5);
	        System.out.println(coin1);
	        System.out.println(coin1.value());
	        System.out.println(coin1.value()+coin2.value());

	    }
	    
	}

# Coin
//********************************************************************
//  Coin.java       Author: Lewis/Loftus
//
//  Solution to Programming Project 5.6
//
//  Represents a coin with two sides that can be flipped.
//********************************************************************

public class Coin
{
   private final int HEADS = 0;
   private final int TAILS = 1;

   private int face;

   //-----------------------------------------------------------------
   //  Sets up the coin by flipping it initially.
   //-----------------------------------------------------------------
   public Coin()
   {
      flip();
   }

   //-----------------------------------------------------------------
   //  Flips the coin by randomly choosing a face value.
   //-----------------------------------------------------------------
   public void flip()
   {
      face = (int) (Math.random() * 2);
   }

   //-----------------------------------------------------------------
   //  Returns true if the current face of the coin is heads.
   //-----------------------------------------------------------------
   public boolean isHeads()
   {
      return (face == HEADS);
   }

   //-----------------------------------------------------------------
   //  Returns the current face of the coin as a string.
   //-----------------------------------------------------------------
   public String toString()
   {
      String faceName;

      if (face == HEADS)
         faceName = "Heads";
      else
         faceName = "Tails";

      return faceName;
   }
}

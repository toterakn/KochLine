package edu.cofc.csci221.ui;

/***
 * 
 * @author Kristina Totera
 * Assignment 9 - Kochline class, inherits from Line class
 * Used to create fractals
 * @since 18 Nov 2014
 * Due 1 Dec 2014
 * 
 */


public class KochLine extends Line{
	private Point p1;
	private Point p2;
	private Point p3;
	private Point p4;
	private Point p5;
	
	/**
	 * 2 argument public constructor
	 * @param start, starting point for line
	 * @param end, ending point for line
	 */
	public KochLine (Point start, Point end){
		super(start, end);
		p1 = getStart();
		p5 = getEnd();
	}
	/**
	 * Precondition: None
	 * Creates Koch Line A with p1 and p2
	 * Postcondition: Line A is returned
	 * @return Koch Line A
	 */
	public KochLine getLineA(){
		return new KochLine(p1, p2);
	}
	
	/**
	 * Precondition: None
	 * Creates Koch Line B with p2 and p3
	 * Postcondition: Line B is returned
	 * @return Koch Line B
	 */
	public KochLine getLineB(){
		return new KochLine(p2, p3);
	}
	
	/**
	 * Precondition: None
	 * Creates Koch Line C with p3 and p4
	 * Postcondition: Line C is returned
	 * @return Koch Line C
	 */
	public KochLine getLineC(){
		return new KochLine(p3, p4);
	}
	
	/**
	 * Precondition: None
	 * Creates Koch Line D with p4 and p5
	 * Postcondition: Line D is returned
	 * @return Koch Line D
	 */
	public KochLine getLineD(){
		return new KochLine(p4, p5);
	}
	/**
	 * Precondition: None
	 * Postcondition: p2, p3, p4 (x, y) coordinate values computed
	 * @return null
	 */
	public void computeFractal(){
		int X51 = p5.getX() - p1.getX();
		int Y51 = p5.getY() - p1.getY();
		
		int x2 = p1.getX() + X51 / 3;
		int y2 = p1.getY() + Y51 / 3;
		
		int x3 = (int) ((p1.getX() + p5.getX()) / 2 + (Math.sqrt(3) * (p1.getY() - p5.getY())) /6);
		int y3 = (int) ((p1.getY() + p5.getY()) /2 + (Math.sqrt(3) * (p5.getX() - p1.getX())) /6);
		
		int x4 = p1.getX() + (2 * X51) / 3;
		int y4 = p1.getY() + (2 * Y51) / 3;
		
		p2 = new Point(x2, y2);
		p3 = new Point(x3, y3);
		p4 = new Point(x4, y4);
		
	}
	/**
	 * Precondition: None
	 * Evaluates if all the kochline segments are valid, uses inherited isValid method
	 * Postcondition: Boolean returned, true if kochline is valid, false otherwise
	 * @return boolean
	 */
	public boolean isKochLineValid(){
		
		if (getLineA().isValid() && getLineB().isValid() && getLineC().isValid() && getLineD().isValid()){
			return true;
		}else{
			return false;
		}
	}
	
	
}

package com.example.killthemall_training;

import java.util.ArrayList;
import java.util.List;

import android.content.Context;
import android.graphics.Bitmap;
import android.graphics.BitmapFactory;
import android.graphics.Canvas;
import android.graphics.Color;
import android.view.MotionEvent;
import android.view.SurfaceHolder;
import android.view.SurfaceHolder.Callback;
import android.view.SurfaceView;

public class GameView extends SurfaceView {

	private Bitmap bmp;
	private SurfaceHolder holder;
	private GameLoopThread gameLoopThread;
	private int qt =5;
	private List<Sprite> sprites1 = new ArrayList<Sprite>();
	private List<Sprite> sprites2 = new ArrayList<Sprite>();
	private List<Sprite> sprites3 = new ArrayList<Sprite>();
	private List<Sprite> sprites4 = new ArrayList<Sprite>();
	private List<Sprite> sprites5 = new ArrayList<Sprite>();
	private List<Sprite> sprites6 = new ArrayList<Sprite>();
	private List<Sprite> sprites7 = new ArrayList<Sprite>();
	private List<Sprite> sprites8 = new ArrayList<Sprite>();
	private List<Sprite> sprites9 = new ArrayList<Sprite>();
	private List<Sprite> sprites10 = new ArrayList<Sprite>();
	private List<Sprite> sprites11 = new ArrayList<Sprite>();
	private List<Sprite> sprites12 = new ArrayList<Sprite>();
	public String word;
	
	private long lastClick;
	private Bitmap bmpBlood;
	private List<TempSprite> temps = new ArrayList<TempSprite>();

       	public GameView(Context context) {
		super(context);
		gameLoopThread = new GameLoopThread(this);
		holder = getHolder();
	    holder.addCallback(new Callback(){

			@Override
			public void surfaceChanged(SurfaceHolder arg0, int arg1, int arg2,int arg3) {}

			@Override
			public void surfaceCreated(SurfaceHolder arg0) {
				createSprites(qt);
				gameLoopThread.setRunning(true);
                gameLoopThread.start();
			}

			@Override
			public void surfaceDestroyed(SurfaceHolder arg0) {}
	    	
	    }); 
	    bmpBlood = BitmapFactory.decodeResource(getResources(), R.drawable.blood1);
	}
       	
       	public void setSprites1(){
       		add1();
       	}
       	public void setSprites2(){
       		add2();
       	}
       	public void setSprites3(){
       		add3();
       	}
       	public void setSprites4(){
       		add4();
       	}
       	public void setSprites5(){
       		add5();
       	}
       	public void setSprites6(){
       		add6();
       	}
       	public void setSprites7(){
       		add7();
       	}
       	public void setSprites8(){
       		add8();
       	}
       	public void setSprites9(){
       		add9();
       	}
       	public void setSprites10(){
       		add10();
       	}
       	public void setSprites11(){
       		add11();
       	}
       	public void setSprites12(){
       		add12();
       	}
       	
       	public void add1(){
       		sprites1.add(createSprite(R.drawable.bad1));
       	}
       	public void add2(){
       		sprites2.add(createSprite(R.drawable.bad2));
       	}
       	public void add3(){
       		sprites3.add(createSprite(R.drawable.bad3));
       	}
       	public void add4(){
       		sprites4.add(createSprite(R.drawable.bad4));
       	}
       	public void add5(){
       		sprites5.add(createSprite(R.drawable.bad5));
       	}
       	public void add6(){
       		sprites6.add(createSprite(R.drawable.bad6));
       	}
       	public void add7(){
       		sprites7.add(createSprite(R.drawable.good1));
       	}
       	public void add8(){
       		sprites8.add(createSprite(R.drawable.good2));
       	}
       	public void add9(){
       		sprites9.add(createSprite(R.drawable.good3));
       	}
       	public void add10(){
       		sprites10.add(createSprite(R.drawable.good4));
       	}
       	public void add11(){
       		sprites11.add(createSprite(R.drawable.good5));
       	}
       	public void add12(){
       		sprites12.add(createSprite(R.drawable.good6));
       	}
       	public Sprite get1(int i){
       		return sprites1.get(i);
       	}
       	public Sprite getSprites1(int i){       		
       		return get1(i);
       	}
       	public Sprite get2(int i){
       		return sprites2.get(i);
       	}
       	public Sprite getSprites2(int i){       		
       		return get2(i);
       	}
       	public Sprite get3(int i){
       		return sprites3.get(i);
       	}
       	public Sprite getSprites3(int i){       		
       		return get3(i);
       	}
       	public Sprite get4(int i){
       		return sprites4.get(i);
       	}
       	public Sprite getSprites4(int i){       		
       		return get4(i);
       	}
       	public Sprite get5(int i){
       		return sprites5.get(i);
       	}
       	public Sprite getSprites5(int i){       		
       		return get5(i);
       	}
       	public Sprite get6(int i){
       		return sprites6.get(i);
       	}
       	public Sprite getSprites6(int i){       		
       		return get6(i);
       	}
       	public Sprite get7(int i){
       		return sprites7.get(i);
       	}
       	public Sprite getSprites7(int i){       		
       		return get7(i);
       	}
       	public Sprite get8(int i){
       		return sprites8.get(i);
       	}
       	public Sprite getSprites8(int i){       		
       		return get8(i);
       	}
       	public Sprite get9(int i){
       		return sprites9.get(i);
       	}
       	public Sprite getSprites9(int i){       		
       		return get9(i);
       	}
       	public Sprite get10(int i){
       		return sprites10.get(i);
       	}
       	public Sprite getSprites10(int i){       		
       		return get10(i);
       	}
       	public Sprite get11(int i){
       		return sprites11.get(i);
       	}
       	public Sprite getSprites11(int i){       		
       		return get11(i);
       	}
       	public Sprite get12(int i){
       		return sprites12.get(i);
       	}
       	public Sprite getSprites12(int i){       		
       		return get12(i);
       	}
       	

       	private void createSprites(int qt) {
       		
       		for (int i=1; i<=qt; i++){
       			for (int j=1; j<=12;j++){
       			
       		   	switch(j){
       			
       		   	case 1:
       				setSprites1();
       				break;
       			case 2:
       				setSprites2();
       				break;
       			case 3:
       				setSprites3();
       				break;
       			case 4:
       				setSprites4();
       				break;
       			case 5:
       				setSprites5();
       				break;
       			case 6:
       				setSprites6();
       				break;
       			case 7:
       				setSprites7();
       				break;
       			case 8:
       				setSprites8();
       				break;
       			case 9:
       				setSprites9();
       				break;
       			case 10:
       				setSprites10();
       				break;
       			case 11:
       				setSprites11();
       				break;
       			case 12:
       				setSprites12();
       				break;
       		   	}
       			}
            }
            }

       	
       	private Sprite createSprite(int resouce) {  
            Bitmap bmp = BitmapFactory.decodeResource(getResources(), resouce);  
            return new Sprite(this,bmp);  
       	}  



	
       	protected void onDraw(Canvas canvas) {
            canvas.drawColor(Color.BLACK);
            for (int i = temps.size() - 1; i >= 0; i--) {
                temps.get(i).onDraw(canvas);
            }
            for (Sprite sprite : sprites1) {  
                sprite.onDraw(canvas);  
            }
            for (Sprite sprite : sprites2) {  
                sprite.onDraw(canvas);  
            } 
            for (Sprite sprite : sprites3) {  
                sprite.onDraw(canvas);  
            } 
            for (Sprite sprite : sprites4) {  
                sprite.onDraw(canvas);  
            } 
            for (Sprite sprite : sprites5) {  
                sprite.onDraw(canvas);  
            } 
            for (Sprite sprite : sprites6) {  
                sprite.onDraw(canvas);  
            } 
            for (Sprite sprite : sprites7) {  
                sprite.onDraw(canvas);  
            } 
            for (Sprite sprite : sprites8) {  
                sprite.onDraw(canvas);  
            } 
            for (Sprite sprite : sprites9) {  
                sprite.onDraw(canvas);  
            } 
            for (Sprite sprite : sprites10) {  
                sprite.onDraw(canvas);  
            } 
            for (Sprite sprite : sprites11) {  
                sprite.onDraw(canvas);  
            } 
            for (Sprite sprite : sprites12) {  
                sprite.onDraw(canvas);  
            } 
       	}

       	@Override  
        public boolean onTouchEvent(MotionEvent event) {  
       		if (System.currentTimeMillis() - lastClick > 300) {  
                lastClick = System.currentTimeMillis(); 
       		synchronized (getHolder()) { 
       		  float x=event.getX();
       		  float y=event.getY();
              for (int i = sprites1.size()-1; i >= 0; i--) {  
                     Sprite sprite = getSprites1(i);  
                     if (sprite.isCollition(x,y)) {  
                            sprites1.remove(sprite); 
                        	temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                            setSprites12();
                            setSprites12();
                            setSprites12();
                            break;
                     }  
              }
              for (int i = sprites2.size()-1; i >= 0; i--) {  
                  Sprite sprite = getSprites2(i);  
                  if (sprite.isCollition(x,y)) {  
                         sprites2.remove(sprite); 
                     	temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                     	setSprites11();
                     	setSprites11();
                     	setSprites11();
                         break;
                  }  
           
              }  
              for (int i = sprites3.size()-1; i >= 0; i--) {  
            	  Sprite sprite = getSprites3(i);  
            	  if (sprite.isCollition(x,y)) {  
                      sprites3.remove(sprite); 
                  		temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                  		setSprites10();
                  		setSprites10();
                  		setSprites10();
                  		break;
            	  }  
              }  
              for (int i = sprites4.size()-1; i >= 0; i--) {  
            	  Sprite sprite = getSprites4(i);  
            	  if (sprite.isCollition(x,y)) {  
            		  sprites4.remove(sprite); 
            		  temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                      setSprites9();
                      setSprites9();
                      setSprites9();
                      break;
            	  }	  
              }  
              for (int i = sprites5.size()-1; i >= 0; i--) {  
            	  Sprite sprite = getSprites5(i);  
            	  if (sprite.isCollition(x,y)) {  
            		  sprites5.remove(sprite); 
            		  temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                      setSprites8();
                      setSprites8();
                      setSprites8();
            		  break;
            	  }  
              }
              for (int i = sprites6.size()-1; i >= 0; i--) {  
            	  Sprite sprite = getSprites6(i);  
            	  if (sprite.isCollition(x,y)) {  
            		  sprites6.remove(sprite); 
            		  temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                      setSprites7();
                      setSprites7();
                      setSprites7();
            		  break;
            	  }  
              }
              for (int i = sprites7.size()-1; i >= 0; i--) {  
            	  Sprite sprite = getSprites7(i);  
            	  if (sprite.isCollition(x,y)) {  
            		  sprites7.remove(sprite); 
            		  temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                      setSprites6();
                      setSprites6();
                      setSprites6();
            		  break;
            	  }  
              }
              for (int i = sprites8.size()-1; i >= 0; i--) {  
            	  Sprite sprite = getSprites8(i);  
            	  if (sprite.isCollition(x,y)) {  
            		  sprites8.remove(sprite); 
            		  temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                      setSprites5();
                      setSprites5();
                      setSprites5();
            		  break;
            	  }  
              }
              for (int i = sprites9.size()-1; i >= 0; i--) {  
            	  Sprite sprite = getSprites9(i);  
            	  if (sprite.isCollition(x,y)) {  
            		  sprites9.remove(sprite); 
            		  temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                      setSprites4();
                      setSprites4();
                      setSprites4();
            		  break;
            	  }  
              }
              for (int i = sprites10.size()-1; i >= 0; i--) {  
            	  Sprite sprite = getSprites10(i);  
            	  if (sprite.isCollition(x,y)) {  
            		  sprites10.remove(sprite); 
            		  temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                      setSprites3();
                      setSprites3();
                      setSprites3();
            		  break;
            	  }  
              }
              for (int i = sprites11.size()-1; i >= 0; i--) {  
            	  Sprite sprite = getSprites11(i);  
            	  if (sprite.isCollition(x,y)) {  
            		  sprites11.remove(sprite); 
            		  temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                      setSprites2();
                      setSprites2();
                      setSprites2();
            		  break;
            	  }  
              }
              for (int i = sprites12.size()-1; i >= 0; i--) {  
            	  Sprite sprite = getSprites12(i);  
            	  if (sprite.isCollition(x,y)) {  
            		  sprites12.remove(sprite); 
            		  temps.add(new TempSprite(temps, this, x, y, bmpBlood));
                      setSprites1();
                      setSprites1();
                      setSprites1();
            		  break;
            	  }  
              }
       		}
       		}
              return true;  
        } 
}

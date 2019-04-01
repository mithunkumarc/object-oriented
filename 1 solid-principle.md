solid principle :

          In object-oriented computer programming, SOLID is a mnemonic acronym for five design principles 
          intended to make software designs more understandable, flexible and maintainable.


single resposibiilty principle : A class should have only a single responsibility

          a class must be given single resposibility :
            eg : class for database connection
            eg : class for transaction

 
open closed principle : 

          open for extension  : 
                    inheritance (extend subclass), missing/enchanced feature can be added in subclass
          
          closed for modification : 
                    dont allow changes in existing class


          class Mouse:
          class WirelessMouse: (add bluetooth feature) 

	
liskov substitution principle : 
	
          Objects in a program should be replaceable with instances of their subtypes without altering 
          the correctness of that program.

          class DefaultMediaPlayer
            playAudio()

          class VlcPlayer extends DefaultMediaPlayer:
            playAudio()


        	Vlc can replace DefaultPlayer




interface segregation priciple :    "Many client-specific interfaces are better than one general-purpose interface."


            bad : 

            interface shareWhatsapp{

              public void shareWhatsApp();
            }	


            interface shareGmail{
              public void shareGmail();
            }	


            good : 

            interface sharing {
              public void shareWhatspp();
              public void shareGmail();
            }



 
dependency inversion principle : One should "depend upon abstractions, [not] concretions

                //bad
                class Zoo:
                  public void feed(Dog d):
                    d.eat()

                  public void feed(Cat c):
                    c.eat()


                //good : 
                
                interface Pet:
                  eat();


                class Dog implements Pet:
                  eat()

                class Cat implements Pet:
                  eat()



                class Zoo:
                  public void feed(Pet p):	
                    p.eat()


                p could be , Dog or Cat

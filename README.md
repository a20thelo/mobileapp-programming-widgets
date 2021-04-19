
# Rapport mobileapp-programming-widgets

**Appen widgets forkades och klonades från LenaSys github. En constraint layout fanns redan från början med i layout activity main xml. 
Den ersattes med en linear-layout eftersom det var ett krav att lägga till en egen layout. Widgetsen imageview, textview och button lades till. 
Det gjordes genom att skiva exempelvis <button> och lägga till alla attribut som föreslogs.  
Ett ID för button lades till i main activity (public class MainActivity) genom denna kod:**

```
    Button button;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button button = findViewById(R.id.button);
    }
}

```

**Det var svårt att förflytta mina widgets eftersom jag först önskade att en widget skulle ligga i en 
annan widget. Men jag fick då tips på en handledning att en constraint layout skulle passa bättre,
därför bytte jag tillbaka till en constraint layout från en linear layout.
En constraint layout kräver att elementen (widgets) som omfattas av layouten har constraint-attribut
annars blev det felmeddelanden i android studio. Attributen för mina widgets var snarlika varandra 
alla fick ett id. Exempel på attribut som man kan se på button:**
 ##app:layout_constraintBottom_toBottomOf="parent.

```
 <Button
        android:id="@+id/button"
        android:layout_width="105dp"
        android:layout_height="58dp"
        android:layout_marginBottom="16dp"
        android:text="Tryck här"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toRightOf="parent"
        app:layout_constraintRight_toLeftOf="parent" />
```

**Widgets kunde förflyttas genom att hålla in en blå cirkel och dra pilen från cirkeln till ett annat element.
För att undvika bias attribut var det smartast att göra på detta sätt då det annars får ett bias-värde. 
Biasvärden bör undivkas då det inte går att avgöra hur objekten framträder på andra enheter.**

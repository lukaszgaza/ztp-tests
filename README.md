# Testowanie aplikacji

### Testy jednostkowe
Jest to metoda weryfikacji poprawności działania programu poprzez testowanie jego pojedynczych elementów (np. metod). Najpopularniejszą biblioteką służącą do tworzenia testów jednostkowych w Javie jest [JUnit](https://junit.org/junit5/docs/current/user-guide/#writing-tests). W przypadku Pythona testy jednostkowe można tworzyć na przykład korzystając z [pytest](https://docs.pytest.org/en/7.1.x/).

Czasami ze jednostki które chcemy przetestować (np. klasy) mają swoję zależności (bazy danych, pliki na dysku twardym czy zewnętrzne API udostępniane przez REST). Ponieważ w testach jednostkowych chcemy przetestować tylko jednostki zależności znajdujące się poza tymi jednostkami nie powinny być testowane. W tym celu w testach używa się jednostek (stub lub mock) mających imitować rzeczywiste obiekty Z tematyką tworzenia obiektów stub i mock można zapoznać się [tutaj](https://www.samouczekprogramisty.pl/testy-jednostkowe-z-uzyciem-mock-i-stub/). W przypadku języka Java najpopularniejszą biblioteką służącą do tworzenia obiektów typu stub i mock w testach jest [mockito](https://www.baeldung.com/mockito-annotations). W przypadku Pythona w tym celu można skorzystać na przykład z [pytest-mock](https://pypi.org/project/pytest-mock/).

## Zadania
1. Zaimplementuj w Javie klasę posiadającą metodę statyczną służącą do sprawdzania czy podany rok jest rokiem przestępnym. Napisz testy jednostkowe sprawdzające poprawność implementacji
   * rozwiązanie (implementacja i testy) powinno znajdnować się w podkatalogu `java-unit`
   * projekt powinien być projektem maven lub gradle
   * w podkatalogu `java-unit` powinien znajdować się plik `README.md` opsiujący w jaki sposób należy skompilować i przetestować projekt

2. Zaimplementuj w Pythonie funkcję służącą do sprawdzania czy podany rok jest rokiem przestępnym. Napisz testy jednostkowe sprawdzające poprawność implementacji
    * rozwiązanie (implementacja i testy) powinno znajdnować się w podkatalogu `python-unit`
    * aplikacja powinna działać w środowisku wirtualnym (np. `venv`)
    * wraz z kodem w katalogu `python-unit` powinien znajdować się plik opisujący jakie zależności mają być zainstalowane w środowisku wirtualnym (np. `requirements.txt` dla `venv`)
    * w podkatalogu `python-unit` powinien znajdować się plik `README.md` opsiujący w jaki sposób należy stworzyć i aktywować środowisko wirtualne oraz w jaki sposób należy uruchomić testy

3. Zaimplementuj serwis `PersonCounterService` z poprzedniego laboratorium w Javie. Napisz testy jednostkowe testujące poprawność implementacji.
    * rozwiązanie (implementacja i testy) powinno znajdnować się w podkatalogu `java-mock`
    * projekt powinien być projektem maven lub gradle
    * ponieważ są to testy jednostkowe `PersonCounterService` nie powinien w testach komunikować się bezpośrednio z `CounterService` ale z jego mockiem/stubem
    * w podkatalogu `java-mock` powinien znajdować się plik `README.md` opsiujący w jaki sposób należy skompilować i przetestować projekt
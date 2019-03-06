Soneta.Sdk
Sdk stworzone przez firm� Soneta pozwalaj�ce automatycznie skonfigurowa� oraz uzupe�ni� projekty dodatk�w o niezb�dne elementy potrzebne do wsp�pracy z oprogramowaniem enova oraz triva.

Spos�b zaimplementowania/Example:
W celu zaimportowania Soneta.Sdk w projekcie importuj�cym w pliku nazwaprojektu.csproj w linii dotycz�cej projektu ustawiamy: <Project Sdk="Soneta.Sdk/numerWersji">.
Po zapisie zmian zostanie wykonana automatyczna konfiguracja projektu.

W przypadku gdy w solucji znajduj� si� wiele projekt�w, by unikn�� konieczno�ci zmian w ka�dym projekcie numeru wersji, istnieje mo�liwo�� stworzenia pliku nadrz�dnego 
global.json (poza projektami) o zawarto�ci:
 {
  "msbuild-sdks": {
    "Soneta.Sdk": "numerWersji"
  }
}
Dzi�ki temu w plikach .csproj wymagany b�dzie tylko wpis <Project Sdk="Soneta.Sdk"> bez konieczno�ci umieszczania numeru wersji.


For Contributors: 
1) Po poprawnym zbudowaniu Sdk ustawiamy si� w cmd na �cie�ce **\bin\Release
2) Wpisujemy komend� -> dotnet nuget push nazwaPaczki.nupkg -s C:\Users\...\.nuget\packages  (pushujemy do naszego lokalnego folderu z paczkami)
3) Dzi�ki powy�szym czynno�ciom nasze SDK b�dzie widoczne dla naszych nowo utworzonych projekt�w.
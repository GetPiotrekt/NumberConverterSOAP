## To repozytorium zawiera dokumentację również w języku polskim, która znajduje się poniżej.
Link: https://www.dataaccess.com/webservicesserver/NumberConversion.wso

# EN / SOAP – Number Conversion Service

This project implements a simple client–server application that converts numeric values into words or dollar amounts using the public Number Conversion SOAP web service from DataAccess.

# 🚀 Features

    •	Convert numbers to words: The server converts numeric values into their word representation.
    •	Convert numbers to dollars: The server converts numeric values into dollar amounts (e.g., 123 → “one hundred twenty-three dollars”).
    •	Custom Server–Client Communication: The client can send requests to the server via TCP.
    •	Request/Response Handling: Client sends a number, receives a formatted response.
    •	Error Handling: Detects invalid input or connection issues.

# 📋 Requirements

## Functional Requirements
    1.	Convert Number to Words
    
        •	Server must convert integer numbers to their word equivalents.
        •	Client must be able to request the conversion and display the response.

    2.	Convert Number to Dollars
    
        •	Server must convert integer numbers to dollar amounts in words.
        •	Client must be able to request the conversion and display the response.

    3.	Networking
    
        •	Server listens on a defined TCP port.
        •	Client connects to the server on the same port.

    4.	Error Reporting
    
        •	System must notify the user when input is invalid or the server is unreachable.

## Non-Functional Requirements
    1.	Reliability
    
        •	Server should handle invalid input gracefully.
        •	Application must not crash on errors or network issues.

    2.	Performance
    
        •	Conversion requests must be processed without noticeable delay.

    3.	Maintainability
    
        •	Methods like konwertujLiczbeNaSlowo() and konwertujLiczbeNaDolary() must be modular.
        •	Clear separation between client and server logic.

    4.	Portability
    
        •	Server and client must run on any system supporting Java and TCP/IP.

# 🧩 Architecture

The system follows a simple Client–Server architecture:
## Client <──TCP──> Server <──SOAP──> Number Conversion Service

## Server Responsibilities
    •	Accept client connections.
    •	Convert numbers to words (konwertujLiczbeNaSlowo(int number)).
    •	Convert numbers to dollars (konwertujLiczbeNaDolary(int number)).
    •	Return formatted results to the client.

## Client Responsibilities
    •	Connect to the server via TCP.
    •	Send numbers for conversion using:
    •	zadajZapytanieKonwersjiLiczbyNaSlowo(int number)
    •	zadajZapytanieKonwersjiLiczbyNaDolary(int number)
    •	Display the server’s response.

# 🔧 Technologies
    •	Java: main language for server and client.
    •	TCP/IP Sockets: client–server communication.
    •	SOAP (Simple Object Access Protocol): communication with the web service.
    •	Number Conversion SOAP Web Service (DataAccess): converts numbers to words/dollars.

**────────────────────────**

# PL / SOAP – Serwis Konwersji Liczb

Projekt implementuje prostą aplikację klient–serwer w Javie, która konwertuje liczby całkowite na słowa lub kwoty dolarów przy użyciu publicznego SOAP web service Number Conversion od DataAccess.

# 🚀 Funkcje
    •	Konwersja liczb na słowa: Serwer konwertuje liczby całkowite na ich słowną reprezentację.
    •	Konwersja liczb na dolary: Serwer konwertuje liczby całkowite na kwoty w dolarach (np. 123 → „one hundred twenty-three dollars”).
    •	Komunikacja klient–serwer: Klient może wysyłać żądania do serwera przez TCP.
    •	Obsługa żądań i odpowiedzi: Klient wysyła liczbę i otrzymuje sformatowaną odpowiedź.
    •	Obsługa błędów: System wykrywa niepoprawne dane wejściowe lub problemy z połączeniem.

# 📋 Wymagania

## Wymagania funkcjonalne
    1.	Konwersja liczby na słowo
    
        •	Serwer musi konwertować liczby całkowite na ich zapis słowny.
        •	Klient musi móc wysłać żądanie konwersji i wyświetlić odpowiedź.

    2.	Konwersja liczby na dolary
    
        •	Serwer musi konwertować liczby całkowite na kwoty dolarów w słowach.
        •	Klient musi móc wysłać żądanie konwersji i wyświetlić odpowiedź.

    3.	Komunikacja sieciowa
    
        •	Serwer nasłuchuje na określonym porcie TCP.
        •	Klient łączy się z serwerem na tym samym porcie.

    4.	Obsługa błędów
    
        •	System musi powiadamiać użytkownika, gdy dane wejściowe są niepoprawne lub serwer jest niedostępny.

## Wymagania niefunkcjonalne
    1.	Niezawodność
    
        •	Serwer powinien prawidłowo obsługiwać niepoprawne dane wejściowe.
        •	Aplikacja nie powinna ulegać awarii w przypadku błędów lub problemów sieciowych.

    2.	Wydajność
    
        •	Żądania konwersji muszą być przetwarzane bez zauważalnego opóźnienia.

    3.	Utrzymanie
    
        •	Metody takie jak konwertujLiczbeNaSlowo() i konwertujLiczbeNaDolary() muszą być modułowe.
        •	Czysty podział logiki między klientem a serwerem.

    4.	Przenośność
    
        •	Serwer i klient muszą działać na każdym systemie obsługującym Javę i TCP/IP.

# 🧩 Architecture

System oparty jest o prostą architekturę klient–serwer:
## Klient <──TCP──> Serwer <──SOAP──> Serwis Konwersji Liczb

## Obowiązki serwera
    •	Obsługa połączeń od klientów.
    •	Konwersja liczb na słowa (konwertujLiczbeNaSlowo(int liczba)).
    •	Konwersja liczb na dolary (konwertujLiczbeNaDolary(int liczba)).
    •	Zwracanie sformatowanych wyników klientowi.

## Obowiązki klienta
    •	Łączenie się z serwerem przez TCP.
    •	Wysyłanie liczb do konwersji za pomocą:
    •	zadajZapytanieKonwersjiLiczbyNaSlowo(int liczba)
    •	zadajZapytanieKonwersjiLiczbyNaDolary(int liczba)
    •	Wyświetlanie odpowiedzi serwera.

# 🔧 Technologie
    •	Java: główny język dla serwera i klienta.
    •	TCP/IP Sockets: komunikacja klient–serwer.
    •	SOAP (Simple Object Access Protocol): komunikacja z serwisem webowym.
    •	Publiczny serwis Number Conversion (DataAccess): konwersja liczb na słowa i dolary.
    •	BufferedReader / BufferedWriter: efektywna obsługa żądań i odpowiedzi.

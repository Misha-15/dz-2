#include <iostream>
#include <string>
using namespace std;

//класс электрочайник
class ElectricKettle {
private:
    string brand;
    int volume;  //объем в мл
    int power;   //мощность в ваттах
    string color;
    bool isOn;

public:
    //конструктор
    ElectricKettle(string b, int v, int p, string c, bool state)
        : brand(b), volume(v), power(p), color(c), isOn(state) {}

    //геттеры и сеттеры
    string getBrand() const { return brand; }
    void setBrand(const string& b) { brand = b; }

    int getVolume() const { return volume; }
    void setVolume(int v) { volume = v; }

    int getPower() const { return power; }
    void setPower(int p) { power = p; }

    string getColor() const { return color; }
    void setColor(const string& c) { color = c; }

    bool getIsOn() const { return isOn; }
    void setIsOn(bool state) { isOn = state; }

    //методы
    void turnOn() {
        isOn = true;
        cout << "чайник включен\n";
    }

    void turnOff() {
        isOn = false;
        cout << "чайник выключен\n";
    }

    void boilWater() const {
        if (isOn) {
            cout << "вода кипятится\n";
        }
        else {
            cout << "сначала включите чайник\n";
        }
    }

    void displayInfo() const {
        cout << "чайник " << brand << " (" << color << "), объем: " << volume
            << " мл, мощность: " << power << " Вт.\n";
    }
};

// класс книга
class Book {
private:
    string title;
    string author;
    int pages;
    string genre;
    bool isOpen;

public:
    //конструктор
    Book(string t, string a, int p, string g, bool open)
        : title(t), author(a), pages(p), genre(g), isOpen(open) {}

    //геттеры и сеттеры
    string getTitle() const { return title; }
    void setTitle(const string& t) { title = t; }

    string getAuthor() const { return author; }
    void setAuthor(const string& a) { author = a; }

    int getPages() const { return pages; }
    void setPages(int p) { pages = p; }

    string getGenre() const { return genre; }
    void setGenre(const string& g) { genre = g; }

    bool getIsOpen() const { return isOpen; }
    void setIsOpen(bool open) { isOpen = open; }

    //методы
    void openBook() {
        isOpen = true;
        cout << "книга \"" << title << "\" открыта.\n";
    }

    void closeBook() {
        isOpen = false;
        cout << "книга \"" << title << "\" закрыта.\n";
    }

    void readPage() const {
        if (isOpen) {
            cout << "читаем страницу книги \"" << title << "\".\n";
        }
        else {
            cout << "сначала откройте книгу\n";
        }
    }

    void displayInfo() const {
        cout << "книга \"" << title << "\", автор: " << author
            << ", жанр: " << genre << ", страниц: " << pages << ".\n";
    }
};

//класс телефон
class Phone {
private:
    string brand;
    string model;
    int batteryLevel;
    string color;
    bool isOn;

public:
    //конструктор
    Phone(string b, string m, int bl, string c, bool state)
        : brand(b), model(m), batteryLevel(bl), color(c), isOn(state) {}

    //геттеры и сеттеры
    string getBrand() const { return brand; }
    void setBrand(const string& b) { brand = b; }

    string getModel() const { return model; }
    void setModel(const string& m) { model = m; }

    int getBatteryLevel() const { return batteryLevel; }
    void setBatteryLevel(int bl) { batteryLevel = bl; }

    string getColor() const { return color; }
    void setColor(const string& c) { color = c; }

    bool getIsOn() const { return isOn; }
    void setIsOn(bool state) { isOn = state; }

    //методы
    void turnOn() {
        isOn = true;
        cout << "телефон включен\n";
    }

    void turnOff() {
        isOn = false;
        cout << "телефон выключен\n";
    }

    void makeCall(const string& number) const {
        if (isOn) {
            cout << "звоним на номер " << number << "...\n";
        }
        else {
            cout << "сначала включите телефон\n";
        }
    }

    void chargePhone() {
        batteryLevel = 100;
        cout << "телефон полностью заряжен\n";
    }

    void displayInfo() const {
        cout << "телефон " << brand << " " << model << " (" << color
            << "), заряд: " << batteryLevel << "%.\n";
    }
};

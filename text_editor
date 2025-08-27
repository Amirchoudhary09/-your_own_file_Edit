#include <bits/stdc++.h>
using namespace std;

class editer {
public:
    vector<string> ans;
    string renderdocument;

    // insert text
    void text(string value) {
        ans.push_back(value);
    }

    // insert image 
    void image(string ima) {
        ans.push_back(ima);
    }

    // render document
    void render() {
        string result;
        for (auto element : ans) {
            // check if it's an image by extension
            if (element.size() > 4 &&
                (element.substr(element.size() - 4) == ".jpg" ||
                 element.substr(element.size() - 4) == ".png")) {
                result += "[image: " + element + "]\n";
            } else {
                result += element + "\n";
            }
        }
        renderdocument = result;
    }

    // save document to file
    void save() {
        ofstream file("document.txt"); 
        if (file.is_open()) {
            file << renderdocument;
            file.close();
            cout << "Your file is saved successfully as document.txt" << endl;
        } else {
            cout << "Error: Could not open file for writing." << endl;
        }
    }
};

int main() {
    editer a1;

    // add some text and images
    a1.text("My self Amir Choudhary");
    a1.text("I am learning C++");
    a1.image("profile.png");
    a1.image("logo.jpg");
    a1.text("This is my editor application");
    a1.image("profile.png");
    a1.image("logo.jpg");
    a1.text("It can store multiple lines of text");

    // process + save
    a1.render();
    a1.save();

    // print on console too
    cout << "\n--- Rendered Document ---\n";
    cout << a1.renderdocument << endl;

    return 0;
}

import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        debugShowCheckedModeBanner: false,
        home: Scaffold(
          appBar: AppBar(
            title: Center(child: Text("Login")),
            backgroundColor: Colors.red[900],
          ),
          body: Container(
            decoration: BoxDecoration(
                gradient: RadialGradient(colors: [
              Colors.white70,
              Colors.blueGrey,
            ])),
            child: Center(
              child: Column(
                mainAxisAlignment: MainAxisAlignment.spaceAround,
                children: [
                  Container(
                    width: 200,
                    child: TextFormField(
                      decoration: const InputDecoration(
                          border: UnderlineInputBorder(),
                          labelText: 'Enter your username'),
                    ),
                  ),
                  Container(
                    width: 200,
                    child: TextFormField(
                      decoration: const InputDecoration(
                          border: UnderlineInputBorder(),
                          labelText: 'Enter your Password'),
                    ),
                  ),
                  Container(
                    width: 200,
                    child: ElevatedButton(
                        style: ElevatedButton.styleFrom(
                          primary: Colors.red[900], // background
                          //onPrimary: Colors.yellow, // foreground
                        ),
                        onPressed: () {},
                        child: Text("Login")),
                  )
                  //ElevatedButton(onPressed: () {}, child: Text("Login"))
                ],
              ),
            ),
          ),
        ));
  }
}

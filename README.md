import 'package:flutter/material.dart';
import 'import 'package:google_fonts/google_fonts.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
        useMaterial3: true,
      ),
      home: const MyHomePage(title: 'Flutter Demo Home Page'),
    );
  }
}

class MyHomePage extends StatefulWidget {
  const MyHomePage({super.key, required this.title});

  final String title;

  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  double height = 56.0;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        title: Text(widget.title),
      ),
      body: Center(
        child: Container(
          decoration: const BoxDecoration(
            color: Color(0xFFFFFFFF),
          ),
          child: Container(
            padding: const EdgeInsets.fromLTRB(26, 260, 26, 230),
            child: Column(
              mainAxisAlignment: MainAxisAlignment.start,
              crossAxisAlignment: CrossAxisAlignment.center,
              children: [
                Container(
                  margin: const EdgeInsets.fromLTRB(0, 0, 97.2, 41),
                  child: RichText(
                    text: TextSpan(
                      style: GoogleFonts.roboto(
                        fontWeight: FontWeight.w500,
                        fontSize: 40,
                        color: const Color(0xFF505050),
                      ),
                      children: [
                        TextSpan(
                          text: 'LOGIN',
                          style: GoogleFonts.roboto(
                            fontWeight: FontWeight.w500,
                            fontSize: 30,
                            height: 1.3,
                          ),
                        ),
                        TextSpan(
                          text: '/',
                          style: GoogleFonts.roboto(
                            fontWeight: FontWeight.w500,
                            fontSize: 35,
                            height: 1.3,
                          ),
                        ),
                        TextSpan(
                          text: ' ',
                        ),
                        TextSpan(
                          text: 'Sign Up',
                          style: GoogleFonts.roboto(
                            fontWeight: FontWeight.w400,
                            fontSize: 20,
                            height: 1.3,
                            color: const Color(0xFF7795FF),
                          ),
                        ),
                      ],
                    ),
                  ),
                ),
                Container(
                  margin: const EdgeInsets.fromLTRB(0, 0, 0, 56),
                  child: Column(
                    mainAxisAlignment: MainAxisAlignment.start,
                    crossAxisAlignment: CrossAxisAlignment.start,
                    children: [
                      Container(
                        margin: const EdgeInsets.fromLTRB(0, 0, 0, 6),
                        child: const Align(
                          alignment: Alignment.topLeft,
                          child: Text(
                            'Email:',
                            style: TextStyle(
                              fontWeight: FontWeight.w400,
                              fontSize: 20,
                              color: Color(0xFF838383),
                            ),
                          ),
                        ),
                      ),
                      Container(
                        height: height,
                        child: TextField(
                          decoration: InputDecoration(
                            hintText: 'Enter your email',
                            hintStyle: const TextStyle(
                              fontWeight: FontWeight.w400,
                              fontSize: 20,
                              color: Color(0xFF838383),
                            ),
                            border: OutlineInputBorder(
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ),
                          style: const TextStyle(
                            fontWeight: FontWeight.w400,
                            fontSize: 20,
                            color: Color(0xFF505050),
                          ),
                        ),
                      ),
                      Container(
                        margin: const EdgeInsets.fromLTRB(0, 20, 0, 6),
                        child: const Text(
                          'Password:',
                          style: TextStyle(
                            fontWeight: FontWeight.w400,
                            fontSize: 20,
                            color: Color(0xFF838383),
                          ),
                        ),
                      ),
                      Container(
                        height: height,
                        child: TextField(
                          obscureText: true,
                          decoration: InputDecoration(
                            hintText: 'Enter your password',
                            hintStyle: const TextStyle(
                              fontWeight: FontWeight.w400,
                              fontSize: 20,
                              color: Color(0xFF838383),
                            ),
                            border: OutlineInputBorder(
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ),
                          style: const TextStyle(
                            fontWeight: FontWeight.w400,
                            fontSize: 20,
                            color: Color(0xFF505050),
                          ),
                        ),
                      ),
                      Container(
                        margin: const EdgeInsets.fromLTRB(0, 20, 0, 20),
                        child: ElevatedButton(
                          onPressed: () {
                            // Add your login functionality here
                          },
                          style: ElevatedButton.styleFrom(
                            primary: Theme.of(context).colorScheme.primary,
                            onPrimary: Colors.white,
                            elevation: 0,
                            shape: RoundedRectangleBorder(
                              borderRadius: BorderRadius.circular(10),
                            ),
                          ),
                          child: const Text('LOGIN'),
                        ),
                      ),
                    ],
                  ),
                ),
              ],
            ),
          ),
        ),
      ),
    );
  }
}

A Template C++ Library for loading shared objects easily.

Tested on Windows & Linux.

Example use:

```
typedef karma::io::Symbol<unsigned             > UnsignedFunction ; // An alias for a symbol that returns an unsigned integer.
typedef karma::io::Symbol<const char*, unsigned> CStringFunction  ; // An alias for a symbol that takes in a unsigned integer and returns a string.
typedef karma::io::Symbol<void, unsigned       > VoidFunction     ; // An alias for a symbol that takes in just an unsigned integer and returns void.

// The object loader itself.
karma::io::ObjectLoader loader ;

// The symbols to load.
UnsignedFunction function_one   = loader.symbol( "symbol_one"   ) ;
CStringFunction  function_two   = loader.symbol( "symbol_two"   ) ;
VoidFunction     function_three = loader.symbol( "symbol_three" ) ;

// Now you can call these symbols like functions.
unsigned    number = function_one  (    ) ;
const char* string = function_two  ( 1u ) ;
                     function_three( 5u ) ; // Void function so returns nothing!

```


# YAUD
Yet Another UI Description

This repo include the definition and runtime for YAUD. The runtime parses YAUD and glue to several GUI frameworks on different languages.

The mainstream runtime is Qt5 (C++/Python) and others are under development.

## UI Component Type

  text (txt, t) for static text. Rendered as QLabel.
  input (in, i) for input box. Rendered as QLineEdit.
  single_select (ssel, s) for single select from multiple items. Rendered as QListWidget, QComboBox or QRadioBox Group
  multi_select (msel, m) for multiple select from multiple items. Rendered as QListWidget or QCheckBox Group
  check (chk, c) is an alias of multi_select (one item)
  button (btn, b) is for push button. Rendered as QPushButton
  vertical (v) is for vertical layout. Rendered as QWidget or QGroupBox with QVBoxLayout
  horizontal (h) is for horizontal layout. Rendered as QWidget or QGroupBox with QHBoxLayout
  form (f) is for form layout. Rendered as QWidget or QGroupBox with QFormLayout
  grid (g) is for grid layout. Rendered as QWidget or QGroupBox with QGridLayout
  
## YAUD Grammar

each item is a four-element array with:
  
  The first item, a string, as UI component type
  The second item, a string, as ID, should be unique
  The third item, a dictonary, as extra render properity. or a list, as component data, or not present.
  The fourth item, a list, as component data, or not present.
  
Special cases:
 
  A string is seen as an array with one element of this string
  A one element array is seen as text with value as the element

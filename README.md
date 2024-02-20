# Italics for Visual Studio

This is a Visual Studio extension that allows you to use italics in the text editor. In order to use this extension you will need to know the names of the [text classification types](https://docs.microsoft.com/en-us/dotnet/api/microsoft.visualstudio.text.classification.iclassificationtype?view=visualstudiosdk-2022) that you want to italicize.

## Usage

- Install the VSIX and open Visual Studio 2022
- Open Tools -> Options -> Italics -> General
- In the "Classification types" field enter the text classification types you want to italicize
    - Input as list
        - Click the "..." button on the right side of the text field 
        - List the name of each classification type, one per line
    - Input as comma-separated values
        - List all the identifiers on one line
        - Do not enclose the identifiers in quotes
        - Spaces between identifiers are ok
- Click OK
- Open a file and you should see italics!

## Example Settings Value

### As line-separated values

```
comment
CSS Comment
CSS Keyword
HTML Comment
keyword
keyword - control
preprocessor keyword
preprocessor text
regex - comment
XML Doc Comment
xml doc comment - attribute name
xml doc comment - attribute quotes
xml doc comment - attribute value
xml doc comment - cdata section
xml doc comment - comment
xml doc comment - delimiter
xml doc comment - entity reference
xml doc comment - name
xml doc comment - processing instruction
xml doc comment - text
XML Doc Tag
```

### As comma-separated values

```
comment,CSS Comment,CSS Keyword,HTML Comment,keyword,keyword - control,preprocessor keyword,preprocessor text,regex - comment,XML Doc Comment,xml doc comment - attribute name,xml doc comment - attribute quotes,xml doc comment - attribute value,xml doc comment - cdata section,xml doc comment - comment,xml doc comment - delimiter,xml doc comment - entity reference,xml doc comment - name,xml doc comment - processing instruction,xml doc comment - text,XML Doc Tag
```

## Credit

In order to create this extension I cribbed extensively from [Better Comments](https://github.com/omsharp/BetterComments) by omsharp.

## Other Classification Types

This is a list of classification types I got by inspecting `IClassificationFormatMapService.CurrentPriorityOrder` in the debugger on my system. I do not guarantee its accuracy or completeness.

```
bidirectional text control character,
brace matching,
C/C++ User Keywords,
class name,
comment,
constant name,
cppClassTemplate,
cppControlKeyword,
cppEnumerator,
cppEvent,
cppFunction,
cppFunctionTemplate,
cppGenericType,
cppGlobalVariable,
CppInactiveCodeClassification,
cppLabel,
cppLocalVariable,
cppMacro,
cppMemberField,
cppMemberFunction,
cppMemberOperator,
cppNamespace,
cppNewDelete,
cppOperator,
cppParameter,
cppProperty,
cppRefType,
CppSolidColorClassification,
cppStaticMemberField,
cppStaticMemberFunction,
cppStringDelimiterCharacter,
cppStringEscapeCharacter,
cppType,
cppUserDefinedLiteralNumber,
cppUserDefinedLiteralRaw,
cppUserDefinedLiteralString,
cppValueType,
CSS Comment,
CSS Keyword,
CSS Property Name,
CSS Property Value,
CSS Selector,
CSS String Value,
currentParam,
delegate name,
enum member name,
enum name,
event name,
excluded code,
extension method name,
field name,
formal language,
FSharp.DisposableLocalValue,
FSharp.DisposableTopLevelValue,
FSharp.DisposableType,
FSharp.Function,
FSharp.MutableVar,
FSharp.Printf,
HighContrastSelection,
HTML Attribute Name,
HTML Attribute Value,
HTML Comment,
HTML Element Name,
HTML Entity,
HTML Operator,
HTML Server-Side Script,
HTML Tag Delimiter,
HtmlClientTemplateSeparator,
HtmlClientTemplateTag,
HtmlClientTemplateValue,
identifier,
Inline Rename Field Text,
IntellisenseTextBlockClassificationType,
Interactive Window Error Output,
interface name,
JSON Property Name,
JSON Unused Code,
keyword,
keyword - control,
label name,
LessCssKeyword,
LessCssMixinDeclaration,
LessCssMixinReference,
LessCssNamespaceReference,
LessCssVariableDeclaration,
LessCssVariableReference,
line number,
literal,
local name,
MarkerPlaceHolder,
markup attribute,
markup attribute value,
markup node,
method name,
module name,
namespace name,
natural language,
navigableSymbol,
number,
operator,
operator - overloaded,
parameter name,
preprocessor keyword,
preprocessor text,
property name,
punctuation,
quickinfo-bold,
RazorCode,
RazorComponentAttribute,
RazorComponentElement,
RazorDirective,
RazorDirectiveAttribute,
RazorTagHelperAttribute,
RazorTagHelperElement,
RazorTransition,
reassigned variable,
record class name,
record struct name,
regex - alternation,
regex - anchor,
regex - character class,
regex - comment,
regex - grouping,
regex - other escape,
regex - quantifier,
regex - self escaped character,
regex - text,
ScssMixinDeclaration,
ScssMixinReference,
ScssVariableDeclaration,
ScssVariableReference,
sighelp-documentation,
Stale Code,
static symbol,
string,
string - escape character,
string - verbatim,
struct name,
StructurePopupCode,
symbol definition,
symbol reference,
TestSummaryDefaultClassificationType,
TestSummaryDiagnosticClassificationType,
TestSummaryHeaderClassificationType,
TestSummaryLabelClassificationType,
TestSummaryNoSourceClassificationType,
TestSummaryStackClassificationType,
TextMate.Classifier,
type,
type parameter name,
unnecessary code,
UnnecessaryCodeDiagnostic,
url,
VBScript Comment,
VBScript Function Block Start,
VBScript Identifier,
VBScript Keyword,
VBScript Number,
VBScript Operator,
VBScript String,
WatchWindowEditClassificationType,
word wrap glyph,
XML Doc Comment,
xml doc comment - attribute name,
xml doc comment - attribute quotes,
xml doc comment - attribute value,
xml doc comment - cdata section,
xml doc comment - comment,
xml doc comment - delimiter,
xml doc comment - entity reference,
xml doc comment - name,
xml doc comment - processing instruction,
xml doc comment - text,
XML Doc Tag,
xml literal - attribute name,
xml literal - attribute quotes,
xml literal - attribute value,
xml literal - cdata section,
xml literal - comment,
xml literal - delimiter,
xml literal - embedded expression,
xml literal - entity reference,
xml literal - name,
xml literal - processing instruction,
xml literal - text
```

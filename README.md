## Getting Started

To get a copy of the project up and running on your local machine for development and testing purposes, follow these steps:

### Prerequisites
- **Gradle Version**: 8
- **Java Version**: Java 8
- **Code Formatting**: Ktlint
- **Code Smelling**: Detekt

# Code Convention Android

Every developer has his/her own preferences to write codes. However, to build well-designed products by working as a team, each developer must agree to write clean, readable and maintainable code.
Some of these conventions might take some time for you to get used to but they are not to be blindly followed; strive to understand these and ask when in doubt.

### General Best Practices

- Keep the code simple.
- Follow SOLID and Clean Code Principle.
- Don’t write code for future functionality based on your assumptions, write relevant code.
- Never Say Never to learn and use english!

### Formatting

- Break long lines of code. In android studio, after finish write a code please use option+cmd+L to auto format your code.
- Place inline comments above the code you write if needed.
- Don’t misspell / typo.
- Use an empty line between methods to make it easier to read.
- Use spaces after commas(,), colons(:), semicolons(;), and around curly brackets ({}).

### Naming

- Avoid abbreviations, except on some XML view ID below and product name from user.
- Use American English.
- Name variables, methods and classes to reveal intent.
- Use nouns for variable, interface, class, and object name.
- Use verbs for method & function.
- Never start naming with numbers, negative word, and **VERY**.
  e.g: - 1stPhase ❌, FirstPhase ✅
  - NotSuccessState ❌, FailedState ✅
  - VeryGood ❌, Excellent ✅,
- Use Plurals for list or multiple data e.g. products, cities, children
- Pay Attention to irregular Nouns!
  e.g:
-  Data is plural, **Never** use Datas!
-  Person is singular, People is Plural
- Avoid object types in names e.g **DO** users **DON’T** userArray, userList
- Treat acronyms as words in names, even if the acronym is the entire name e.g  **DO** `XmlHttpRequest` **DON’T**  `XMLHTTPRequest`


# Naming

### **XML ID Naming**

Use camelCase with the format : viewTypePurpose or purposeViewType (look at table below) to get the ID in Kotlin code.

| Component Name                                                                                | Prefix               | Example                   |
|-----------------------------------------------------------------------------------------------|----------------------|---------------------------|
| Button, ImageButton, MaterialButton                                                           | btn                  | btnLogin                  |
| TextView, MaterialTextView                                                                    | tv                   | tvName                    |
| EditText, TextInputEditText                                                                   | et                   | etEmail                   |
| ImageView, ShapeableImageView                                                                 | img                  | imgUser                   |
| Parent Layout (Relative, Constraint, Linear, Frame, Coordinator, Fragment, FragmentContainer) | (purpose)Container   | registerContainer         |
| Spinner                                                                                       | spn                  | spnCountry                |
| RadioGroup                                                                                    | rg                   | rgGender                  |
| RadioButton, MaterialRadioButton                                                              | rb                   | rbMale                    |
| CheckBox, MaterialCheckBox                                                                    | cb                   | cbTermsConditionAgreement |
| TextInputLayout                                                                               | til                  | tilPassword               |
| ErrorView                                                                                     | errv                 | errvProfile               |
| ProgressBar                                                                                   | pb                   | pbHome                    |
| Chip                                                                                          | chip                 | chipDay                   |
| ChipGroup                                                                                     | chipGroup            | chipGroupCategory         |
| View                                                                                          | view(Purpose)        | viewLeftTapArea           |
| RecyclerView                                                                                  | rv                   | rvMovie                   |
| ListView                                                                                      | lv                   | lvProduct                 |
| CardView, MaterialCardView                                                                    | cv                   | cvAddress                 |
| WebView                                                                                       | wv                   | wvPayment                 |
| TabLayout                                                                                     | tab                  | tabMain                   |
| ViewPager                                                                                     | vp                   | vpMain                    |
| NavigationDrawer                                                                              | (purpose)Drawer      | mainDrawer                |
| ScrollView                                                                                    | sv                   | svProfile                 |
| NestedScrollView                                                                              | nsv                  | nsvHome                   |
| AppBar                                                                                        | appBar               | appBarProfile             |
| EllipseView                                                                                   | ev                   | evAdditionalInfo          |
| Divider from View, Material Divider                                                           | (purpose)Divider     | userInfoDivider           |
| Toolbar, Material toolbar                                                                     | (purpose)Toolbar     | mainToolbar               |
| AutoCompleteTextView, MaterialAutoCompleteTextView                                            | actv                 | actvProduct               |
| Switch, SwitchMaterial                                                                        | (purpose)switch      | bluetoothSwitch           |
| FloatingActionButton                                                                          | fab                  | fabAddNote                |
| CalendarView                                                                                  | calendar             | calendarDoB               |
| SeekBar                                                                                       | sb                   | sbVolume                  |
| RatingBar                                                                                     | rating               | ratingFood                |
| SearchView                                                                                    | search               | searchProduct             |
| BottomNavigationBar                                                                           | bnv                  | bnvMain                   |
| NavigationView                                                                                | nav                  | navMain                   |
| Guideline                                                                                     | (purpose)Guideline   | rightAreaGuideline        |
| Barrier                                                                                       | (purpose)Barrier     | descriptionBarrier        |
| Group                                                                                         | (purpose)Group       | userInfoGroup             |
| MapView                                                                                       | map                  | mapDeliveryTracking       |
| SwipeRefreshLayout                                                                            | srl                  | srlHome                   |
| Bottom App Bar                                                                                | bottomAppBar         | bottomAppBarMain          |
| Custom View                                                                                   | custom(purpose)      | customErrorMessage        |
| From Dependencies                                                                             | (object name)Purpose | pinResetPassword          |

Another example:

tvLabelName = Text view with “**Name”** string

tvName = Text view with name value

### **Layout Naming**

Use snake case in naming the layout resources file.

| Item Name | Format | Example |
| --- | --- | --- |
| Activity Layout | activity_purpose | activity_login |
| Fragment Layout | fragment_purpose | fragment_register |
| Adapter Item Layout | item_purpose | item_product |
| Other Layout & Custom Layout | layout_purpose | layout_custom_player |
| Dialog Fragment | fragment_purpose_dialog | fragment_confirmation_dialog |
| Modal Bottom Sheet | fragment_purpose_bottom_sheet | fragment_filter_hotel_bottom_sheet |
| Standard Bottom Sheet | layout_purpose_bottom_sheet | layout_nearest_restaurant_bottom_sheet |

Use snake case for string resource file.

Messages :

| Type | Usage | Prefix | Example |
| --- | --- | --- | --- |
| Informative | Toast, Snackbar | message_ | message_insert_succeed |
| Error | ErrorView, Toast, Snackbar | error_ | error_email_invalid |

Strings :

| Type | Usage | Prefix | Example |
| --- | --- | --- | --- |
| Label Text | Mostly in TextView | label_ | label_address |
| Button or Actionable View | Button | action_ | action_login |
| Page Title | Toolbar | title_ | title_profile |
| Menu Item Text | Menu | menu_ | menu_logout |
| Hint | TextInputLayout, EditText | hint_ | hint_password |
| Dialog Title | Dialog | title_dialog_ | title_dialog_logout |
| Dialog Message | Dialog | message_dialog_ | message_dialog_logout |
| Array | ViewGroup | array_ | array_months |
| Sample | Use attribute tools:text In Various Text Component | sample_ | sample_name |

**Note :**

Important to add translatable=”false” to avoid translation in localizations **IF THERE IS MULTI-LANGUAGE FEATURE**. For Example :

```
<string name="message_input_your_answer" translatable="false">Mohon masukan jawaban kamu</string>
```

### **Resources and Assets Naming**

Uses a snake case in naming the resource file in drawable, color, assets, mipmap and menu.

| Type                              | Location        | Prefix    | Example             |
|-----------------------------------|-----------------|-----------|---------------------|
| background                        | drawable        | bg_       | bg_home             |
| button                            | drawable        | btn_      | btn_gradient        |
| selector drawable, selector color | drawable, color | selector_ | selector_login      |
| icon (use Vector instead)         | drawable        | ic_       | ic_user             |
| default image placeholder         | drawable        | default_  | default_banner      |
| animation (lottie svg)            | assets          | anim_     | anim_loading        |
| animation (native)                | anim            | anim_     | anim_rotate         |
| icon app                          | mipmap          | ic_       | ic_launcher         |
| menu                              | menu            | menu_     | menu_main           |
| divider                           | drawable        | divider_  | divider_dashed_line |
| Image (PNG, Jpeg, WebP)           | drawable        | img_      | img_logo            |

### **Colors Naming**

Uses a camel case in naming the colors in colors.xml.

| Type                                | Format                           | Example       |
|-------------------------------------|----------------------------------|---------------|
| color                               | color(ColorName)                 | colorNavyBlue |
| color with transparency and opacity | color(Color)Transparent(Opacity) |               |
| color(Color)Alpha(Opacity)          | colorBlackTransparent12          |               |
| colorBlackAlpha12                   |                                  |               |

Note:

Please follow the name color in Design Resources on Figma. UI/UX Team always provide it in every projects.

### **Dimension Naming**

Uses a snake_case in naming the dimension in file dimens.xml.

| Type                    | Unit | Format                     | File            | Example            |
|-------------------------|------|----------------------------|-----------------|--------------------|
| View (width and height) | dp   | dimen_[size][unit]         | dimens.xml      | dimen_16dp         |
| Margin Padding          | dp   | dimen_[size][unit]         | dimens.xml      | dimen_24dp         |
| Text Size               | sp   | text_size_[purpose]_[size] | dimens_text.xml | text_size_headline |

View, Margin, Padding in dimens.xml example :

```
<dimen name="dimen_0dp">0dp</dimen>
<dimen name="dimen_16dp">16dp</dimen>
<dimen name="dimen_12dp">12dp</dimen>
<dimen name="toolbar_icon_width">100dp</dimen>
<dimen name="toolbar_icon_height">20dp</dimen>
<dimen name="dimen_4dp">4dp</dimen>
<dimen name="dimen_10dp">10dp</dimen>
<dimen name="dimen_1dp">1dp</dimen>
<dimen name="dimen_24dp">24dp</dimen>
<dimen name="dimen_34dp">34dp</dimen>
<dimen name="dimen_5dp">5dp</dimen>
<dimen name="dimen_68dp">68dp</dimen>
```

Text Dimension in dimens_text.xml

```
<dimen name="text_size_headline">24sp</dimen>
<dimen name="text_size_title">20sp</dimen>
<dimen name="text_size_subhead">16sp</dimen>
<dimen name="text_size_title_toolbar">20dp</dimen>
<dimen name="text_size_subtitle_toolbar">16dp</dimen>
<dimen name="text_size_menu">16sp</dimen>
```

### **Styles File and Naming**

Use a combination of a snake case in naming the styles file and a Pascal case in its component naming.

### **Styles File**

| Type     | Format             | Example                            |
|----------|--------------------|------------------------------------|
| General  | styles             | styles.xml                         |
| Purposed | styles_purpose.xml | styles_button.xml, styles_text.xml |

### **Styles Naming**

| Type   | Format                                        | Example                                     |
|--------|-----------------------------------------------|---------------------------------------------|
| Parent | [ProjectName][Component], [SpecificComponent] | ProjectButtonBaseBottomSheetDialogStyle     |
| Child  | [Parent].[Style]                              | ProjectButton.Grey ProjectButton.Grey.Small |

### Object **Naming**

| Type                 | Kind          | Example                                            | case       |
|----------------------|---------------|----------------------------------------------------|------------|
| Class                | Noun          | CreditScore                                        | PascalCase |
| Function/Method      | Verb          | getUser(): User                                    | camelCase  |
| Interface            | Noun          | OnItemClickListener LoginCallback                  | PascalCase |
| Variable             | Noun          | address: String username: String fullName: String  | camelCase  |
| Variable in Plural   | Noun          | stores: MutableList<Store> products: List<Product> | camelCase  |
| Declarative Variable | is + Noun     |                                                    |            |
| is + Adjective       | isPremiumUser |                                                    |            |
| isEligible           | camelCase     |                                                    |            |

### Backing Properties

If a class has two properties which are conceptually the same but one is part of a public API and another is an implementation detail, use an underscore as the prefix for the name of the private property:

source: [https://kotlinlang.org/docs/coding-conventions.html#names-for-backing-properties](https://kotlinlang.org/docs/coding-conventions.html#names-for-backing-properties)

```jsx
class C {
    private val _elementList = mutableListOf<Element>()

    val elementList: List<Element>
         get() = _elementList
}
```

### **Class/File Naming**

Uses a pascal case.

| Type                                                       | Kind               | Suffix                               | Example    | Remarks & Alternative                                        |     |
|------------------------------------------------------------|--------------------|--------------------------------------|------------|--------------------------------------------------------------|-----|
| Regular Class                                              | Class              |                                      | Login      |                                                              |     |
| Database                                                   | Data Class         | [Name]Entity                         | UserEntity |                                                              |     |
| Api Response                                               | Data Class         | [Name]DataResponse                   |            |                                                              |     |
| [Name][ObjectName]Response → if nested object, see example | UserResponse       | UserDataResponse, UserResultResponse |            |                                                              |     |
| View/Domain Data                                           | Data Class         |                                      | User       | Based on Data Layer Model name                               |     |
| Mapper                                                     | Function, new fiie | [Name]Mapper (for object)            | UserMapper | Extension Function to[Purpose](), ex UserResponse.toDomain() |     |

User.toEntity()
UserRespone.toDomain()
UserParam.toRequest()
User.toParcelize() |  |
| Interface Implementation (Concrete Class, exclude UseCase & Repository) | Class | [Name]Listener → for view action
[Name]Callback → for general purpose
[Name]Able → for polymorphism | OnMovieItemClickListener,
Clickable,
Listenable | Name by its purpose

High order function (Anonymous or Literal) |  |
| Kotlin Extension Function | Function | [Purpose]Ext | ViewExt | Put in the one package |  |
| Activity | Class | [Purpose]Activity | LoginActivity | Put in Presentation Purpose Package eg: Login |  |
| Service | Class | [Purpose]Service | LocationService | Put in the one package |  |
| Fragment | Class | [Purpose]Fragment | ProfileFragment | Put in Presentation Purpose Package eg: Profile |  |
| BroadcastReceiver | Class | [Purpose]Receiver |  | Put in the one package |  |
| Dependency Injection Module | Koin Module | [Purpose]Module | UserModule ApiModule | Put in the one package |  |
| Application | Class | [AppName]Application | HelloWorldApplication |  |  |
| Groupie Viewholder Item | Class | [Purpose]GroupieItem | MovieGroupieItem | Put in the one package |  |
| RecyclerView Adapter | Class | [Purpose]Adapter | ProductAdapter | Put in the one package |  |
| BodyRequest Class (Data Layer) | Class | [Purpose]Request | LoginRequest |  |  |
| BodyRequest Param Class (View/Domain Layer ) | Class | [Purpose]Param | LoginParam |  |  |
| Utils | Object | [Purpose]Utils | LocationUtils |  |  |
| Event | Class | [Purpose]Event | SessionExpiredEvent |  |  |
| ItemDecoration | Class | [Purpose]ItemDecoration | DashedLineItemDecoration |  |  |

### **API Response Class Naming Rules**

```json
“data” : {
    “products”: [],
    “metadata”: {
    “limit” : 10,
    “skip”: 0,
    “count”: 5,
    “sort_by”: “latest”,
    }
}
```

Parent Class: ProductDataResponse

Child Class: ProductResponse

Paging Metadata rules:

ProductMetadataResponse → Specific case

PagingMetadataResponse → General & Reusable case

```json
“data” : {
	“province”:  {
					“id” : 10,
					“name”: “DKI Jakarta”
	}
}
```

Parent Class: ProvinceDataResponse

Child Class: ProvinceResponse

```json
“data” : {
    “id” : 10,
    “name”: “DKI Jakarta”
}
```

Class: ProvinceResponse

### **Constant and Bundle Keys**

Uses a snake case and a capital case. Put all constants in one separated object class according to its purpose.

| Type                     | Location                            | Example                                                                   |
|--------------------------|-------------------------------------|---------------------------------------------------------------------------|
| Bundle Argument          |                                     |                                                                           |
| Intent Argument          | BundleKey                           |                                                                           |
| Object Class             | const val VOD_ID: String = "vod_id" |                                                                           |
| usage : BundleKey.VOD_ID |                                     |                                                                           |
| Preference Key           | PreferenceKey Object Class          | const val ACCESS_TOKEN = "access_token" usage :PreferenceKey.ACCESS_TOKEN |
| Custom Regex             | CustomRegex Object Class            | const val MUST_CONTAIN_NUMBER_REGEX = ".*[0-9].*"                         |
| Date Format              | DateFormat Object Class             | TBC….                                                                     |
| AppConstants             | AppConstants Object Class           | const val PREMIUM = "PREMIUM"                                             |

### **Enum Class**

Uses a Pascal Case, named by its purpose and a Capital Case for its content. It is to replace `stringDef` and `intDef` from java, we use enum as a substitute in Kotlin code. Example :

```
@Parcelize enum class PlayerContentType(val contentType: String) : Parcelable {
	TV("tv"),
	TVOD("tvod"),
	VOD("vod"),
	YOUTUBE("youtube"),
	EVENT("event"),
	PREMIUM("premium"),
	FREE("free")
}
```

### **Package Name**

Use lowercase for package naming, e.g:

**com.nucleo.presentation.purchasesummary**

# Comments

Follow Java Docs Comment Style Guide
Set comment when you create complex function

Reference: https://www.youtube.com/watch?v=7Ww3RhkYE_Y

```
// Bad

// Two line
// comments

/**
  * Block comment but mis-aligned
 */

// Good

// One line comment

/*
 * Block comment
 * that is longer than 2 lines
 */

 /**
  * Class/method description (Javadoc)
  *
  * @param  url  an absolute URL giving the base location of the image
  * @param  name the location of the image, relative to the url argument
  * @return      the image at the specified URL
  * @see         Image
  */
```

# Ordering

#### **BaseActivity ordering**

```

companion object{
    fun start(context: Context){}
}

// other initialization

override fun getViewBinding() or  override val layoutResource

override fun initIntent(){}

override fun initUI(){}

override fun initAction(){}

override fun initProcess(){}

override fun initObservers(){}

//other method
```

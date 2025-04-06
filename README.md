<!--TECH4300 Mobile Development Assessment 1 Florencia Scolari ID 1847863 April 2025-->

CONSTRAINT 1. The UI will dynamically utilize available space, ensuring effective adaptation to changes in screen orientation.
    Covered on TASKS 3 & 4.
CONSTRAINT 2. Implement appropriate colour/contrast schemes and styles to facilitate easy differentiation of information on the screen from other elements.
    Covered on TASK 1
CONSTRAINT 3. Design the user interface to seamlessly support a minimum of two different languages.
    Covered on TASK 2 (Spanish and Portuguese added. With English, 3 languages covered)


Workflow:
1. Portrait Layout (ImageViews, TextViews, ConstraintLayout, ScrollView, Color Palette (WCAG guidelines for Accessible colors is min of >= 4.5:1 ratio & 16sp for text size)
2. Localisation
3. Landscape Layout
4. Other Sizes
5. Build a slide deck
6. Record video presentation
7. Submit

Out of Scope
- Night/Dark Mode Color Variation


---- 1. PORTRAIT LAYOUT TASKS ----
▸ Set strings in strings.xml
▸ Set strings in activity_main.xml
▸ Set id in activity_main.xml
▸ Set a top bar (box) in the background
    📘 Shape: Rectangle vs SVG?
    🐞 top box isn't taking its parent's height -> SOLVED. it was because it has size defined within the drawable. I removed it and it worked.

    📘 dp units
▸ Set drawable for profile picture
▸ Set circle as image container
    📘 How to make an ImageView rounded? -> SOLVED. Used ShapeableImageView instead of ImageView
    Add style for rounded container on Themes
    ⚠️ ShapeableImageView is within the default Android Studio setup. TBD if it is allowed for A1. So cool to use!
    🐞 shapeableImageView doesn't display image when running emulator. SOLVED. The right way of pointing the image resource is android:src=, I was using tools:srcCompat

--- Button Views ---
▸ Set primary and secondary styles on themes to be reusable (and colors on colors.xml)
    ⚠️ How on earth an outline button is a custom one instead of being a default view?
▸ Set secondary btn as custom btn
    🐞 Having components from Material Components are overwriting the components that don't have that theme applied. I tried to have both types but it didn't work.
       SOLUTION APPLIED: Understand and using button views only from material components (Outlined btn and Contained btn)
▸ Set color by state to add feedback after tapping btn --> No need to set it, it has been handled by Material Components

--- Text Views ---
    📘 Each view needs at least 1 vertical constraint and 1 horizontal constraint
▸ Set styles on themes.xml for heading 1, heading 2, and label
▸ Set TextViews for sections: Team Details, Work Details and Personal Details
    ⚠️ I don't have much space above the fold!! How can I go further? I mean, scroll down and have more content?
       Possible solution: using ScrollView > ConstraintView
       Let's give it a go... in a different branch for sure
       SOLUTION APPLIED: ScrollView with 1 nested child: the ConstraintLayout that I've been using. It worked!! 🚀

--- Splash Screen ---
▸ Set icon (ic_launcher) and background color

---- 2. LOCALISATION TASKS ----
▸ Set second language. Chosen: Spanish. es/strings.xml
    TEST Successful 🚀
▸ Set third language. Chosen: Portuguese. es/strings.xml
    TEST Successful 🚀

--- 3. Landscape Layout ----
▸ Test if guidelines in percentage instead of dp is better for adapt the content through different screen sizes
    SOLUTION APPLIED: Vertical guidelines in percentage. It worked!
▸ Set Landscape layout for default view

--- 4. Other Screen Sizes ----
▸ Set a version through qualifier Size for Large Size
    . Landscape Layout added
▸ Set a version through qualifier Size for Small Size
    . Landscape Layout added




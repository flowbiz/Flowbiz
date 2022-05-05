# <a id="top">Landing Home Page According The Design</a>
The Flowbiz Landing page is served by a Gatsby React server.<br>
Existing Application can be found here:<br>
https://home.flowbiz.info/BDtOaiBGS8bB06Q2

The requirement is to modify the gatsby react application in order to make the Home Page look and behave according to Design Specification:<br>
https://xd.adobe.com/view/7f86feb6-b713-4bea-a733-dd73b40035c1-2ad5/
- [1. Features](#features)
  - [1.1. Screen Mode](#screen_mode)
  - [1.2. Home Page Info Cards](#home_page_info_cards)
    - [1.2.1. Data Source](#data_source_topic)
    - [1.2.2. Card Structure](#card_structure_topic)
  - [1.3. Contact Card](#contact_card)
    - [1.3.1. Submit Contact Flow](#submit_contact_flow_topic)
  - [1.4. Footer](#footer)
  - [1.5. Navigation](#navigation)
    - [1.5.1. Sign In/Out Button](#sign_in/out_button_topic)
    - [1.5.2. Pages Links](#pages_links_topic)
    - [1.5.3. Local Switch](#local_switch_topic)
    - [1.5.4. Light/Dark Mode Switch](#light/dark_mode_switch_topic)
  - [1.6. Flowbiz Logo](#flowbiz_logo)
    - [1.6.1. Page Scrolled Up Mode](#page_scrolled_up_mode_topic)
    - [1.6.2. Scrolling Down Mode](#scrolling_down_mode_topic)
    - [1.6.3. Mobile View](#mobile_view_topic)
    - [1.6.4. Logo Link](#logo_link_topic)

- [2. RoadMap](#roadMap)
    - [2.1. Home Page Info Cards Desktop Mode](#home_page_info_cards_desktop_mode_stage)
    - [2.2. Home Page Info Cards Mobile Mode](#home_page_info_cards_mobile_mode_stage)
    - [2.3. Contact Card Desktop Mode](#contact_card_desktop_mode_stage)
    - [2.4. Contact Card Mobile Mode](#contact_card_mobile_mode_stage)
    - [2.5. Footer Desktop Mode](#footer_desktop_mode_stage)
    - [2.6. Footer Mobile Mode](#footer_mobile_mode_stage)
    - [2.7. Navigation Desktop Mode](#navigation_desktop_mode_stage)
    - [2.8. Navigation Mobile Mode](#navigation_mobile_mode_stage)
    - [2.9. Flowbiz Logo Desktop Mode](#flowbiz_logo_desktop_mode_stage)
    - [2.10. Flowbiz Logo Mobile Mode](#flowbiz_logo_mobile_mode_stage)
# 1. <a id="features">Features</a>
## 1.1. <a id="screen_mode">Screen Mode</a>
The Flowbiz landing page should be adjusted for both Desktop and Mobile views<br>
The Mobile view can be seen here: https://xd.adobe.com/view/c55a60fd-612a-4226-b33e-4f770f0c510a-9009/screen/802d8e3d-acfc-4359-b925-8b15913f4fdd ????? 
- For each page and functionality, the designer should present both modes: Desktop and Mobile
## 1.2. <a id="home_page_info_cards">Home Page Info Cards</a>
There are 4 Info Cards in the home page:<br>
1. Create & Develop Your Product<br>
2. Which one are you?<br>
3. We’ve got you covered<br>
4. How Does It Work

The cards should be presented according to the design specification
- The design specification defines 2 modes: Desktop and Mobile.<br>
The work should cover both modes.
### 1.2.1. <a id="data_source_topic">Data Source</a>
All the data in the Home cards is coming from external API.<br>
In gatsby building process it calls for get-blogs api and on response<br>
it uses the **gatsby** createNode api to create the different gatsby nodes that are needed for the site rendering.<br>
The React CardBody component receives a single card data information and renders the card visual view
### 1.2.2. <a id="card_structure_topic">Card Structure</a>
A UX Card may contain the following:
1. name - Name of the card. Usually used to render the card header text
2. headers - Optional headers list to be displayed in the card
3. description - Descriptive text to be displayed in the card. May contain also an image
4. buttons - A list of button info items that should be rendered to buttons in the card
5. style - The style card sub field is responsible to set the styling of the card<br>
It contains a motive sub field that determines the general

For example, the following card input :
```
{
  "name": "Create & Develop Your Product",
  "headers": [
    "EASY AS 1,2,3"
  ],
  "description": {
    "text": "Answer a few simple questions and let the WonderFlow wizard help you bring your app and software visions to life.",
    "image": "https://user-images.githubusercontent.com/12394551/163946957-fb473e0d-9aa6-4100-a980-15dade961213.png",
  "buttons": [
    {
      "type": "Action",
      "method": "goToWizard",
      "label": "Try the Wonderflow Wizard",
    },
    {
      "type": "Action",
      "method": "learnMore",
      "label": "Learn more",
    }
  ],
  "style": {
    "motive": "white_card",
    "button_1": "light_blue_button"
  }
}
```

should produce this Card Visual:

![card_structure_mockup1](https://user-images.githubusercontent.com/12394551/165494828-59e7d77f-79ff-4446-807d-4566c66312ab.png)

The developer should modify the React components and CSS styles in order to achieve the desired card UX style.<br>
The developer may also modify the data source by adding more card fields and values
- Specific CSS styling attributes should be configured in the relevant css part of the gatsby application
- The Card info data should only contain style keywords (motive, layout, etc.) but not specific css coding

## 1.3. <a id="contact_card">Contact Card</a>
The [Contact Card](#contact_card) let the user submit contact details.
### 1.3.1. <a id="submit_contact_flow_topic">Submit Contact Flow</a>
1. Write Name
2. Write Email
3. Describe Need (free text)
4. Submit


Filling the [Contact](../LandingPageDesign/README.md#contact_topic) details should be done in a wizard style. i.e. step by step.<br>
First, the user fills his name and clicks Next.<br>
Then the user fills his email and clicks Next.<br>
Then the user fills the need and clicks Submit.
## 1.4. <a id="footer">Footer</a>
The [Footer](#footer) is a Card that appears in every page in the site, as the last card.<br>
It presents the site navigation links, a footer image and maybe also the Flowbiz logo.

![footer_mockup1](https://user-images.githubusercontent.com/12394551/165639313-e311feeb-2eb4-4eb6-ad41-a050ba03f511.png)
## 1.5. <a id="navigation">Navigation</a>
The [Navigation](../LandingPageDesign/README.md#navigation_topic) control Panel let the user jump between the different pages of the site, sign in and out from the site and switch between Local and Light/Dark modes

![navigation_mockup1](https://user-images.githubusercontent.com/12394551/166155050-a48e36bd-ea47-405e-94d9-f6bbf8d7d3d1.png)

- https://xd.adobe.com/view/4395c0a2-5fe3-475e-86e5-09fd02be07ab-16c6/screen/1f4e9e23-8964-46fa-b680-6d582f7a848e
### 1.5.1. <a id="sign_in/out_button_topic">Sign In/Out Button</a>
A small button with a face image that let the user sign in and from the site

![sign_in/out_button_mockup1](https://user-images.githubusercontent.com/12394551/166893541-8a61ffb9-d9e4-4d8b-bb18-571707d071c6.png)

After the user signs in the icon should change to the user photo as received from the authentication server (google) with the user name

![sign_in/out_button_mockup1](https://user-images.githubusercontent.com/12394551/166894212-458712bb-2f65-4c00-b72a-6ec84e959fa9.png)
##### On Mobile View

![sign_in/out_button_mockup2](https://user-images.githubusercontent.com/12394551/166895006-f5b98fae-e97a-4470-9f76-0d4d1cc613d6.png)

### 1.5.2. <a id="pages_links_topic">Pages Links</a>
Links to the other 4 pages in the site: `How it works`, `Startups & Entrepreneurs`, `Product & dev teams` and `Outsourcing made simple`
### 1.5.3. <a id="local_switch_topic">Local Switch</a>
A switch selection button that let the user switch between the page available languages.<br>
Currently there are 2 supported languages: English and Hebrew

![local_switch_mockup1](https://user-images.githubusercontent.com/12394551/166895696-66e64fba-c897-401f-9a3d-9b8fcb17067e.png)
##### Regular, Bubble and Arrow

![local_switch_mockup2](https://user-images.githubusercontent.com/12394551/166155617-35629f75-7335-48d4-93f0-2794f8750cb7.png)
##### Clicked, Bubble and Dropdown selection
- The bubble and the selected language key are highlighted

![local_switch_mockup3](https://user-images.githubusercontent.com/12394551/166155616-51bb51e3-8707-4b88-880a-8f10076afcd8.png)
##### On Mobile View

![local_switch_mockup4](https://user-images.githubusercontent.com/12394551/166895977-c4e4f61e-2164-4371-866f-ee8903f237b1.png)
### 1.5.4. <a id="light/dark_mode_switch_topic">Light/Dark Mode Switch</a>
A switch button that let the user switch between the page Light/Dark style mode<br>
The button itself has two modes to indicate the Light/Dark mode of the page

![light/dark_mode_switch_mockup1](https://user-images.githubusercontent.com/12394551/166896285-75ebcbd6-1f4b-4b9e-8988-44603b0861f8.png)
##### Light

![light/dark_mode_switch_mockup2](https://user-images.githubusercontent.com/12394551/166155210-86b4278c-d966-4fb2-b586-70618eec2c4d.png)
##### Dark

![light/dark_mode_switch_mockup3](https://user-images.githubusercontent.com/12394551/166155209-da1702b5-f2aa-4386-bd4f-e7739a81f309.png)
## 1.6. <a id="flowbiz_logo">Flowbiz Logo</a>
The developer should code the site logo according the design.<br>
The logo is composed of two elements
##### 1. White Flowbiz word missing the 'o' letter: 'Fl wbiz'
- The white word with yellow background would produce a yellow logo visual

![flowbiz_logo_mockup1](https://user-images.githubusercontent.com/12394551/165710142-4517f05d-d7b8-4149-848d-1d36cb5e1658.png)
##### 2. Bulb Image

![flowbiz_logo_mockup2](https://user-images.githubusercontent.com/12394551/165710579-fd9a3aeb-2616-4f93-a171-2b339e2bbd5f.png)
- The white background should be transparent
- The two elements combined together produce a Flowbiz logo with a bulb as the 'o' letter

![flowbiz_logo_mockup3](https://user-images.githubusercontent.com/12394551/165711521-3b522771-ade6-4e88-bc30-7c3e39e3c336.png)
### 1.6.1. <a id="page_scrolled_up_mode_topic">Page Scrolled Up Mode</a>
When the page is scrolled all the way up, the logo appears on the upper panel as a word and a bulb

![page_scrolled_up_mode_mockup1](https://user-images.githubusercontent.com/12394551/165716505-a277c704-742d-4e98-9ba3-2c7599fdb316.png)
### 1.6.2. <a id="scrolling_down_mode_topic">Scrolling Down Mode</a>
When the user scrolls down in the page, the 'Fl biz' word fades away and only the bulb remains

![scrolling_down_mode_mockup1](https://user-images.githubusercontent.com/12394551/165717629-940a3cad-dce1-4f81-bd1c-051cbee33842.png)
### 1.6.3. <a id="mobile_view_topic">Mobile View</a>
TBD
### 1.6.4. <a id="logo_link_topic">Logo Link</a>
When the user clicks the logo, he is redirected to Home page
# 2. <a id="roadMap">RoadMap</a>
## 2.1. <a id="home_page_info_cards_desktop_mode_topic">Home Page Info Cards Desktop Mode</a>
Home Page Cards on Desktop mode look exactly as the design specification and according to requirements
- 10% of payment
- In each of the development steps, the designer reviews the work done by the development team, gives his comments and finally approves that the cards are developed according to the design
## 2.2. <a id="home_page_info_cards_mobile_mode_topic">Home Page Info Cards Mobile Mode</a>
Home Page Cards on Mobile mode look exactly as the design specification and according to requirements
- 10% of payment
## 2.3. <a id="contact_card_desktop_mode_topic">Contact Card Desktop Mode</a>
The Contact Card on Desktop mode look exactly as the design specification and according to requirements
- 10% of payment
## 2.4. <a id="contact_card_mobile_mode_topic">Contact Card Mobile Mode</a>
The Contact Card on Mobile mode look exactly as the design specification and according to requirements
- 10% of payment
## 2.5. <a id="footer_desktop_mode_topic">Footer Desktop Mode</a>
The Footer on Desktop mode look exactly as the design specification and according to requirements
- 10% of payment
## 2.6. <a id="footer_mobile_mode_topic">Footer Mobile Mode</a>
The Footer on Mobile mode look exactly as the design specification and according to requirements
- 10% of payment
## 2.7. <a id="navigation_desktop_mode_topic">Navigation Desktop Mode</a>
The Navigation on Desktop mode look exactly as the design specification and according to requirements
- 10% of payment
## 2.8. <a id="navigation_mobile_mode_topic">Navigation Mobile Mode</a>
The Navigation on Mobile mode look exactly as the design specification and according to requirements
- 10% of payment
## 2.9. <a id="flowbiz_logo_desktop_mode_topic">Flowbiz Logo Desktop Mode</a>
The Flowbiz Logo on Desktop mode look exactly as the design specification and according to requirements
- 10% of payment
## 2.10. <a id="flowbiz_logo_mobile_mode_topic">Flowbiz Logo Mobile Mode</a>
The Flowbiz Logo on Mobile mode look exactly as the design specification and according to requirements
- 10% of payment

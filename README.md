# hackathon_lonersgroup
loners group source code.  We copy the code from container in preview code power apps

foodbank2U codes - powerapp

- Main Home Page:
    Control: Screen
    Children:
    - Button2:
        Control: Classic/Button
        Properties:
          OnSelect: |+
            =Navigate('our program', ScreenTransition.Fade)
          Text: ="Food Donors"
          Fill: =RGBA(203, 102, 102, 1)
          FocusedBorderColor: =ColorFade(Self.Fill, -75%)
          X: =180
          Y: =377
    - Button1:
        Control: Classic/Button
        Properties:
          Text: ="Admin"
          Fill: =RGBA(203, 102, 102, 1)
          FocusedBorderColor: =ColorFade(Self.Fill, -75%)
          X: =180
          Y: =544
    - Label1:
        Control: Label
        Properties:
          Text: ="Foodbank2U"
          Align: =Align.Center
          BorderColor: =RGBA(220, 153, 153, 1)
          BorderThickness: =4
          DisabledBorderColor: =RGBA(202, 202, 202, 1)
          Fill: =RGBA(220, 153, 153, 1)
          FontWeight: =FontWeight.Semibold
          Height: =90
          Size: =26
          Width: =640


- our program:
    Control: Screen
    Properties:
      Fill: =RGBA(255, 255, 255, 1)
    Children:
    - Label17:
        Control: Label
        Properties:
          Text: ="*all images are taken from google and credit to all owners "
          Size: =12
          X: =39
          Y: =1012
    - Icon2:
        Control: Classic/Icon
        Variant: Home
        Properties:
          OnSelect: |+
            =Navigate('Main Home Page', ScreenTransition.Fade)
          Icon: =Icon.Leave
          X: =530
          Y: =15
    - Component1_3:
        Control: Component
        ComponentName: Component1
        Properties:
          menudata: |-
            =Table(
                {
                    ScreenID: 1, 
                    ScreenText:"Donate", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: donorform1
                 },
                   {
                    ScreenID: 2, 
                    ScreenText:"Covered Location", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: locationpage
                 },
                   {
                    ScreenID: 3, 
                    ScreenText:"Contact Us", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: contactpage
                 },
                   {
                    ScreenID: 4, 
                    ScreenText:"Our Team", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: teampage
                 }
                )
          propert: =true
          Height: =367
    - Label15:
        Control: Label
        Properties:
          Text: ="a platform that effectively connects donors, food banks, and those in need can greatly enhance the food donation process. By making donations more accessible, organized, and efficient, we can ensure that surplus food reaches the right people and helps combat hunger in our communities."
          Align: =Align.Center
          Height: =202
          Size: =15
          Width: =622
          X: =18
          Y: =165
    - Button3:
        Control: Classic/Button
        Properties:
          OnSelect: |+
            =Navigate('volunteerpage', ScreenTransition.Fade)
          Text: ="Join Our Volunteer"
          DisabledBorderColor: =RGBA(220, 153, 153, 1)
          Fill: =RGBA(220, 153, 153, 1)
          FocusedBorderColor: =ColorFade(Self.Fill, -75%)
          Size: =18
          X: =319
          Y: =820
    - Label6:
        Control: Label
        Properties:
          Text: ="We sorting and deliver surplus food to receiver "
          Height: =107
          Size: =17
          Width: =226
          X: =368
          Y: =643
    - Label5:
        Control: Label
        Properties:
          Text: ="We collecting donated food from donaters"
          Height: =131
          Size: =17
          Width: =220
          X: =39
          Y: =631
    - Image5:
        Control: Image
        Properties:
          Image: ='images (8)'
          Height: =200
          ImagePosition: =ImagePosition.Fill
          Width: =210
          X: =368
          Y: =443
    - Image4:
        Control: Image
        Properties:
          Image: ='images (9)'
          Height: =196
          ImagePosition: =ImagePosition.Fill
          Width: =210
          X: =39
          Y: =443
    - Label4:
        Control: Label
        Properties:
          Text: ="Our Program"
          Align: =Align.Center
          FontWeight: =FontWeight.Semibold
          X: =39
          Y: =340
    - Label3:
        Control: Label
        Properties:
          Text: ="FoodBank2U"
          FontWeight: =FontWeight.Bold
          Size: =25
          Y: =145
    - Label2:
        Control: Label
        Properties:
          Text: ="Foodbank2U"
          Align: =Align.Center
          Fill: =RGBA(220, 153, 153, 1)
          FontWeight: =FontWeight.Semibold
          Height: =94
          Size: =26
          Width: =640

- donorform1:
    Control: Screen
    Variant: phoneLayout_HeaderAndForm_ver3.0
    Children:
    - Icon1_4:
        Control: Classic/Icon
        Variant: Reset
        Properties:
          OnSelect: |+
            =Navigate('our program', ScreenTransition.Fade)
          Icon: =Icon.Reset
          X: =541
          Y: =12
    - Button4:
        Control: Classic/Button
        Properties:
          OnSelect: =SubmitForm(Form2)
          Text: ="Submit"
          Fill: =RGBA(220, 153, 153, 1)
          Size: =19
          X: =180
          Y: =1033
    - Component1_4:
        Control: Component
        ComponentName: Component1
        Properties:
          menudata: |-
            =Table(
                {
                    ScreenID: 1, 
                    ScreenText:"Donate", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: donorform1
                 },
                   {
                    ScreenID: 2, 
                    ScreenText:"Covered Location", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: locationpage
                 },
                   {
                    ScreenID: 3, 
                    ScreenText:"Contact Us", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: contactpage
                 },
                   {
                    ScreenID: 4, 
                    ScreenText:"Our Team", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: teampage
                 }
                )
          propert: =true
          Height: =313
    - Label13:
        Control: Label
        Properties:
          Text: ="Donate Form"
          Align: =Align.Center
          Size: =23
          X: =40
          Y: =105
    - Label12:
        Control: Label
        Properties:
          Text: ="Foodbank2U"
          Align: =Align.Center
          FontWeight: =FontWeight.Semibold
          Height: =88
          Size: =26
          Width: =452
          X: =80
    - Form2:
        Control: Form
        Layout: vertical
        Properties:
          OnSuccess: =Navigate(successpage)
          DataSource: =donor_data_for_foodbank
          DefaultMode: =FormMode.New
          Height: =801
          Y: =324
        Children:
        - Donor Name_DataCard2:
            Control: TypedDataCard
            Variant: textualEditCard
            Properties:
              DataField: ="Title"
              Default: =ThisItem.'Donor Name'
              DisplayName: =DataSourceInfo([@donor_data_for_foodbank],DataSourceInfo.DisplayName,Title)
              MaxLength: =DataSourceInfo([@donor_data_for_foodbank], DataSourceInfo.MaxLength, Title)
              Update: =DataCardValue6.Text
              DisplayMode: =Parent.DisplayMode
              Height: =50
            Children:
            - StarVisible6:
                Control: Label
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey6.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey6.Y
            - ErrorMessage6:
                Control: Label
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue6.Y + DataCardValue6.Height
            - DataCardValue6:
                Control: Classic/TextInput
                Properties:
                  Default: =Parent.Default
                  DelayOutput: =true
                  MaxLength: =Parent.MaxLength
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  PaddingLeft: =5
                  RadiusBottomLeft: =0
                  RadiusBottomRight: =0
                  RadiusTopLeft: =0
                  RadiusTopRight: =0
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey6.Y + DataCardKey6.Height + 5
            - DataCardKey6:
                Control: Label
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
        - Phone Number_DataCard2:
            Control: TypedDataCard
            Variant: textualEditCard
            Properties:
              DataField: ="field_1"
              Default: =ThisItem.'Phone Number'
              DisplayName: =DataSourceInfo([@donor_data_for_foodbank],DataSourceInfo.DisplayName,field_1)
              MaxLength: =DataSourceInfo([@donor_data_for_foodbank], DataSourceInfo.MaxLength, field_1)
              Update: =DataCardValue7.Text
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Y: =1
            Children:
            - StarVisible7:
                Control: Label
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey7.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey7.Y
            - ErrorMessage7:
                Control: Label
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue7.Y + DataCardValue7.Height
            - DataCardValue7:
                Control: Classic/TextInput
                Properties:
                  Default: =Parent.Default
                  DelayOutput: =true
                  MaxLength: =Parent.MaxLength
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  PaddingLeft: =5
                  RadiusBottomLeft: =0
                  RadiusBottomRight: =0
                  RadiusTopLeft: =0
                  RadiusTopRight: =0
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey7.Y + DataCardKey7.Height + 5
            - DataCardKey7:
                Control: Label
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
        - Type of Donation_DataCard3:
            Control: TypedDataCard
            Variant: allowedValuesStringEditCard
            Properties:
              AllowedValues: =DataSourceInfo([@donor_data_for_foodbank], DataSourceInfo.AllowedValues, field_2)
              DataField: ="field_2"
              Default: =ThisItem.'Type of Donation'
              DisplayName: =DataSourceInfo([@donor_data_for_foodbank],DataSourceInfo.DisplayName,field_2)
              Update: =DataCardValue12.Selected.Title
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Y: =2
            Children:
            - StarVisible12:
                Control: Label
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey12.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey12.Y
            - ErrorMessage12:
                Control: Label
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue12.Y + DataCardValue12.Height
            - DataCardValue12:
                Control: Classic/DropDown
                Properties:
                  Default: =Parent.Default
                  Items: =typeofonation
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey12.Y + DataCardKey12.Height + 5
            - DataCardKey12:
                Control: Label
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
        - Type of Food Donation_DataCard3:
            Control: TypedDataCard
            Variant: allowedValuesStringEditCard
            Properties:
              AllowedValues: =DataSourceInfo([@donor_data_for_foodbank], DataSourceInfo.AllowedValues, field_3)
              DataField: ="field_3"
              Default: =ThisItem.'Type of Food Donation'
              DisplayName: =DataSourceInfo([@donor_data_for_foodbank],DataSourceInfo.DisplayName,field_3)
              Update: =DataCardValue13.Selected.Title
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Y: =3
            Children:
            - StarVisible13:
                Control: Label
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey13.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey13.Y
            - ErrorMessage13:
                Control: Label
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue13.Y + DataCardValue13.Height
            - DataCardValue13:
                Control: Classic/DropDown
                Properties:
                  Default: =Parent.Default
                  Items: =fooddonation
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey13.Y + DataCardKey13.Height + 5
            - DataCardKey13:
                Control: Label
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
        - Location to Donate_DataCard3:
            Control: TypedDataCard
            Variant: allowedValuesStringEditCard
            Properties:
              AllowedValues: =DataSourceInfo([@donor_data_for_foodbank], DataSourceInfo.AllowedValues, field_4)
              DataField: ="field_4"
              Default: =ThisItem.'Location to Donate'
              DisplayName: =DataSourceInfo([@donor_data_for_foodbank],DataSourceInfo.DisplayName,field_4)
              Update: =DataCardValue11.Selected.Title
              DisplayMode: =Parent.DisplayMode
              Height: =155
              Y: =4
            Children:
            - StarVisible11:
                Control: Label
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey11.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey11.Y
            - ErrorMessage11:
                Control: Label
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =28
            - DataCardValue11:
                Control: Classic/DropDown
                Properties:
                  Default: =Parent.Default
                  Items: =locationtodonate
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey11.Y + DataCardKey11.Height + 5
            - DataCardKey11:
                Control: Label
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
    - RectQuickActionBar3:
        Control: Rectangle
        Properties:
          Fill: =RGBA(220, 153, 153, 1)
          Height: =88
          Width: =Parent.Width


- successpage:
    Control: Screen
    Variant: phoneLayout_Success_ver3.0
    Children:
    - LblSuccessMsg1:
        Control: Label
        Properties:
          OnSelect: |+
            =Navigate('our program', ScreenTransition.Fade)
          Text: ="This was successfully completed"
          Align: =Align.Center
          AutoHeight: =true
          Height: =iconCircle1.Height
          Width: =Parent.Width * 0.75
          X: =Parent.Width/2 - Self.Width/2
          Y: =iconCheck1.Y + iconCheck1.Height + 100
    - iconCheck1:
        Control: Classic/Icon
        Variant: Check
        Properties:
          OnSelect: |+
            =Navigate('our program', ScreenTransition.Fade)
          Height: =iconCircle1.Height
          Icon: =Icon.Check
          PaddingBottom: =Self.PaddingTop
          PaddingLeft: =Self.PaddingTop
          PaddingRight: =Self.PaddingTop
          PaddingTop: =18
          Width: =iconCircle1.Width
          X: =Parent.Width/2 - Self.Width/2
          Y: =(Parent.Height/2 - Self.Height/2) * .7
    - iconCircle1:
        Control: Circle
        Variant: Circle
        Properties:
          X: =Parent.Width/2 - Self.Width/2
          Y: =(Parent.Height/2 - Self.Height/2) * .7


- locationpage:
    Control: Screen
    Children:
    - Label17_1:
        Control: Label
        Properties:
          Text: ="*all images are taken from google and credit to all owners "
          Size: =12
          X: =40
          Y: =1042
    - Icon2_5:
        Control: Classic/Icon
        Variant: Home
        Properties:
          OnSelect: |+
            =Navigate('Main Home Page', ScreenTransition.Fade)
          Icon: =Icon.Leave
          X: =117
          Y: =9
    - Icon1_1:
        Control: Classic/Icon
        Variant: Reset
        Properties:
          OnSelect: |+
            =Navigate('our program', ScreenTransition.Fade)
          Icon: =Icon.Reset
          X: =559
          Y: =9
    - Component1_7:
        Control: Component
        ComponentName: Component1
        Properties:
          menudata: |-
            =Table(
                {
                    ScreenID: 1, 
                    ScreenText:"Donate", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: donorform1
                 },
                   {
                    ScreenID: 2, 
                    ScreenText:"Covered Location", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: locationpage
                 },
                   {
                    ScreenID: 3, 
                    ScreenText:"Contact Us", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: contactpage
                 },
                   {
                    ScreenID: 4, 
                    ScreenText:"Our Team", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: teampage
                 }
                )
          propert: =true
          Height: =337
    - Label9_3:
        Control: Label
        Properties:
          Text: ="Kuala Selangor"
          Height: =80
          Width: =202
          X: =385
          Y: =923
    - Label9_2:
        Control: Label
        Properties:
          Text: ="Klang"
          Height: =60
          Width: =202
          X: =48
          Y: =923
    - Label9_1:
        Control: Label
        Properties:
          Text: ="Shah Alam"
          Height: =60
          Width: =202
          X: =391
          Y: =547
    - Label9:
        Control: Label
        Properties:
          Text: ="Setia Alam"
          Height: =60
          Width: =202
          X: =48
          Y: =547
    - Image6:
        Control: Image
        Properties:
          Image: ='images (7)'
          Height: =202
          ImagePosition: =ImagePosition.Fill
          Width: =302
          X: =321
          Y: =702
    - Image3:
        Control: Image
        Properties:
          Image: ='download (7)'
          Height: =202
          ImagePosition: =ImagePosition.Fill
          Width: =280
          X: =12
          Y: =702
    - Image2:
        Control: Image
        Properties:
          Image: ='download (5)'
          Height: =205
          ImagePosition: =ImagePosition.Fill
          Width: =302
          X: =321
          Y: =323
    - Label8:
        Control: Label
        Properties:
          Text: ="Covered Location"
          Align: =Align.Center
          FontWeight: =FontWeight.Bold
          X: =12
          Y: =123
    - Image1:
        Control: Image
        Properties:
          Image: ='download (6)'
          DisplayMode: =DisplayMode.View
          Height: =205
          ImagePosition: =ImagePosition.Fill
          Width: =280
          X: =12
          Y: =323
    - Label10:
        Control: Label
        Properties:
          Text: ="Foodbank2U"
          Align: =Align.Center
          Fill: =RGBA(220, 153, 153, 1)
          FontWeight: =FontWeight.Semibold
          Height: =83
          Size: =26
          Width: =640

- contactpage:
    Control: Screen
    Children:
    - Label17_2:
        Control: Label
        Properties:
          Text: ="*all images are taken from google and credit to all owners "
          Size: =12
          X: =59
          Y: =1032
    - Icon1_2:
        Control: Classic/Icon
        Variant: Reset
        Properties:
          OnSelect: |+
            =Navigate('our program', ScreenTransition.Fade)
          Icon: =Icon.Reset
          X: =557
          Y: =13
    - Icon2_6:
        Control: Classic/Icon
        Variant: Home
        Properties:
          OnSelect: |+
            =Navigate('Main Home Page', ScreenTransition.Fade)
          Icon: =Icon.Leave
          X: =110
          Y: =13
    - Component1_6:
        Control: Component
        ComponentName: Component1
        Properties:
          menudata: |-
            =Table(
                {
                    ScreenID: 1, 
                    ScreenText:"Donate", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: donorform1
                 },
                   {
                    ScreenID: 2, 
                    ScreenText:"Covered Location", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: locationpage
                 },
                   {
                    ScreenID: 3, 
                    ScreenText:"Contact Us", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: contactpage
                 },
                   {
                    ScreenID: 4, 
                    ScreenText:"Our Team", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: teampage
                 }
                )
          propert: =true
          Height: =337
          Y: =13
    - Form6:
        Control: Form
        Layout: vertical
        Properties:
          OnSuccess: =Navigate(successpage_1)
          DataSource: =contact_1
          DefaultMode: =FormMode.New
          Height: =321
          Y: =192
        Children:
        - Email Address_DataCard3:
            Control: TypedDataCard
            Variant: textualEditCard
            Properties:
              DataField: ="EmailAddress"
              Default: =ThisItem.'Email Address'
              DisplayName: =DataSourceInfo([@contact_1],DataSourceInfo.DisplayName,'EmailAddress')
              MaxLength: =DataSourceInfo([@contact_1], DataSourceInfo.MaxLength, 'EmailAddress')
              Update: =DataCardValue26.Text
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Width: =320
            Children:
            - StarVisible26:
                Control: Label
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey26.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey26.Y
            - ErrorMessage26:
                Control: Label
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue26.Y + DataCardValue26.Height
            - DataCardValue26:
                Control: Classic/TextInput
                Properties:
                  Default: =Parent.Default
                  DelayOutput: =true
                  MaxLength: =Parent.MaxLength
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  PaddingLeft: =5
                  RadiusBottomLeft: =0
                  RadiusBottomRight: =0
                  RadiusTopLeft: =0
                  RadiusTopRight: =0
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey26.Y + DataCardKey26.Height + 5
            - DataCardKey26:
                Control: Label
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
        - Text_DataCard3:
            Control: TypedDataCard
            Variant: textualEditCard
            Properties:
              DataField: ="Text"
              Default: =ThisItem.Text
              DisplayName: =DataSourceInfo([@contact_1],DataSourceInfo.DisplayName,'Text')
              MaxLength: =DataSourceInfo([@contact_1], DataSourceInfo.MaxLength, 'Text')
              Update: =DataCardValue27.Text
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Width: =320
              X: =1
            Children:
            - StarVisible27:
                Control: Label
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey27.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey27.Y
            - ErrorMessage27:
                Control: Label
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue27.Y + DataCardValue27.Height
            - DataCardValue27:
                Control: Classic/TextInput
                Properties:
                  Default: =Parent.Default
                  DelayOutput: =true
                  MaxLength: =Parent.MaxLength
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  PaddingLeft: =5
                  RadiusBottomLeft: =0
                  RadiusBottomRight: =0
                  RadiusTopLeft: =0
                  RadiusTopRight: =0
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey27.Y + DataCardKey27.Height + 5
            - DataCardKey27:
                Control: Label
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
        - Your name_DataCard1:
            Control: TypedDataCard
            Variant: textualEditCard
            Properties:
              DataField: ="Yourname"
              Default: =ThisItem.'Your name'
              DisplayName: =DataSourceInfo([@contact_1],DataSourceInfo.DisplayName,'Yourname')
              MaxLength: =DataSourceInfo([@contact_1], DataSourceInfo.MaxLength, 'Yourname')
              Update: =DataCardValue28.Text
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Width: =320
              Y: =1
            Children:
            - StarVisible28:
                Control: Label
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey28.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey28.Y
            - ErrorMessage28:
                Control: Label
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue28.Y + DataCardValue28.Height
            - DataCardValue28:
                Control: Classic/TextInput
                Properties:
                  Default: =Parent.Default
                  DelayOutput: =true
                  MaxLength: =Parent.MaxLength
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  PaddingLeft: =5
                  RadiusBottomLeft: =0
                  RadiusBottomRight: =0
                  RadiusTopLeft: =0
                  RadiusTopRight: =0
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey28.Y + DataCardKey28.Height + 5
            - DataCardKey28:
                Control: Label
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
    - Button5:
        Control: Classic/Button
        Properties:
          OnSelect: =SubmitForm(Form6)
          Text: ="Submit"
          Fill: =RGBA(220, 153, 153, 1)
          Height: =54
          Width: =217
          X: =192
          Y: =512
    - Image7_4:
        Control: Image
        Properties:
          Image: =youtube
          Height: =67
          Width: =112
          X: =324
          Y: =854
    - Image7_3:
        Control: Image
        Properties:
          Image: =twitter
          Height: =67
          Width: =112
          X: =39
          Y: =854
    - Image7_2:
        Control: Image
        Properties:
          Image: =facebook
          Height: =67
          Width: =112
          X: =39
          Y: =761
    - Image7_1:
        Control: Image
        Properties:
          Image: =instagram
          Height: =67
          Width: =112
          X: =324
          Y: =761
    - Button4_4:
        Control: Classic/Button
        Properties:
          OnSelect: =Launch("https://www.youtube.com/")
          Text: ="YouTube"
          Align: =Align.Right
          Color: =RGBA(0, 0, 0, 1)
          Fill: =RGBA(238, 204, 204, 1)
          Height: =74
          Width: =267
          X: =333
          Y: =851
    - Button4_3:
        Control: Classic/Button
        Properties:
          OnSelect: =Launch("https://x.com/X")
          Text: ="X/Twitter"
          Align: =Align.Right
          Color: =RGBA(0, 0, 0, 1)
          Fill: =RGBA(238, 204, 204, 1)
          X: =39
          Y: =851
    - Button4_2:
        Control: Classic/Button
        Properties:
          OnSelect: =Launch("https://www.facebook.com/facebook")
          Text: ="Facebook"
          Align: =Align.Right
          Color: =RGBA(0, 0, 0, 1)
          Fill: =RGBA(238, 204, 204, 1)
          Height: =81
          Width: =279
          X: =39
          Y: =754
    - Button4_1:
        Control: Classic/Button
        Properties:
          OnSelect: =Launch("https://www.instagram.com/instagram/")
          Text: ="Instagram"
          Align: =Align.Right
          Color: =RGBA(0, 0, 0, 1)
          Fill: =RGBA(238, 204, 204, 1)
          Height: =81
          Width: =267
          X: =333
          Y: =754
    - Label16:
        Control: Label
        Properties:
          Text: ="Contact Us"
          Align: =Align.Center
          Font: =Font.Arial
          FontWeight: =FontWeight.Bold
          X: =40
          Y: =113
    - Label11:
        Control: Label
        Properties:
          Text: ="Foodbank2U"
          Align: =Align.Center
          Fill: =RGBA(220, 153, 153, 1)
          FontWeight: =FontWeight.Semibold
          Height: =91
          Size: =26
          Width: =640


- teampage:
    Control: Screen
    Children:
    - Label17_3:
        Control: Label
        Properties:
          Text: ="*all images are taken from google and credit to all owners "
          Size: =12
          X: =40
          Y: =1066
    - Icon1_3:
        Control: Classic/Icon
        Variant: Reset
        Properties:
          OnSelect: |+
            =Navigate('our program', ScreenTransition.Fade)
          Icon: =Icon.Reset
          X: =567
          Y: =15
    - Icon2_7:
        Control: Classic/Icon
        Variant: Home
        Properties:
          OnSelect: |+
            =Navigate('Main Home Page', ScreenTransition.Fade)
          Icon: =Icon.Leave
          X: =106
          Y: =15
    - Component1_8:
        Control: Component
        ComponentName: Component1
        Properties:
          menudata: |-
            =Table(
                {
                    ScreenID: 1, 
                    ScreenText:"Donate", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: donorform1
                 },
                   {
                    ScreenID: 2, 
                    ScreenText:"Covered Location", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: locationpage
                 },
                   {
                    ScreenID: 3, 
                    ScreenText:"Contact Us", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: contactpage
                 },
                   {
                    ScreenID: 4, 
                    ScreenText:"Our Team", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: teampage
                 }
                )
          propert: =true
          Height: =337
          Y: =15
    - Label23_2:
        Control: Label
        Properties:
          Text: |-
            ="Muhammad Noor bin Hakim 
            Chief of Logistics"
          Align: =Align.Center
          Height: =67
          Size: =14
          Width: =215
          X: =352
          Y: =988
    - Label22_2:
        Control: Label
        Properties:
          Text: |-
            ="Farah Farhana binti Amir
            Administration"
          Align: =Align.Center
          Height: =77
          Size: =14
          Width: =140
          X: =61
          Y: =983
    - Image9_2:
        Control: Image
        Properties:
          Image: ='download (10)'
          Height: =200
          Width: =150
          X: =385
          Y: =783
    - Image8_2:
        Control: Image
        Properties:
          Image: ='download (12)'
          Height: =158
          Width: =150
          X: =63
          Y: =804
    - Label23_1:
        Control: Label
        Properties:
          Text: |-
            ="Muqsal Hakimi bin Aimin
            Main of Delivery Men"
          Align: =Align.Center
          Height: =67
          Size: =14
          Width: =215
          X: =371
          Y: =696
    - Label22_1:
        Control: Label
        Properties:
          Text: |-
            ="Azhar Irfan bin Muhd Harith
            Chief of Volunteering
            "
          Align: =Align.Center
          Height: =77
          Size: =14
          Width: =199
          X: =57
          Y: =686
    - Image9_1:
        Control: Image
        Properties:
          Image: ='download (11)'
          Height: =158
          ImagePosition: =ImagePosition.Fill
          Width: =150
          X: =404
          Y: =514
    - Image8_1:
        Control: Image
        Properties:
          Image: ='download (9)'
          Height: =158
          ImagePosition: =ImagePosition.Fill
          Width: =150
          X: =82
          Y: =514
    - Label23:
        Control: Label
        Properties:
          Text: |-
            ="Erina Farah binti Iqbal
            Co-Founder"
          Align: =Align.Center
          Height: =67
          Size: =14
          Width: =215
          X: =385
          Y: =399
    - Label22:
        Control: Label
        Properties:
          Text: |-
            ="Shahrul Hakim bin Muhd
            Founder"
          Align: =Align.Center
          Height: =77
          Size: =14
          Width: =245
          X: =34
          Y: =399
    - Image9:
        Control: Image
        Properties:
          Image: ='download (13)'
          Height: =158
          ImagePosition: =ImagePosition.Fill
          Width: =150
          X: =404
          Y: =224
    - Image8:
        Control: Image
        Properties:
          Image: ='download (8)'
          Height: =158
          ImagePosition: =ImagePosition.Fill
          Width: =150
          X: =82
          Y: =224
    - Label21:
        Control: Label
        Properties:
          Text: ="Our Team"
          FontWeight: =FontWeight.Bold
          Size: =22
          X: =40
          Y: =133
    - Label11_1:
        Control: Label
        Properties:
          Text: ="Foodbank2U"
          Align: =Align.Center
          Fill: =RGBA(220, 153, 153, 1)
          Height: =95
          Size: =26
          Width: =640


- volunteerpage:
    Control: Screen
    Children:
    - Icon1:
        Control: Classic/Icon
        Variant: Reset
        Properties:
          OnSelect: |+
            =Navigate('our program', ScreenTransition.Fade)
          Icon: =Icon.Reset
          X: =540
          Y: =16
    - Component1_9:
        Control: Component
        ComponentName: Component1
        Properties:
          menudata: |-
            =Table(
                {
                    ScreenID: 1, 
                    ScreenText:"Donate", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: donorform1
                 },
                   {
                    ScreenID: 2, 
                    ScreenText:"Covered Location", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: locationpage
                 },
                   {
                    ScreenID: 3, 
                    ScreenText:"Contact Us", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: contactpage
                 },
                   {
                    ScreenID: 4, 
                    ScreenText:"Our Team", 
                    ScreenIcon:Icon.HorizontalLine,
                    ScreenValue: teampage
                 }
                )
          propert: =true
          Height: =337
          Y: =16
    - Label17_4:
        Control: Label
        Properties:
          Text: ="*all images are taken from google and credit to all owners "
          Size: =12
          X: =80
          Y: =127
    - Label14:
        Control: Label
        Properties:
          Text: ="Whatsapp Group of  Foodbank2U Volunteers"
          Height: =146
          Size: =15
          Width: =305
          X: =279
          Y: =228
    - Image7:
        Control: Image
        Properties:
          Image: =images
          Height: =222
          Width: =232
          X: =30
          Y: =190
    - Button4_5:
        Control: Classic/Button
        Properties:
          OnSelect: =SubmitForm(Form1)
          Text: ="Submit"
          Fill: =RGBA(220, 153, 153, 1)
          Size: =19
          X: =180
          Y: =1033
    - Form1:
        Control: Form
        Layout: vertical
        Properties:
          OnSuccess: =Navigate(successpage_1)
          DataSource: =volunteer
          DefaultMode: =FormMode.New
          Height: =569
          Y: =447
        Children:
        - Full Name_DataCard1:
            Control: TypedDataCard
            Variant: textualEditCard
            Layout: vertical
            Properties:
              DataField: ="Title"
              Default: =ThisItem.'Full Name'
              DisplayName: =DataSourceInfo([@volunteer],DataSourceInfo.DisplayName,'Title')
              MaxLength: =DataSourceInfo([@volunteer], DataSourceInfo.MaxLength, 'Title')
              Update: =DataCardValue1.Text
              DisplayMode: =Parent.DisplayMode
              Height: =50
            Children:
            - StarVisible1:
                Control: Label
                Layout: vertical
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey1.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey1.Y
            - ErrorMessage1:
                Control: Label
                Layout: vertical
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue1.Y + DataCardValue1.Height
            - DataCardValue1:
                Control: Classic/TextInput
                Layout: vertical
                Properties:
                  Default: =Parent.Default
                  DelayOutput: =true
                  MaxLength: =Parent.MaxLength
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  PaddingLeft: =5
                  RadiusBottomLeft: =0
                  RadiusBottomRight: =0
                  RadiusTopLeft: =0
                  RadiusTopRight: =0
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey1.Y + DataCardKey1.Height + 5
            - DataCardKey1:
                Control: Label
                Layout: vertical
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
        - Phone Number_DataCard1:
            Control: TypedDataCard
            Variant: textualEditCard
            Layout: vertical
            Properties:
              DataField: ="field_1"
              Default: =ThisItem.'Phone Number'
              DisplayName: =DataSourceInfo([@volunteer],DataSourceInfo.DisplayName,'field_1')
              MaxLength: =DataSourceInfo([@volunteer], DataSourceInfo.MaxLength, 'field_1')
              Update: =DataCardValue2.Text
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Y: =1
            Children:
            - StarVisible2:
                Control: Label
                Layout: vertical
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey2.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey2.Y
            - ErrorMessage2:
                Control: Label
                Layout: vertical
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue2.Y + DataCardValue2.Height
            - DataCardValue2:
                Control: Classic/TextInput
                Layout: vertical
                Properties:
                  Default: =Parent.Default
                  DelayOutput: =true
                  MaxLength: =Parent.MaxLength
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  PaddingLeft: =5
                  RadiusBottomLeft: =0
                  RadiusBottomRight: =0
                  RadiusTopLeft: =0
                  RadiusTopRight: =0
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey2.Y + DataCardKey2.Height + 5
            - DataCardKey2:
                Control: Label
                Layout: vertical
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
        - Address_DataCard1:
            Control: TypedDataCard
            Variant: textualEditCard
            Layout: vertical
            Properties:
              DataField: ="field_2"
              Default: =ThisItem.Address
              DisplayName: =DataSourceInfo([@volunteer],DataSourceInfo.DisplayName,'field_2')
              MaxLength: =DataSourceInfo([@volunteer], DataSourceInfo.MaxLength, 'field_2')
              Update: =DataCardValue3.Text
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Y: =2
            Children:
            - StarVisible3:
                Control: Label
                Layout: vertical
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey3.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey3.Y
            - ErrorMessage3:
                Control: Label
                Layout: vertical
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue3.Y + DataCardValue3.Height
            - DataCardValue3:
                Control: Classic/TextInput
                Layout: vertical
                Properties:
                  Default: =Parent.Default
                  DelayOutput: =true
                  MaxLength: =Parent.MaxLength
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  PaddingLeft: =5
                  RadiusBottomLeft: =0
                  RadiusBottomRight: =0
                  RadiusTopLeft: =0
                  RadiusTopRight: =0
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey3.Y + DataCardKey3.Height + 5
            - DataCardKey3:
                Control: Label
                Layout: vertical
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
        - Emergency Contact (Phone)_DataCard1:
            Control: TypedDataCard
            Variant: textualEditCard
            Layout: vertical
            Properties:
              DataField: ="field_4"
              Default: =ThisItem.'Emergency Contact (Phone)'
              DisplayName: =DataSourceInfo([@volunteer],DataSourceInfo.DisplayName,'field_4')
              MaxLength: =DataSourceInfo([@volunteer], DataSourceInfo.MaxLength, 'field_4')
              Update: =DataCardValue4.Text
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Y: =3
            Children:
            - StarVisible4:
                Control: Label
                Layout: vertical
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey4.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey4.Y
            - ErrorMessage4:
                Control: Label
                Layout: vertical
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue4.Y + DataCardValue4.Height
            - DataCardValue4:
                Control: Classic/TextInput
                Layout: vertical
                Properties:
                  Default: =Parent.Default
                  DelayOutput: =true
                  MaxLength: =Parent.MaxLength
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  PaddingLeft: =5
                  RadiusBottomLeft: =0
                  RadiusBottomRight: =0
                  RadiusTopLeft: =0
                  RadiusTopRight: =0
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey4.Y + DataCardKey4.Height + 5
            - DataCardKey4:
                Control: Label
                Layout: vertical
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
        - Emergency Contact (Name)_DataCard1:
            Control: TypedDataCard
            Variant: textualEditCard
            Layout: vertical
            Properties:
              DataField: ="field_5"
              Default: =ThisItem.'Emergency Contact (Name)'
              DisplayName: =DataSourceInfo([@volunteer],DataSourceInfo.DisplayName,'field_5')
              MaxLength: =DataSourceInfo([@volunteer], DataSourceInfo.MaxLength, 'field_5')
              Update: =DataCardValue5.Text
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Y: =4
            Children:
            - StarVisible5:
                Control: Label
                Layout: vertical
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey5.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey5.Y
            - ErrorMessage5:
                Control: Label
                Layout: vertical
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue5.Y + DataCardValue5.Height
            - DataCardValue5:
                Control: Classic/TextInput
                Layout: vertical
                Properties:
                  Default: =Parent.Default
                  DelayOutput: =true
                  MaxLength: =Parent.MaxLength
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  PaddingLeft: =5
                  RadiusBottomLeft: =0
                  RadiusBottomRight: =0
                  RadiusTopLeft: =0
                  RadiusTopRight: =0
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey5.Y + DataCardKey5.Height + 5
            - DataCardKey5:
                Control: Label
                Layout: vertical
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
        - Emergency Contact (Relationship)_DataCard1:
            Control: TypedDataCard
            Variant: textualEditCard
            Layout: vertical
            Properties:
              DataField: ="field_6"
              Default: =ThisItem.'Emergency Contact (Relationship)'
              DisplayName: =DataSourceInfo([@volunteer],DataSourceInfo.DisplayName,'field_6')
              MaxLength: =DataSourceInfo([@volunteer], DataSourceInfo.MaxLength, 'field_6')
              Update: =DataCardValue8.Text
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Y: =5
            Children:
            - StarVisible8:
                Control: Label
                Layout: vertical
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey8.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey8.Y
            - ErrorMessage8:
                Control: Label
                Layout: vertical
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue8.Y + DataCardValue8.Height
            - DataCardValue8:
                Control: Classic/TextInput
                Layout: vertical
                Properties:
                  Default: =Parent.Default
                  DelayOutput: =true
                  MaxLength: =Parent.MaxLength
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  PaddingLeft: =5
                  RadiusBottomLeft: =0
                  RadiusBottomRight: =0
                  RadiusTopLeft: =0
                  RadiusTopRight: =0
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey8.Y + DataCardKey8.Height + 5
            - DataCardKey8:
                Control: Label
                Layout: vertical
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
        - Volunteer Role_DataCard2:
            Control: TypedDataCard
            Variant: allowedValuesStringEditCard
            Layout: vertical
            Properties:
              AllowedValues: =DataSourceInfo([@volunteer], DataSourceInfo.AllowedValues, 'field_7')
              DataField: ="field_7"
              Default: =ThisItem.'Volunteer Role'
              DisplayName: =DataSourceInfo([@volunteer],DataSourceInfo.DisplayName,'field_7')
              Update: =DataCardValue10.Selected.'Volunteer Role'
              DisplayMode: =Parent.DisplayMode
              Height: =50
              Y: =6
            Children:
            - StarVisible10:
                Control: Label
                Layout: vertical
                Properties:
                  Text: ="*"
                  Align: =Align.Center
                  Height: =DataCardKey10.Height
                  Visible: =And(Parent.Required, Parent.DisplayMode=DisplayMode.Edit)
                  Width: =30
                  Wrap: =false
                  Y: =DataCardKey10.Y
            - ErrorMessage10:
                Control: Label
                Layout: vertical
                Properties:
                  Live: =Live.Assertive
                  Text: =Parent.Error
                  AutoHeight: =true
                  Height: =10
                  PaddingBottom: =0
                  PaddingLeft: =0
                  PaddingRight: =0
                  PaddingTop: =0
                  Visible: =Parent.DisplayMode=DisplayMode.Edit
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardValue10.Y + DataCardValue10.Height
            - DataCardValue10:
                Control: Classic/DropDown
                Layout: vertical
                Properties:
                  Default: =Parent.Default
                  Items: =volunteer
                  Tooltip: =Parent.DisplayName
                  BorderColor: =If(IsBlank(Parent.Error), Parent.BorderColor, Color.Red)
                  DisplayMode: =Parent.DisplayMode
                  Width: =Parent.Width - 60
                  X: =30
                  Y: =DataCardKey10.Y + DataCardKey10.Height + 5
            - DataCardKey10:
                Control: Label
                Layout: vertical
                Properties:
                  Text: =Parent.DisplayName
                  AutoHeight: =true
                  Height: =48
                  Width: =Parent.Width - 60
                  Wrap: =false
                  X: =30
                  Y: =10
    - Label24:
        Control: Label
        Properties:
          Text: ="Join Our Volunteer"
          Align: =Align.Center
          Fill: =RGBA(220, 153, 153, 1)
          FontWeight: =FontWeight.Semibold
          Height: =97
          Width: =640


- successpage_1:
    Control: Screen
    Variant: phoneLayout_Success_ver3.0
    Children:
    - LblSuccessMsg1_1:
        Control: Label
        Properties:
          OnSelect: |+
            =Navigate('our program', ScreenTransition.Fade)
          Text: ="This was successfully completed"
          Align: =Align.Center
          AutoHeight: =true
          Height: =iconCircle1_1.Height
          Width: =Parent.Width * 0.75
          X: =Parent.Width/2 - Self.Width/2
          Y: =iconCheck1_1.Y + iconCheck1_1.Height + 100
    - iconCheck1_1:
        Control: Classic/Icon
        Variant: Check
        Properties:
          OnSelect: |+
            =Navigate('our program', ScreenTransition.Fade)
          Height: =iconCircle1_1.Height
          Icon: =Icon.Check
          PaddingBottom: =Self.PaddingTop
          PaddingLeft: =Self.PaddingTop
          PaddingRight: =Self.PaddingTop
          PaddingTop: =18
          Width: =iconCircle1_1.Width
          X: =Parent.Width/2 - Self.Width/2
          Y: =(Parent.Height/2 - Self.Height/2) * .7
    - iconCircle1_1:
        Control: Circle
        Variant: Circle
        Properties:
          X: =Parent.Width/2 - Self.Width/2
          Y: =(Parent.Height/2 - Self.Height/2) * .7


App Overview:

My Garden is a simple game that allows you to add plants to your garden and keep them alive by watering them on time. The app illustrates the power of widgets and collection widgets by making it easier for the user to monitor and water their plants from the home screen

Commits:

First commit: starter code.

The second commit: Widget is added to home screen by adding the proper activity and XML files, and then defining the pending intent that launches the MainActivity of the app from the widget.

The third commit: The widget is now provided with a "watering service" that operates in the background once the home screen widget is clicked. The logic identifies all living plants (plants that have exceeded their maximum unwatered time are 'dead') and then waters them, essentially resetting their "last watered time" in the process - this is done by adding an additional pending intent that launches this service. The previous intent still opens the app when the user clicks on the widget.

The fourth commit: This commit establishes a two-way communication between widget and app by providing information from the app to the widget regarding the plant that is the "driest"; the code then updates the widget picture appearance to reflect that specific plant type and the specific condition of that plant.

This fifth commit: The app is redesigned to have the user water ONLY the "driest" plant.  In other words, the fourth commit communicated the state of the "driest" plant from the app to the widget, and this commit takes that information (what is the driest plant) and communicates this back to the app, so that the watering is specific for this plant only.  In addition, clicking on the widget opens the Detail View for this plant.
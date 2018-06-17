App Overview:

My Garden is a simple game that allows you to add plants to your garden and keep them alive by watering them on time. The app illustrates the power of widgets and collection widgets by making it easier for the user to monitor and water their plants from the home screen

Commits:

First commit: starter code.

The second commit: Widget is added to home screen by adding the proper activity and XML files, and then defining the pending intent that launches the MainActivity of the app from the widget.

The third commit: The widget is now provided with a "watering service" that operates in the background once the home screen widget is clicked.  The logic identifies all living plants (plants that have exceeded their maximum unwatered time are 'dead') and then waters them, essentially resetting their "last watered time" in the process - this is done by adding an additional pending intent that launches this service.  The previous intent still opens the app when the user clicks on the widget.

This fourth commit: This commit establishes a two-way communication between widget and app by providing information from the app to the widget regarding the plant that is the "driest"; the code then updates the widget picture appearance to reflect that specific plant type and the specific condition of that plant.
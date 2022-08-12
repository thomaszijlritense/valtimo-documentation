# Available feature toggles

Sometimes different features in implementations need to be switched on or off. This could be because a feature
is (not) needed, or a feature is currently in development and is switched off by default, enabling the release chain to
continue uninhibited.

Below is an overview of available feature toggles for Valtimo, with a short description of their function.

## Front-end

In the front-end, feature toggles can be configured under the `featureToggles` key in the Angular environment file(s)
with a `boolean` value.

* **`disableFormFlow`**

  By default, it is assumed the `form-flow` module is configured in the back-end, and thus a form flow option is
  available on the Process links admin page. If this module is not configured, use this toggle to disable the option on
  the Process links page

* **`enableHackathonCasesPage`**

  The Valtimo product development team participated in a Hackathon and developed a special cases page for municipalities.
  This feature toggle exists for demo purposes, and it is advised not to configure it, leaving the page disabled.

* **`showUserNameInTopBar`**

  If enabled, the full name of the user currently logged in is shown in the top bar next to the user menu button.
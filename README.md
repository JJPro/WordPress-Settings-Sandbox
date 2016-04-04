**Forked from tommcfarlin, made the following changes**

* Commented out code related to tabs, only one theme page left. 
* Commented out code related to checking existence of options
* Commented out old form, and added new form right above the old code. 
* Changed to single page format: 
    1. changed $page parameter in all <code>add_settings_section()</code> and <code>add_settings_field()</code> to 'sandbox_theme_options'
    2. changed $option_group parameter in all <code>register_setting()</code> to the same group, give it whatever name you want, I personally named the group  'sandbox_theme_options', the same as the page name, but you can name the group with anything. 
    3. call the following two functions inside the form: 
        <pre>
  settings_fields( 'sandbox_theme_options' ); // this is our option group name
  do_settings_sections( 'sandbox_theme_options' ); // this is the page to render
        </pre>

## happy path
* greet
  - utter_greet
* faq
  - respond_faq
  - utter_helpful
* affirm
  - slot{"helpful": "True"}
  - utter_thanks
  - action_restart
## interactive_story_1
* greet
    - utter_greet
* faq
    - respond_faq
    - utter_helpful
    - action_listen
    - slot{"helpful": "False"}
    - utter_reask
## interactive_story_1
* greet
    - utter_greet
* faq
    - respond_faq
    - utter_helpful
* helpful{"helpful": "False"}
    - slot{"helpful": "False"}
    - utter_reask
* faq
    - respond_faq
    - utter_helpful
    - utter_helpful
* helpful{"helpful": "True"}
    - slot{"helpful": "True"}
    - utter_thanks

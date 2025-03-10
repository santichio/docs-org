# Software Development Policy

this document define how the team gonna work

- We use agile with scrum
- Sprints of 2 weeks
- Committees to make decision, define deliveries and for prioritization (1 time for month), its more macro. Need to be made by product or team. High management team.
- For each sprint, must have these meeting:
    1. Sprint review meet on last sprint’s Friday last hour; (all team) (1hr) (1/sprint)
    2. Sprint planning meet on first sprint’s Monday in first hour, and don’t have dally; (all team) (1hr) (1/sprint)
    3. Product definition meet; (by product) (2hr) (1/month)
        
        First everybody in this product development and client need to raise all suggestions, and then tech lead gonna select relevant ones to be discussed in the meeting.
        
    4. Product client review meet; (by product) (1hr) (1/sprint)
        
        Here we show new features and request approve for testing and deploy;
        
- All days have “daily meeting”, and must end in 15 minutes;
- All meetings described in this document must delivery a document, containing all topics discussed.
    - For be better and don’t overload team, each meeting one take notes and produce documents;
    - Must be uploaded in our company system for documentation;
    - Must contain participants;
    - Need to follow a template;
    - List of documents and name format, and the total produced in the month:
        - `Dally meet DD/MM/YYYY` 18-20x
        - `Sprint planning meet [sprint_id]` 2x
        - `Sprint  review meet [sprint_id]` 2x
        - `Product review meet [product_id] DD/MM/YYYY` 2x / product
        - `Product definition meet [product_id] DD/MM/YYYY` 1x / product
- All minor releases in production gonna be programmed, taking into consideration important dates for clients (e.g. BlackFriday, Company’s Anniversary Day, Christmas).
- Development and testing cycle (1 cycle = 1 sprint)
    - It gonna have 3 distinct cycles: decisions cycle, development cycle, and test cycle;
    - All 3 cycles occur in parallel;
    - I gonna give you a example of the first 90 days of a new product workflow, and you describe it for me:
        - Day 0-14
            - Decision cycle for sprint 1 and 2 (release v1)
            - No client review
            - No development
            - No testing
            - No deploy
        - Day 15-30
            - No decision
            - No client review
            - Development cycle of sprint 1 (release v1)
            - No testing
            - No deploy
        - Day 31-45
            - Decision cycle for sprint 3 and 4 (release v2)
            - Client review of delivery in sprint 1
            - Development cycle of sprint 2 (release v1)
            - No testing
            - No deploy
        - Day 46-60
            - No decision
            - Client review of delivery in sprint 2
            - Development cycle of sprint 3 (release v2)
            - Testing cycle of release v1
            - No deploy
        - Day 61-75
            - Decision cycle for sprint 5 and 6 (release v3)
            - Client review of delivery in sprint 3
            - Development cycle of sprint 4 (release v2)
            - No testing
            - Deploy release v1
        - Day 76-90
            - No decision
            - Client review of delivery in sprint 4
            - Development cycle of sprint 5 (release v3)
            - No testing
            - No deploy
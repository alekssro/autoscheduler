# App Requirements

The app will be able to generate a good schedule for the given entities, given a set of constrains.

## Minimum Viable Product

- Import entities from a csv with the following structure:
  - rows: entities
  - columns: constrains (values [0, 1])
- Output a suitable schedule given entities and constrains
- Output a score for the given schedule
- Export the schedule for the entities to a csv
- Addition of new entities
- Addition of new constrains
- Specify minimum threshold
- Notify constrains violation

## Minimum Lovable Product

- Import via Web UI
- Add entities via Web UI
- Add constrains via Web UI
- Show results via Web UI
- Download results via Web UI
- Import information from other sources
  - Google Calendar
  - ical
  - ...
- Export information to other services
  - Google Calendar
  - ical
  - ...

------------------------

Based on these requirements, the structure of the project will be the following:

```
docs/
src/
    autoschedule.py
    calculate.py
    helpers.py
    data/
        import.py
        export.py
    db/
        entities.py
        constrains.py    
    calculate/
        RL/
            agent.py
            environment.py
    checks/
        constrain_violation.py
tests/
    test_autoschedule.py
    test_calculate.py
    test_helpers.py
    data/
        test_import.py
        test_export.py
    db/
        test_entities.py
        test_constrains.py
    calculate/
        RL/
            test_agent.py
            test_environment.py
    checks/
        test_constrain_violation.py

Dockerfile
```
# Home Assistant Blueprints

Reusable automation blueprints for [Home Assistant](https://www.home-assistant.io/).

## Light/Switch Scheduler

Schedule one or more lights or switches using fixed times, sunrise, sunset, and
selected days of the week.

### Features

- Control multiple light and switch entities together.
- Set independent fixed times for turning entities on and off.
- Turn entities on or off at sunrise or sunset.
- Apply an optional 15-minute delay after sunrise or sunset.
- Choose which days of the week the automation runs.
- Enable only the scheduling methods you need.

## Installation

### Import into Home Assistant

[![Open your Home Assistant instance and import this blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FvMoff%2Fhome-assistant-blueprints%2Fmain%2Flight-or-switch-scheduler.yaml)

Alternatively:

1. Open **Settings → Automations & scenes → Blueprints** in Home Assistant.
2. Select **Import Blueprint**.
3. Paste this URL:

   ```text
   https://raw.githubusercontent.com/vMoff/home-assistant-blueprints/main/light-or-switch-scheduler.yaml
   ```

4. Preview and import the blueprint.
5. Select **Create automation**, configure the schedule, and save it.

### Manual installation

Download `light-or-switch-scheduler.yaml` and place it at:

```text
/config/blueprints/automation/vMoff/light-or-switch-scheduler.yaml
```

Reload your automations, then create a new automation from the imported blueprint.

## Configuration

| Setting | Description |
| --- | --- |
| Lights or Switches | One or more `light` or `switch` entities to control. |
| Enable Turn ON Time | Enables the fixed turn-on schedule. |
| Turn ON Time | Fixed time at which the selected entities turn on. |
| Enable Turn OFF Time | Enables the fixed turn-off schedule. |
| Turn OFF Time | Fixed time at which the selected entities turn off. |
| Enable Sunrise Trigger | Enables the selected sunrise action. |
| Sunrise Trigger | Turns entities on or off at sunrise or 15 minutes afterward. |
| Enable Sunset Trigger | Enables the selected sunset action. |
| Sunset Trigger | Turns entities on or off at sunset or 15 minutes afterward. |
| Active Days | Days of the week on which the automation may run. |

## Example schedules

- Turn outdoor lights on 15 minutes after sunset and off at 11:00 PM.
- Run decorative lighting only on Friday and Saturday.
- Turn a device off at sunrise every day.
- Apply the same schedule to several lights and switches.

## Notes

- Fixed times are ignored unless their corresponding enable options are turned on.
- Sunrise and sunset selections are ignored unless their corresponding triggers are enabled.
- The active-day selection applies to fixed-time, sunrise, and sunset triggers.
- Sunrise and sunset behavior depends on the location and time-zone settings of your Home Assistant instance.

# Heading

## 1. Numbering + Heading
Lorem Ipsum

## 2. Numbering + Heading
Lorem Ipsum

## 3. Numbering + Heading
Lorem Ipsum

### 3.1 Numbering + Deeper Heading
Lorem Ipsum
![Missing Diagram](./images/does-not-exist.png){ height=300 }

## 4. Long List (structure/length trigger)
- Item 01: Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
- Item 02: Aenean commodo ligula eget dolor. Aenean massa.
- Item 03: Cum sociis natoque penatibus et magnis dis parturient montes.
- Item 04: Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem.
- Item 05: Nulla consequat massa quis enim.
- Item 06: Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu.
- Item 07: In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo.
- Item 08: Nullam dictum felis eu pede mollis pretium.
- Item 09: Integer tincidunt. Cras dapibus.
- Item 10: Vivamus elementum semper nisi.
- Item 11: Aenean vulputate eleifend tellus.
- Item 12: Aenean leo ligula, porttitor eu, consequat vitae, eleifend ac, enim.

## 5. Table (parser boundary trigger)
| State            | App Display           | Notes                                 |
|------------------|-----------------------|----------------------------------------|
| NotPaired        | Pair New              | Initial onboarding                      |
| Pairing          | Searching to pair     | BLE discovery                           |
| InSession        | Sensor Warmup         | Requires timers                         |
| SessionActive    | Readings              | Normal operation                        |
| SessionExpired   | Expired               | Block UX until re-pair                  |

## 6. Code Fence (another boundary trigger)
```json
{
  "component": "sensor-comm",
  "txState": ["NotPaired", "Pairing", "InSession", "SessionActive", "SessionExpired"],
  "notes": "Large fenced blocks sometimes expose truncation when combined with images and tables."
}

## 7. Numbering + Heading
Lorem Ipsum

## 8. Numbering + Heading
Lorem Ipsum

## 9. Numbering + Heading
Lorem Ipsum

## 10. Numbering + Heading
Lorem Ipsum

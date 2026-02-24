# :test_tube: Manual Test Script — E-vini IA (Evino Digital Sommelier)

## Objective
Validate the conversational wine recommendation flow including:

Menu interaction
Voice & text input
Product recommendations
Filters/refinement (ex.: Mais opções, Vinhos brancos)
Cart management
Checkout redirection to Evino
Continue chatting after cart


---

## Preconditions

Internet connection
Microphone permission enabled (for voice tests)
Empty cart (when applicable)
Supported browser (Safari iOS / Chrome Android / Chrome Desktop)


---

## Test Scenarios

### 1) Initial Chat & Menu

| ID | Test | Steps | Expected |
|----|------|-------|----------|
| CT-001 | Load page | Open E-vini IA URL | Welcome message + menu options visible |
| CT-002 | Select each menu option | Tap each menu item one by one | Bot replies with relevant recommendations |
| CT-003 | Send typed message | Type “Quero um vinho branco leve” and send | Bot suggests relevant wines |

---

### 2) Voice Interaction

| ID | Test | Steps | Expected |
|----|------|-------|----------|
| CT-004 | Microphone permission | Tap mic icon and allow | Recording starts / UI shows listening state |
| CT-005 | Speak a menu intent | Speak “Vinho para churrasco” and send | Bot returns barbecue-friendly recommendations |
| CT-006 | Deny mic permission | Deny access and tap mic again | Guidance shown and no crash; typing still works |

---

### 3) Product Recommendations (Cards)

| ID | Test | Steps | Expected |
|----|------|-------|----------|
| CT-007 | Show product cards | Select “Destaques de Portugal” | Cards show name, tags (grape/country), price and “+” |
| CT-008 | Validate card UI | Check 3 cards | Layout consistent, readable, CTA clickable |
| CT-009 | Scroll list | Scroll products area | List scroll works; more items load if applicable |

---

### 4) Refinement Options (Chips/Buttons)

| ID | Test | Steps | Expected |
|----|------|-------|----------|
| CT-010 | More options | Tap “Mais opções” | More wine cards are shown (not only duplicates) |
| CT-011 | Filter white wines | Tap “Vinhos brancos” | Results prioritize/filter to white wines |
| CT-012 | Switch refinements | Tap “Vinhos brancos” then “Mais opções” | Context preserved + more options within the same context |

---

### 5) Cart Flow

| ID | Test | Steps | Expected |
|----|------|-------|----------|
| CT-013 | Add to cart | Tap “+” on a product | Cart count updates (ex.: (1)) |
| CT-014 | Open cart | Open cart modal | Item listed with name, price, quantity controls |
| CT-015 | Change quantity | Use “+” and “-” | Quantity and total update correctly |
| CT-016 | Remove item | Tap “X” remove | Item removed; cart updates state |
| CT-017 | Close cart | Close cart modal | Returns to chat without losing context |

---

### 6) Continue vs Checkout

| ID | Test | Steps | Expected |
|----|------|-------|----------|
| CT-018 | Continue chatting | In cart, tap “Continuar conversando” | Modal closes and chat keeps working |
| CT-019 | Checkout redirection | Tap “Finalizar Compra na Evino” | Opens Evino checkout/app correctly |
| CT-020 | Return to chat | Navigate back to chat after checkout | Chat still accessible; cart state consistent |

---

### 7) Edge Cases / Resilience

| ID | Test | Steps | Expected |
|----|------|-------|----------|
| CT-021 | Empty message | Try sending with no text | Send blocked or no action; no error |
| CT-022 | Offline during response | Send message, disable internet, re-enable | Friendly error and recovery option |
| CT-023 | Very long text | Paste and send long text | UI doesn’t break; limit handled gracefully |
| CT-024 | Basic accessibility | Increase OS font / zoom | Layout remains usable; controls accessible |

---

## Evidence

Screenshots & screen recordings
Device / OS / Browser version
Date/time
Expected vs Actual (for failures)
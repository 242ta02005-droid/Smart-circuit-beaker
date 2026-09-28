# Smart-circuit-beaker
# Smart Circuit Breaker

MAX_CURRENT = 10
MIN_VOLTAGE = 200
MAX_VOLTAGE = 250
MAX_TEMPERATURE = 70

print("==============================")
print("       SMART CIRCUIT BREAKER")
print("==============================")

voltage = float(input("Enter voltage (V): "))
current = float(input("Enter current (A): "))
temperature = float(input("Enter temperature (°C): "))

trip = False

# Voltage protection
if voltage < MIN_VOLTAGE:
    print("⚠️ Under-voltage detected")
    trip = True

elif voltage > MAX_VOLTAGE:
    print("⚠️ Over-voltage detected")
    trip = True

# Current protection
if current > MAX_CURRENT:
    print("⚠️ Overcurrent detected")
    trip = True

# Temperature protection
if temperature > MAX_TEMPERATURE:
    print("⚠️ High temperature detected")
    trip = True

# Circuit breaker operation
if trip:
    print("\n🔴 FAULT DETECTED")
    print("⚡ SMART CIRCUIT BREAKER: TRIPPED")
    print("🔌 Load disconnected")
else:
    print("\n🟢 SYSTEM NORMAL")
    print("⚡ SMART CIRCUIT BREAKER: ON")
    print("✅ Load connected")

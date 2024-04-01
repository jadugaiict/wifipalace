# wifipalace
IT
class WiFiNetwork:
    def __init__(self, ssid, password):
        self.ssid = ssid
        self.password = password

class WiFiPalace:
    def __init__(self):
        self.networks = []

    def add_network(self, ssid, password):
        self.networks.append(WiFiNetwork(ssid, password))

    def list_networks(self):
        if self.networks:
            print("Available Networks:")
            for i, network in enumerate(self.networks):
                print(f"{i + 1}. {network.ssid}")
        else:
            print("No networks available.")

    def connect_to_network(self, index):
        if 0 <= index < len(self.networks):
            print(f"Connecting to {self.networks[index].ssid}...")
            # Code to connect to the WiFi network would go here
            print("Connected successfully!")
        else:
            print("Invalid network index.")

    def disconnect(self):
        print("Disconnecting...")
        # Code to disconnect from the WiFi network would go here
        print("Disconnected successfully!")

# Example Usage
wifi_palace = WiFiPalace()
wifi_palace.add_network("WiFi1", "password1")
wifi_palace.add_network("WiFi2", "password2")

while True:
    print("\nMenu:")
    print("1. List available networks")
    print("2. Connect to a network")
    print("3. Disconnect")
    print("4. Exit")
    choice = input("Enter your choice: ")

    if choice == '1':
        wifi_palace.list_networks()
    elif choice == '2':
        wifi_palace.list_networks()
        index = int(input("Enter the index of the network you want to connect to: ")) - 1
        wifi_palace.connect_to_network(index)
    elif choice == '3':
        wifi_palace.disconnect()
    elif choice == '4':
        print("Exiting...")
        break
    else:
        print("Invalid choice. Please try again.")

        <a href="http://cctvinstallationsdubai.com">Visit CCTV Installations Dubai</a>


# Outfit-Designer-App
A JavaFX-based GUI application that helps users design outfits based on available wardrobe items, weather conditions, or personal style
classDiagram
    class OutfitDesignerApp {
        +main()
    }

    class User {
        +String name
        +List<ClothingItem> wardrobe
        +addClothingItem()
        +getOutfitSuggestion()
    }

    class ClothingItem {
        +String type
        +String color
        +String material
        +String category
        +displayInfo()
    }

    class Outfit {
        +List<ClothingItem> items
        +String occasion
        +displayOutfit()
    }

    class StyleEngine {
        +generateOutfit()
        +matchColors()
        +suggestByOccasion()
    }

    class GUIManager {
        +displayInterface()
        +handleUserInput()
    }

    class WeatherService {
        +getWeatherData()
        +suggestWeatherOutfit()
    }

    OutfitDesignerApp --> User
    User --> ClothingItem
    User --> Outfit
    Outfit --> ClothingItem
    OutfitDesignerApp --> GUIManager
    OutfitDesignerApp --> StyleEngine
    StyleEngine --> Outfit
    StyleEngine --> ClothingItem
    OutfitDesignerApp --> WeatherService
    WeatherService --> Outfit
    ![UML Diagram](https://mermaid.ink/img/pako:eNqNVNtKxDAQ_ZWSJ0X9gUUW1BVZUHwoiyB9GZNpGkiTkkyVIvvvZpuq6U3MQ2nnnMzlzHQ-GbcC2YZxDd7vFEgHdWGycHpL9txSqWiHXkmD7qZpss8In85FDcqcnUfDsTDpxYNHN-Lm5JSRmYEaE-uj8nR9py1VAdwT1tvsA5xw9i1lgRAp5ztkj0mkmGTeSomelF1LKXWxlBp1Dc6t3Grr5uYaCJ0CvXAhINK6LkGE8o2Gbm9Ku5JbLGGU1YI0Kjz9PKLlHHyoex4xul2JmVOn8d5IZXAUWGJodShifHloOPHq7qSIH9l91P62ex5SWQn5cNg_gQE5mY0ffYKmJXAc-a7ACI2nedqbpl0r5gWBKnQ5unfFp_XQgO6AYCnvAV5Ra_4PXF1t-wGPeD_qJ1ParAkUfaT-Vm4sB_vV7S9W0t
![diagram app](https://github.com/user-attachments/assets/f3ece542-9bad-44eb-81bd-0ae061d9c464)

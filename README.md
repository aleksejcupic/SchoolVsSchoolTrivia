Final Project for iOS app development at Boston College
## GuessKing - iOS Game

**GuessKing** is a hybrid of **Hangman** and **Wordle**, designed for iOS using **Swift**. The game connects to an external API to fetch random words for players to guess, while storing user data and game progress using **Firebase** for persistent and personalized gameplay.

### Features
- **Word Guessing Game**: Combines gameplay elements from both Hangman and Wordle.
  - Players guess letters to reveal a hidden word.
  - The game provides feedback on correct and incorrect guesses, as well as their location (index).
- **Word Fetching API**: The game uses a third-party API to fetch random 5-letter words, ensuring a new and challenging experience every time.
- **Firebase Integration**: User data (e.g., game progress, scores) is stored and managed through **Firebase**, enabling persistent data and the ability to resume games.
- **User Accounts**: Users can sign up, log in, and track their progress across multiple sessions.

### Installation

#### Prerequisites
- Xcode (latest version recommended)
- CocoaPods (for managing Firebase dependencies)
- Firebase account with a configured Firebase project

#### Clone the Repository
```bash
git clone https://github.com/aleksejcupic/GuessKing.git
```

#### Install Dependencies
Navigate to the project directory and install the necessary pods for Firebase:
```bash
cd GuessKing
pod install
```

#### Firebase Setup
1. Create a new project in [Firebase Console](https://console.firebase.google.com/).
2. Set up **Authentication** (Email/Password).
3. Set up **Realtime Database** or **Firestore** (whichever you're using).
4. Download the `GoogleService-Info.plist` file and add it to the root of your Xcode project.
5. Ensure Firebase SDK is integrated by adding Firebase dependencies via CocoaPods.

Example `Podfile`:
```ruby
pod 'Firebase/Core'
pod 'Firebase/Auth'
pod 'Firebase/Database'  # Or Firestore, depending on which database you're using
```

#### Run the App
Open the `GuessKing.xcworkspace` in Xcode and run the project on a simulator or a connected iOS device.

### How to Play
1. **Sign up / Log in**: Create a user account to start playing. Your progress and scores will be saved in Firebase.
2. **Guess the Word**: The game will fetch a random word from the API. Start guessing letters!
3. **Feedback**: Correct guesses reveal the letter in the word, while incorrect guesses count towards your allowed attempts (similar to Hangman).
4. **Win/Lose**: You win if you guess the word correctly within the allowed attempts, and lose if you run out of chances.

### Technologies Used
- **Swift**: Main language for developing the iOS app.
- **Firebase**: Backend as a service for user authentication and data storage.
- **API Integration**: Random word generation via an external API.
- **CocoaPods**: For managing external dependencies (like Firebase).

### Future Enhancements
- Implement multiplayer mode for users to challenge each other.
- Add additional word categories for more diverse challenges.
- Improve the UI with animations and sound effects.

---
*Repo used to be called SchoolVsSchoolTrivia*
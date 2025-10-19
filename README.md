# 🎮 Simon Dice - Memory Game

A modern web-based implementation of the classic Simon Says memory game, enhanced with adaptive difficulty, scoring system, themes, and achievements.

## 🎯 What is Simon Dice?

Simon Dice is a memory training game where players must memorize and repeat sequences of keyboard keys that get progressively longer and more challenging. It's based on the classic Simon electronic game but uses keyboard input instead of colored buttons.

## ✨ Features

### 🧠 **Adaptive Difficulty System**

- **4 Difficulty Phases**:
  - **Aprendiendo** (Levels 1-5): Easy vowels only, slow speed, audio cues
  - **Construyendo** (Levels 6-10): Full alphabet, normal speed, audio cues
  - **Desafiante** (Levels 11-15): Numbers + letters, faster speed, no audio
  - **Experto** (Levels 16+): Maximum difficulty, very fast, no audio

### 🎨 **Theme System**

- **5 Beautiful Themes**:
  - 🌙 **Dark**: Classic black and white
  - ⚡ **Neon**: Cyberpunk cyan and magenta
  - 🌊 **Ocean**: Deep blue ocean vibes
  - 🌅 **Sunset**: Warm orange and yellow tones
  - 🌲 **Forest**: Natural green forest theme

### 🎹 **Customizable Key Sets**

- **AEIOU**: Only vowels (easier)
- **A-Z**: Full alphabet (standard)
- **0-9**: Only numbers (challenging)
- **A-Z + 0-9**: Mixed alphanumeric (expert)

### 🏆 **Scoring & Progression**

- **Speed-Based Scoring**: Faster completion = more points
- **Streak Bonuses**: Consecutive correct sequences earn bonus points
- **High Score Tracking**: Persistent local storage for personal bests
- **Achievement System**: 12 unlockable achievements

### 🎵 **Audio Feedback**

- **Key Sounds**: Different tones for each key
- **Success/Failure Sounds**: Audio confirmation
- **Phase-Based Audio**: Enabled/disabled based on difficulty

### 🎭 **Visual Polish**

- **Smooth Animations**: Professional keyframe animations
- **Glow Effects**: Dynamic shadows and glowing borders
- **Floating Points**: Animated point notifications
- **Theme Integration**: All elements adapt to current theme

## 🚀 How to Play

1. **Open** `index.html` in your web browser
2. **Choose** your preferred theme and key set using the controls in the top-left
3. **Watch** the sequence of keys light up
4. **Repeat** the sequence by pressing the same keys in order
5. **Progress** through levels as sequences get longer and faster
6. **Earn** points for speed and accuracy
7. **Unlock** achievements as you improve

## 🎮 Game Controls

- **Keyboard**: Press the keys that light up in the sequence
- **Theme Selector**: Click theme buttons to change appearance
- **Key Customizer**: Choose your preferred key set
- **Score Display**: View current score, streak, and achievements
- **High Score Panel**: See your personal bests

## 📊 Scoring System

### **Point Calculation**:

```
Base Points = (Level + 1) × 100
Speed Bonus = max(0, 1000 - timeTaken) ÷ 10
Streak Bonus = currentStreak × 50
Difficulty Multiplier = 1.0-2.0 based on phase
Final Score = (Base + Speed + Streak) × Multiplier
```

### **Example Scoring**:

- **Level 5, 500ms, Streak 3**: (6×100 + 50 + 150) × 1.0 = **800 points**
- **Level 15, 200ms, Streak 10**: (16×100 + 80 + 500) × 2.0 = **4,360 points**

## 🏅 Achievements

### **Score Achievements**:

- **Primer Mil** - Reach 1,000 points
- **Club de los 5K** - Reach 5,000 points
- **Maestro de los 10K** - Reach 10,000 points

### **Streak Achievements**:

- **Iniciador de Racha** - Streak of 5
- **Maestro de Rachas** - Streak of 10
- **Leyenda de Rachas** - Streak of 20

### **Level Achievements**:

- **Nivel Cinco** - Reach level 5
- **Nivel Diez** - Reach level 10
- **Nivel Quince** - Reach level 15

## 🛠️ Technical Details

### **Technologies Used**:

- **HTML5**: Semantic markup and structure
- **CSS3**: Advanced styling with CSS variables and animations
- **JavaScript ES6+**: Modern JavaScript with classes and modules
- **SweetAlert**: Beautiful alert dialogs
- **Local Storage**: Persistent data storage

### **Browser Compatibility**:

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

### **File Structure**:

```
simondice/
├── index.html          # Main game file
├── simon.css           # Game styles and themes
├── sweetalert.css      # Alert dialog styles
├── sweetalert.min.js   # Alert dialog library
└── README.md           # This file
```

## 🎯 Game Tips

1. **Start Easy**: Begin with vowels only to learn the basics
2. **Use Audio**: Listen to the key sounds in early levels
3. **Build Streaks**: Maintain consecutive correct sequences for bonus points
4. **Practice Speed**: Faster completion earns more points
5. **Choose Themes**: Find a theme that's comfortable for your eyes
6. **Customize Keys**: Select key sets that match your skill level

## 🔧 Customization

### **Adding New Themes**:

1. Add new CSS variables in `simon.css`
2. Create theme class with color definitions
3. Add theme button in HTML

### **Adding New Achievements**:

1. Add achievement check in `ScoreManager.checkAchievements()`
2. Define achievement name and description
3. Set trigger conditions

### **Modifying Difficulty**:

1. Adjust phase definitions in `DifficultyManager`
2. Modify key sets in `getKeySetForComplexity()`
3. Change timing in `playbackSpeed` values

## 📱 Mobile Support

The game is designed for desktop keyboard input but can be adapted for mobile:

- Touch events can replace keyboard events
- Responsive design adapts to different screen sizes
- Theme system works across all devices

## 🤝 Contributing

Feel free to contribute to this project by:

- Adding new themes
- Creating additional achievements
- Improving accessibility
- Adding new game modes
- Enhancing visual effects

## 📄 License

This project is open source and available under the MIT License.

## 🎉 Enjoy Playing!

Have fun training your memory with Simon Dice! Challenge yourself to beat your high scores and unlock all achievements. The game is designed to be both entertaining and educational, helping improve your memory and reaction time.

---

**Made with ❤️ for memory training enthusiasts**

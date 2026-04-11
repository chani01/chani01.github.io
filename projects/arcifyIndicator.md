# ArcifyCircleIndicator

**ArcifyCircleIndicator** is a customizable circular progress indicator library for Android Jetpack Compose. It provides flexible and animated arc-shaped progress bars with various configuration options to enhance your application's user interface.

## Features

### Progress Modes
- **Manual**: Allows manual control of the progress value
- **Auto**: Automatically progresses at a specified interval with infinite loop
- **TimeBased**: Automatically progresses based on a specified duration with smooth real-time updates

### Customization Options
- **Color**: Set the color of the progress arc
- **Background Color**: Define the color of the unprogressed background arc
- **Stroke Width**: Adjust the thickness of the progress bar
- **Stroke Cap**: Choose the shape of the ends of the progress bar (Butt or Round)
- **Progress Direction**: Select the direction of progress (CLOCKWISE or COUNTERCLOCKWISE)
- **Animation Specification**: Configure the animation's duration and easing
- **Center Content**: Insert custom composable content at the center of the indicator
- **Progress Change Callback**: Receive callbacks when the progress value changes

### Additional Components
- **ArcifyInfiniteIndicator**: Infinite rotating progress indicator for loading states

## Installation

### 1. Add JitPack repository
```gradle
dependencyResolutionManagement {
    repositories {
        maven { url = uri("https://jitpack.io") }
    }
}
```

### 2. Add dependency
```gradle
dependencies {
    implementation "com.github.chani01:ArcifyIndicator:<latest_version>"
}
```

## Usage

### Manual Progress Mode

Control the progress value manually:

```kotlin
ArcifyCircleIndicator(
    modifier = Modifier.size(200.dp),
    progressState = ArcifyProgressState.Manual(progress = 0.75f),
    color = Color.Blue,
    backgroundColor = Color.Gray,
    strokeWidth = 8.dp,
    strokeCap = StrokeCap.Round,
    progressDirection = ArcifyProgressDirection.CLOCKWISE
)
```

### Auto Progress Mode

Automatically progress with a specified delay interval:

```kotlin
ArcifyCircleIndicator(
    modifier = Modifier.size(200.dp),
    progressState = ArcifyProgressState.Auto(autoProgressDelay = 3000L), // 3 seconds
    color = Color.Green,
    backgroundColor = Color.LightGray,
    strokeWidth = 8.dp,
    animationSpec = tween(
        durationMillis = 1000,
        easing = LinearEasing
    )
)
```

> **Note**: The `autoProgressDelay` parameter has a minimum value of 1ms to prevent crashes. If you pass 0, it will automatically be adjusted to 1ms.

### TimeBased Progress Mode

Automatically progress based on a specified duration with real-time updates:

```kotlin
var animatedProgress by remember { mutableFloatStateOf(0f) }

ArcifyCircleIndicator(
    modifier = Modifier.size(200.dp),
    progressState = ArcifyProgressState.TimeBased(duration = 5000L), // 5 seconds
    color = MaterialTheme.colorScheme.primary,
    strokeWidth = 8.dp,
    strokeCap = StrokeCap.Round,
    animationSpec = tween(
        durationMillis = 50,
        easing = LinearEasing
    ),
    centerContent = {
        Text("${(animatedProgress * 100).toInt()}%")
    },
    onProgressChanged = { animatedProgress = it }
)
```

### Center Content and Progress Change Callback

Display custom content at the center and receive progress updates:

```kotlin
var currentProgress by remember { mutableFloatStateOf(0f) }

ArcifyCircleIndicator(
    modifier = Modifier.size(150.dp),
    progressState = ArcifyProgressState.Manual(progress = 0.5f),
    color = Color.Red,
    strokeWidth = 10.dp,
    centerContent = {
        Text(
            text = "${(currentProgress * 100).toInt()}%",
            style = MaterialTheme.typography.headlineMedium
        )
    },
    onProgressChanged = { progress ->
        currentProgress = progress
    }
)
```

### Infinite Progress Indicator

For loading states with infinite rotating animation:

```kotlin
ArcifyInfiniteIndicator(
    modifier = Modifier.size(100.dp),
    color = MaterialTheme.colorScheme.primary.copy(alpha = 0.8f),
    backgroundColor = MaterialTheme.colorScheme.onSurface.copy(alpha = 0.2f),
    strokeWidth = 6.dp,
    strokeCap = StrokeCap.Round,
    progressDirection = ArcifyProgressDirection.CLOCKWISE,
    animationDuration = 1000,
    centerContent = {
        Text(text = "Loading...", style = MaterialTheme.typography.bodyMedium)
    }
)
```

## API Reference

### ArcifyCircleIndicator

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `modifier` | `Modifier` | `Modifier` | Configure the size and layout |
| `progressState` | `ArcifyProgressState` | `Manual(0f)` | Defines the progress state and mode |
| `color` | `Color` | `primary.copy(0.8f)` | Color of the progress arc |
| `backgroundColor` | `Color` | `onSurface.copy(0.2f)` | Color of the background arc |
| `strokeWidth` | `Dp` | `6.dp` | Thickness of the progress bar |
| `strokeCap` | `StrokeCap` | `Round` | Shape of the line ends |
| `progressDirection` | `ArcifyProgressDirection` | `CLOCKWISE` | Direction of progress |
| `animationSpec` | `AnimationSpec<Float>?` | `tween(1000)` | Animation configuration |
| `centerContent` | `@Composable (() -> Unit)?` | `null` | Custom center content |
| `onProgressChanged` | `((Float) -> Unit)?` | `null` | Progress change callback |

### ArcifyProgressState

- **`Manual(progress: Float)`**: Manual progress control (0.0 to 1.0)
- **`Auto(autoProgressDelay: Long = 500L)`**: Automatic progress with delay interval (minimum 1ms)
- **`TimeBased(duration: Long = 5000L)`**: Time-based automatic progress with specified duration

### ArcifyProgressDirection

- **`CLOCKWISE`**: Progress proceeds clockwise (to the right)
- **`COUNTERCLOCKWISE`**: Progress proceeds counterclockwise (to the left)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributions

Contributions are welcome! Feel free to open issues, submit pull requests, or suggest new features.

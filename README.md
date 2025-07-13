# 42_fdf

A 3D wireframe visualization project that transforms height maps into interactive 3D models, created as part of the 42 School curriculum.

## 📖 About

**FdF** (Fil de Fer - French for "wireframe") takes height map data and renders it as a 3D wireframe model using computer graphics concepts including coordinate transformations, perspective projection, and line drawing algorithms.

## 🚀 Features

- **3D Wireframe Rendering**: Transform 2D height maps into 3D wireframe models
- **Interactive Controls**: Rotate, translate, and zoom in real-time
- **Multiple Projections**: Isometric and perspective projections
- **Color Gradients**: Height-based color mapping
- **Optimized Rendering**: Efficient line drawing using Bresenham's algorithm

## 🔧 Build Instructions

### Prerequisites

- GCC compiler, Make
- MinilibX graphics library (included)
- libft library (included)

### Compilation

```bash
make                # Build the project
make clean         # Clean object files
make fclean        # Clean everything
make re            # Rebuild everything
```

## 📝 Usage

```bash
# Render a height map
./fdf test_maps/42.fdf
./fdf test_maps/pyramide.fdf
./fdf test_maps/julia.fdf
```

### Controls

- **Arrow Keys**: Translate the model
- **Mouse**: Rotate the model
- **+/-**: Zoom in/out
- **R**: Reset view
- **P**: Toggle projection mode
- **ESC**: Exit

### Map Format

```
0  0  0  0  0
0 10 10 10  0
0 10 20 10  0
0 10 10 10  0
0  0  0  0  0
```

## 🔍 Implementation Details

### 3D Transformations

- **Translation**: Moving the model in 3D space
- **Rotation**: Rotating around X, Y, and Z axes
- **Scaling**: Uniform and non-uniform scaling
- **Projection**: Converting 3D coordinates to 2D screen coordinates

### Projection Systems

- **Isometric**: Maintains parallel lines, no perspective distortion
- **Perspective**: Realistic depth perception with vanishing points

### Line Drawing

Uses Bresenham's algorithm for efficient pixel-perfect line drawing.

### Color System

Height-based color mapping: low heights (blue/cyan) → medium heights (green/yellow) → high heights (red/white).

## 🧪 Testing

Sample maps included: 42.fdf, pyramide.fdf, julia.fdf, elem.fdf, pentenegpos.fdf

Create custom maps:

```bash
echo "0 0 0 0 0
0 1 1 1 0
0 1 2 1 0
0 1 1 1 0
0 0 0 0 0" > my_map.fdf

./fdf my_map.fdf
```

## 🔗 Dependencies

- **libft**: Custom C library for basic functions
- **MinilibX**: Graphics library for window management and rendering
- **Math Library**: Mathematical functions for transformations

---

_Computer graphics programming project demonstrating 3D transformations, projections, and real-time rendering techniques._

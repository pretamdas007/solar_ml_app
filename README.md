# 🌞 Solar Flare Analysis ML Application

A production-ready machine learning application for analyzing GOES/EXIS satellite data to detect, separate, and analyze solar flares with special focus on nanoflare identification.

![Solar Flare Analysis](https://img.shields.io/badge/License-MIT-blue.svg)
![Next.js](https://img.shields.io/badge/Next.js-15.3.3-black)
![React](https://img.shields.io/badge/React-19.0.0-blue)
![Python](https://img.shields.io/badge/Python-3.8+-yellow)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-blue)

## 🌟 Features

- **🤖 ML-Powered Flare Detection**: Advanced machine learning algorithms to separate overlapping solar flares
- **🔬 Nanoflare Identification**: Automatic detection of nanoflares with |α| > 2 for coronal heating studies
- **📊 Interactive Dashboard**: Modern React-based frontend with real-time visualization
- **📈 Statistical Analysis**: Comprehensive power-law analysis and energy distribution studies
- **🚀 Production Ready**: Full-stack deployment with Node.js backend and Python ML integration
- **⚡ Real-time Processing**: Live data analysis with WebSocket support
- **🎯 Bayesian Uncertainty**: Advanced uncertainty quantification for predictions

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Next.js 15    │    │   Python ML     │    │   GOES/EXIS     │
│   Frontend      │◄──►│   Backend       │◄──►│   Satellite     │
│                 │    │                 │    │   Data          │
│ • React 19      │    │ • TensorFlow    │    │                 │
│ • TypeScript    │    │ • Scikit-learn  │    │ • NetCDF4       │
│ • Tailwind CSS  │    │ • Flask API     │    │ • X-ray Flux    │
│ • Recharts      │    │ • NumPy/SciPy   │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🚀 Technologies

### Frontend
- **Next.js 15** - React framework with App Router and Turbopack
- **React 19** - Modern UI components with concurrent features
- **TypeScript** - Type-safe development
- **Tailwind CSS 4** - Utility-first CSS framework
- **Recharts** - Interactive data visualization
- **Lucide React** - Beautiful icons

### Backend
- **Python 3.8+** - Core ML processing
- **Flask** - API server for ML model serving
- **TensorFlow/PyTorch** - Deep learning frameworks
- **Scikit-learn** - Traditional ML algorithms
- **NumPy/SciPy** - Scientific computing
- **Pandas** - Data manipulation
- **NetCDF4** - GOES satellite data processing

### Data Processing
- **GOES/EXIS Satellite Data** - Real-time solar X-ray flux
- **Power-law Analysis** - Energy distribution modeling
- **Bayesian Neural Networks** - Uncertainty quantification
- **Monte Carlo Methods** - Statistical validation

## 📋 Prerequisites

- **Node.js** 18+ 
- **Python** 3.8+
- **Git**

## 🛠️ Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/solar-flare-ml-app.git
cd solar-flare-ml-app
```

### 2. Install Frontend Dependencies

```bash
npm install
```

### 3. Set up Python Environment

```bash
# Create virtual environment
python -m venv .venv

# Activate virtual environment
# On Windows:
.venv\Scripts\activate
# On macOS/Linux:
source .venv/bin/activate

# Install Python dependencies
pip install -r requirements.txt
```

### 4. Environment Configuration

Create a `.env.local` file in the root directory:

```env
PYTHON_API_URL=http://localhost:5000
NEXT_PUBLIC_API_URL=http://localhost:3000
```

### 5. Start the Application

**Development Mode:**

```bash
# Start Python backend (Terminal 1)
python python_bridge.py

# Start Next.js frontend (Terminal 2)
npm run dev
```

**Or use the convenience scripts:**

```bash
# Windows
./start_app.bat

# macOS/Linux
./start_app.sh

# PowerShell
./start_app.ps1
```

### 6. Access the Application

- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:5000

## 📊 Application Features

### 🔍 Data Analysis Pipeline
1. **Data Loading** - Import GOES/EXIS satellite data
2. **Flare Detection** - Identify and segment solar flares
3. **Feature Extraction** - Extract physical parameters
4. **ML Prediction** - Classify nanoflares and predict energy distributions
5. **Visualization** - Interactive charts and statistical analysis

### 🎯 ML Models
- **Bayesian Neural Networks** - Uncertainty-aware predictions
- **Random Forest** - Ensemble classification
- **XGBoost** - Gradient boosting for regression
- **Monte Carlo Dropout** - Uncertainty quantification

### 📈 Visualizations
- **Time Series Analysis** - X-ray flux evolution
- **Power-law Distributions** - Energy scaling analysis  
- **Uncertainty Plots** - Prediction confidence intervals
- **Correlation Matrices** - Feature relationships

## 🧪 API Endpoints

### Analysis Endpoints
- `POST /api/analyze` - Run complete analysis pipeline
- `GET /api/analysis/flares` - Get detected flares
- `GET /api/analysis/plots` - Generate visualization plots

### ML Endpoints  
- `POST /api/ml/predict` - Make predictions
- `POST /api/bayesian/train` - Train Bayesian models
- `GET /api/bayesian/uncertainty` - Get uncertainty estimates

### Monte Carlo Endpoints
- `POST /api/montecarlo/simulation` - Run Monte Carlo simulations
- `POST /api/montecarlo/augmentation` - Data augmentation
- `POST /api/montecarlo/cross-validation` - Cross-validation

## 📁 Project Structure
```bash
# Activate your virtual environment first
pip install flask flask-cors tensorflow scikit-learn numpy scipy netcdf4 matplotlib
```

## 📁 Project Structure

```
solar-flare-ml-app/
├── src/                           # Frontend source code
│   ├── app/                       # Next.js App Router
│   │   ├── api/                   # API routes
│   │   │   ├── analyze/          # Main analysis endpoint
│   │   │   ├── bayesian/         # Bayesian ML endpoints
│   │   │   ├── montecarlo/       # Monte Carlo endpoints
│   │   │   └── ml/               # General ML endpoints
│   │   ├── background-removal/   # Background removal page
│   │   ├── comparison/           # Model comparison page
│   │   ├── data-loader/          # Data upload page
│   │   ├── energy-calculation/   # Energy analysis page
│   │   ├── extract-features/     # Feature extraction page
│   │   ├── ml-predictions/       # ML predictions page
│   │   ├── power-law/            # Power law analysis page
│   │   └── train-model/          # Model training page
│   └── components/               # React components
│       ├── ml/                   # ML-specific components
│       ├── Layout.tsx            # App layout
│       ├── NotificationSystem.tsx
│       ├── ResultsVisualization.tsx
│       └── SolarFlareAnalyzer.tsx
├── public/                       # Static assets
├── python_bridge.py             # Python Flask API server
├── enhanced_python_api.py       # Enhanced ML API endpoints
├── package.json                 # Node.js dependencies
├── requirements.txt             # Python dependencies
├── next.config.ts               # Next.js configuration
├── tsconfig.json                # TypeScript configuration
├── tailwind.config.js           # Tailwind CSS configuration
├── start_app.ps1                # PowerShell startup script
├── start_app.sh                 # Bash startup script
├── start_app.bat                # Windows batch startup script
└── README.md                    # This file
```

## 🧪 Development

### Frontend Development

```bash
# Start development server with Turbopack
npm run dev

# Build for production
npm run build

# Start production server
npm start

# Run linting
npm run lint
```

### Backend Development

```bash
# Start Flask development server
python python_bridge.py

# Run with debug mode
python python_bridge.py --debug

# Test API endpoints
python -m pytest tests/
```

## 🔧 Configuration

### Environment Variables

Create `.env.local` in the root directory:

```env
# API Configuration
NEXT_PUBLIC_API_URL=http://localhost:3000
PYTHON_API_URL=http://localhost:5000
FLASK_DEBUG=false

# ML Model Configuration  
MODEL_CACHE_SIZE=100
MAX_DATA_POINTS=1000000
UNCERTAINTY_SAMPLES=100

# Data Processing
MAX_FILE_SIZE=500MB
ALLOWED_EXTENSIONS=.nc,.h5,.fits
DATA_RETENTION_DAYS=30
```

### Model Parameters

The application supports various configurable parameters:

- **Flare Detection Threshold**: Minimum flux increase for flare detection
- **Background Window**: Time window for background calculation
- **Energy Calculation**: Method for flare energy estimation
- **Uncertainty Quantification**: Number of Monte Carlo samples
- **Power-law Fitting**: Fitting algorithm and bounds

## 📊 Data Formats

### Input Data
- **GOES/EXIS NetCDF Files** (`.nc`)
- **HDF5 Files** (`.h5`)
- **FITS Files** (`.fits`)
- **CSV Time Series** (`.csv`)

### Output Data
- **JSON Results** - Complete analysis results
- **CSV Exports** - Flare catalogs and statistics
- **PNG Plots** - Generated visualizations
- **Model Checkpoints** - Trained ML models

## 🚀 Deployment

### Docker Deployment

```bash
# Build container
docker build -t solar-flare-ml-app .

# Run container
docker run -p 3000:3000 -p 5000:5000 solar-flare-ml-app
```

### Production Setup

1. **Environment Setup**
   ```bash
   export NODE_ENV=production
   export PYTHON_ENV=production
   ```

2. **Database Configuration** (if using persistent storage)
   ```bash
   export DATABASE_URL=postgresql://user:pass@localhost/solarflare
   ```

3. **Build and Start**
   ```bash
   npm run build
   npm start &
   python python_bridge.py --port 5000 &
   ```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Make your changes**
4. **Add tests** for new functionality
5. **Run the test suite**
   ```bash
   npm test
   python -m pytest
   ```
6. **Commit your changes**
   ```bash
   git commit -m 'Add amazing feature'
   ```
7. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
8. **Open a Pull Request**

## � License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **GOES/EXIS Team** - For providing excellent satellite data
- **NOAA/NASA** - For making solar data freely available
- **Scientific Community** - For solar flare research foundations
- **Open Source Contributors** - For the amazing tools and libraries

## 📚 References

1. Gryciuk et al. - "Solar Flare Shape-Based Model"
2. GOES/EXIS Documentation - NOAA/NASA
3. Parker Solar Probe Mission - NASA
4. Coronal Heating Problem - Review Articles

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/your-username/solar-flare-ml-app/issues)
- **Discussions**: [GitHub Discussions](https://github.com/your-username/solar-flare-ml-app/discussions)
- **Documentation**: [Wiki](https://github.com/your-username/solar-flare-ml-app/wiki)

---

**Made with ❤️ for Solar Physics Research**
- **Criteria**: Power-law index |α| > 2
- **Purpose**: Corona heating mechanism studies
- **Validation**: Statistical significance testing

### Power Law Analysis
- **Formula**: N(E) ∝ E^(-α)
- **Range**: 10^26 - 10^32 Joules
- **Applications**: Energy budget calculations

## 📁 Project Structure

```
ml_app/
├── src/
│   ├── app/                    # Next.js App Router
│   │   ├── api/               # API routes
│   │   │   ├── analyze/       # Analysis endpoint
│   │   │   └── model/         # Model management
│   │   ├── globals.css        # Global styles
│   │   ├── layout.tsx         # Root layout
│   │   └── page.tsx           # Main dashboard
│   └── components/            # React components
│       ├── SolarFlareAnalyzer.tsx
│       └── NotificationSystem.tsx
├── python_bridge.py           # Python ML API server
├── start_app.ps1             # Windows startup script
└── package.json              # Dependencies
```

## 🧪 Development

### Running Tests
```bash
npm test
```

### Building for Production
```bash
npm run build
npm start
```

### Python Model Development
```bash
python -c "from python_bridge import initialize_model; initialize_model()"
```

## 📈 Performance

- **Analysis Speed**: ~30 seconds for typical GOES day file
- **Memory Usage**: <2GB for full analysis
- **Concurrent Users**: Supports multiple simultaneous analyses
- **Data Size**: Optimized for files up to 100MB

## 🔧 Troubleshooting

### Common Issues

**Port Already in Use:**
```bash
# Kill existing processes
npx kill-port 3000
npx kill-port 5000
```

**Python Dependencies:**
```bash
pip install --upgrade -r requirements.txt
```

**Virtual Environment Issues:**
```bash
# Create new environment
python -m venv goesflareenv
# Activate and install
goesflareenv\Scripts\activate
pip install -r requirements.txt
```

## 📚 Scientific Background

### Solar Flare Physics
Solar flares are sudden releases of electromagnetic energy in the solar corona, classified by their X-ray flux:
- **A, B, C**: Background levels
- **M**: Medium flares (10^-5 to 10^-4 W/m²)
- **X**: Major flares (>10^-4 W/m²)

### Nanoflares
Tiny flares with energies ~10^24-10^27 erg, potentially responsible for coronal heating through power-law energy distribution with steep indices (α > 2).

### GOES/EXIS Data
The Geostationary Operational Environmental Satellites carry the Extreme Ultraviolet and X-ray Irradiance Sensors (EXIS) providing:
- **XRS**: X-Ray Sensor (0.5-4 Å, 1-8 Å)
- **EUVS**: Extreme UV Sensor
- **1-minute cadence**: High temporal resolution

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- NASA GOES Team for satellite data
- Solar Physics community for scientific guidance
- Open source libraries and frameworks used

## 📞 Support

For support, please open an issue in the repository or contact the development team.

---

**Built with ❤️ for Solar Physics Research**

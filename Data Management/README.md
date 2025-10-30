# Data Management Guide

## Storage Solutions

### GitHub
GitHub provides version-controlled storage ideal for:
- Code repositories and scripts
- Collaborative projects with multiple contributors
- Tracking changes and maintaining project history
- Public repositories (free) or private repositories (free with limitations)

**Best for:** Code, documentation, small datasets (<100MB files), configuration files

**Limitations:** Not suitable for large binary files; 100GB repository size limit

Very basic tutorial on Github: https://docs.github.com/en/get-started/start-your-journey/hello-world

Link to Github Desktop: https://desktop.github.com/download/
You can also integrate Github with your IDE (i.e. Github Extension for vscode, Github for RStudio)

### Cloud Storage
Cloud storage options (Google Drive, Dropbox, OneDrive, etc.) offer:
- Large file storage capabilities
- Easy sharing and collaboration
- Automatic synchronization across devices
- Integrated with various productivity tools

**Best for:** Large datasets, media files, backups, team file sharing

**Considerations:** Check storage quotas, access permissions, and data privacy policies

## Document Preparation

### Overleaf vs Local LaTeX

**Overleaf (Online LaTeX Editor)**
- ✅ No installation required
- ✅ Real-time collaboration
- ✅ Automatic compilation
- ✅ Built-in templates and packages
- ✅ Version history
- ❌ Requires internet connection
- ❌ Limited compile time on free tier

**Local LaTeX**
- ✅ Works offline
- ✅ Full control over packages and compilation
- ✅ Faster compilation for large documents
- ✅ No file size restrictions
- ❌ Requires installation and setup (TeX Live, MiKTeX)
- ❌ Manual version control needed
- ❌ Collaboration requires external tools

**Recommendation:** Use Overleaf for collaborative papers and quick edits; use local LaTeX for thesis-length documents or when offline access is essential.

## Computational Workflows

### Local Python Development with Anaconda

Anaconda is a comprehensive Python distribution and package manager ideal for data science and scientific computing.

**Key Features:**
- Pre-installed data science packages (NumPy, Pandas, Matplotlib, Scikit-learn, etc.)
- Conda package manager for easy installation and dependency resolution
- Environment management for isolated project dependencies
- Cross-platform support (Windows, macOS, Linux)
- Includes Jupyter Notebook and JupyterLab

**Environment Management:**
```bash
# Create a new environment
conda create -n myproject python=3.10

# Activate environment
conda activate myproject

# Add conda-forge channel
conda config --add channels conda-forge

# Install packages
# (from anaconda's default package list, and from anaconda 5.0 it will automatically search conda-forge)
conda install numpy pandas matplotlib

# Export environment
conda env export > environment.yml

# Create environment from file
conda env create -f environment.yml
```

**Advantages:**
- ✅ Manages both Python packages and system dependencies
- ✅ Isolated environments prevent dependency conflicts
- ✅ Works offline once packages are cached
- ✅ Easy to replicate environments across machines
- ✅ Handles complex dependencies better than pip alone

**Anaconda vs Miniconda:**
- **Anaconda:** Full installation (~3GB) with 250+ pre-installed packages
- **Miniconda:** Minimal installation (~400MB) with only Python and conda

**Best Practices:**
- Create separate environments for each project
- Use `environment.yml` files for reproducibility
- Regularly update conda: `conda update conda`
- Consider Miniconda if you want to minimize installation size

### Google Colab with Google Drive Integration

Google Colab integrated with Google Drive enables:
- Cloud-based Jupyter notebooks with free GPU/TPU access
- Seamless data access from your Drive storage
- Collaborative coding and analysis
- No local setup required

**Mounting Google Drive:**
```python
from google.colab import drive
drive.mount('/content/drive')
```

**Use cases:**
- Machine learning model training
- Data analysis and visualization
- Quick prototyping without local compute resources
- Sharing reproducible analysis notebooks

**Limitations:**
- Session timeouts (12-hour maximum)
- Resource limitations on free tier
- Requires Google account

**Anaconda vs Colab:**
- **Use Local Anaconda** for: development, debugging, offline work, full environment control
- **Use Colab** for: GPU/TPU access, collaboration, no-setup-required analysis, sharing results

## Integrated Development Environments (IDEs)

### Visual Studio Code (VS Code)
**Best for:** General-purpose programming, Python, web development

**Benefits:**
- Free and open-source
- Extensive extension marketplace
- Built-in Git integration
- Integrated terminal
- Excellent Python support with extensions
- Remote development capabilities (SSH, containers, WSL)
- Jupyter notebook support
- Lightweight and fast

### Vanilla Jupyter Notebook / JupyterLab
**Best for:** Data analysis, exploratory work, documentation

**Benefits:**
- Interactive code execution
- Inline visualization and markdown
- Easy to share and reproduce analyses
- Supports multiple programming languages
- Great for teaching and presentations
- JupyterLab offers enhanced interface with tabs and extensions
- Widely used in data science community

### Spyder
**Best for:** Scientific computing, MATLAB users transitioning to Python

**Benefits:**
- Comes with Anaconda distribution
- MATLAB-like interface
- Variable explorer for inspecting data
- Integrated IPython console
- Built-in debugger
- Help pane with documentation
- Designed specifically for data science

### RStudio
**Best for:** R programming, statistical analysis

**Benefits:**
- Industry standard for R development
- Integrated R console, editor, and plots
- Package management
- R Markdown support for reproducible reports
- Git integration
- Project management features
- Free and open-source

### Sublime Text / Atom
**Best for:** Lightweight text editing, quick scripts

**Benefits:**
- Fast and responsive
- Minimal resource usage
- Extensible with packages
- Multiple cursors and selections
- Cross-platform
- Good for quick edits and smaller projects
- Note: Atom development discontinued in 2022

**Choosing an IDE:**
- **Beginners:** Start with VS Code or Jupyter Notebook
- **Data Science:** Jupyter, Spyder, or VS Code with Python extensions
- **Professional Development:** PyCharm Professional or VS Code
- **R Users:** RStudio
- **Quick Scripts:** Sublime Text or VS Code

## Best Practices

1. **Version Control:** Use Git/GitHub for all code and text-based files
2. **Backup Strategy:** Follow 3-2-1 rule (3 copies, 2 different media, 1 offsite)
3. **Documentation:** Maintain clear README files and documentation
4. **File Organization:** Use consistent naming conventions and folder structures
5. **Access Management:** Set appropriate permissions for shared resources

---

*Last updated: October 2025*

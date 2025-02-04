# **AI Image Generator using Together Ai & Flux**

MindSketch.Ai is an open-source, real-time AI image generator powered by Together.ai, designed for seamless and high-quality image creation. It enables users to generate stunning visuals instantly, making AI-driven creativity more accessible and efficient. With customizable parameters and an intuitive interface, users can generate images for various themes such as Fantasy, Sci-Fi, Nature, Artistic, and more.

## **Features**

- **Dynamic Prompt Library**: Choose from a collection of predefined prompts for themes like Fantasy, Sci-Fi, Nature, and more, or provide your own custom text prompts.
- **Customizable Parameters**: Fine-tune generation settings like CFG scale, steps, resolution, and batch size to get your desired result.
- **Batch Image Generation**: Generate multiple images at once with unique prompts for each image.
- **Interactive UI**: Real-time prompt selection, live image previews, and easy-to-use download options.
- **Optimized Performance**: Automatically switch between GPU and CPU for optimal performance. Supports both high-end GPUs and fallback to CPU for compatibility.
- **High-Resolution Image Generation**: Ability to generate high-quality images at resolutions up to 512x512 with additional fine-tuning options.

---

## **Tech Stack**

### **Backend:**
- **[Python](https://www.python.org/)**: Used for backend server-side logic.
- **[Flask](https://flask.palletsprojects.com/)**: Lightweight web framework for API handling.
- **[PyTorch](https://pytorch.org/)**: Deep learning framework used for model execution.
- **[Flask-CORS](https://flask-cors.readthedocs.io/en/latest/)**: For handling Cross-Origin Resource Sharing (CORS).

### **Frontend:**
- **[React.js](https://reactjs.org/)**: JavaScript library for building interactive user interfaces.
- **[Tailwind CSS](https://tailwindcss.com/)**: Utility-first CSS framework for styling.
- **[Axios](https://axios-http.com/)**: Promise-based HTTP client for the browser and Node.js to handle API calls.

---

## **Demo**

<img src="https://github.com/user-attachments/assets/032c0d5a-627d-4354-9489-d5acfb653411" width="400"/>

<img src="https://github.com/user-attachments/assets/4ce9f4ec-5e8c-4fa1-aa27-4397285a8bea" width="400"/>

<img src="https://github.com/user-attachments/assets/44834f34-f5aa-4cfb-ba4e-4e195f8192e0" width="400"/>

<img src="https://github.com/user-attachments/assets/b0621a50-ecf0-41ac-8f89-dcca6861f03a" width="400"/>





---

## **Getting Started**

Follow the steps below to set up the project locally:

### **Prerequisites**
Before you start, ensure you have the following installed:
- **Python 3.8+**  
- **Node.js 16+**  
- **npm**  
- A **CUDA-enabled GPU** (recommended but not required for CPU fallback support).

### **Backend Setup**
1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/stable-diffusion-image-generator.git
   cd stable-diffusion-image-generator
   ```

2. **Set up a virtual environment** (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Python dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Flask server**:
   ```bash
   python app.py
   ```
   The server will start at `http://127.0.0.1:5000`.

---

### **Frontend Setup**
1. Navigate to the `frontend` directory:
   ```bash
   cd frontend
   ```

2. Install the necessary dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```
   Your React app will now be running at `http://localhost:3000`.

---

## **Usage**
Once both the frontend and backend servers are running:
1. Open your browser and go to `http://localhost:3000` (React app).
2. Select a prompt from the dropdown menu or enter a custom prompt.
3. Adjust parameters such as **guidance scale**, **steps**, and **resolution** for the desired image output.
4. Click **Generate Images** to create the images.
5. Download your generated images by clicking the download button.

---

## **Folder Structure**
```
.
├── app.py                # Backend logic (Flask)
├── requirements.txt      # Python dependencies
├── generated_images/     # Folder for storing generated images
├── frontend/             # React frontend code
│   ├── public/           # Static assets
│   ├── src/              # Source code for frontend
│   │   ├── App.jsx       # Main React component
│   │   ├── index.css     # Styling with Tailwind CSS
│   │   └── components/   # React components for UI
├── screenshots/          # Demo images for README
└── README.md             # Project documentation
```

---

## **Environment Variables**

Create a `.env` file in the root directory to configure certain parameters:
```env
# Flask Configuration
FLASK_APP=app.py
FLASK_ENV=development

# Model configuration
MODEL_NAME=stabilityai/stable-diffusion-3.5-large
DEVICE=cuda  # Options: cuda, cpu
```

### **Explanation of Environment Variables:**
- `MODEL_NAME`: The model checkpoint for Stable Diffusion.
- `DEVICE`: Specifies whether the model runs on GPU (`cuda`) or CPU (`cpu`).

---

## **Troubleshooting**

### **Out of Memory Errors**:
- Reduce the **image resolution** or **batch size** in the settings.
- Use a GPU with more VRAM or switch to CPU (though slower).

### **CORS Issues**:
- Ensure the Flask server (`http://127.0.0.1:5000`) is running.
- Make sure the React app is correctly configured to interact with this URL for API requests.

### **Flask Server Not Starting**:
- Check for any missing dependencies with `pip freeze`.
- Ensure no other services are using port 5000.

### **Frontend Issues**:
- If the React app is not loading, ensure that it's running on the correct port (`http://localhost:3000`).
- Check the developer console for any errors related to API calls or components.

---

## **Future Enhancements**

- **Higher-Resolution Images**: Support for images with larger resolutions and tiling techniques for even better quality.
- **User Profiles & History**: Allow users to save and track generated images.
- **Image Customization**: Implement features like image upscaling, watermarking, or applying additional filters.
- **Advanced UI/UX**: Introduce an even more polished UI with enhanced responsiveness and user experience.
- **Model Fine-Tuning**: Integrate the ability for users to fine-tune the model with their custom datasets.

---

## **Contributing**

We welcome contributions to this project! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push the changes to your forked repository.
5. Create a pull request for review.

---

## **Contact**

If you have any questions, suggestions, or issues, feel free to reach out:

**Sarthak Arora**  
📧 Email: [sarthakk.arora1@gmail.com](mailto:sarthakk.arora1@gmail.com)

---

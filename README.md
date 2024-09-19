# Machine Learning Approach to Extracting Entity Values from Images

## 📝 Introduction
This project focuses on extracting key entity values from product images, a common requirement in e-commerce. Attributes such as weight, dimensions, voltage, and wattage need to be extracted from images when textual descriptions are insufficient. By employing Optical Character Recognition (OCR) and machine learning techniques, this project aims to enhance inventory management, quality assurance, and listing accuracy.

## 🔧 Machine Learning Approach
The process involves several key steps:

### 1. Data Preprocessing
- **Image Access**: Images of products are accessed via URLs.
- **Text Extraction**: OCR is applied to extract text from the images.
- **Text Cleaning**: Unnecessary spaces and symbols are removed to prepare the text for further processing.

### 2. Pattern Recognition with Regular Expressions (Regex)
- **Pattern Identification**: Regular expressions are used to identify patterns in the text related to product attributes such as weight, voltage, and dimensions.
  - Example Regex for Weight: `r'(?:item weight|weight)[\s:]*([\d.]+\s?(?:lbs?|pounds?|kg|kilograms?|g|grams?))'`
  - This pattern captures relevant keywords and numeric values along with their units (e.g., "50 pounds" or "22 kg").
- **Attribute Extraction**: Similar regex patterns are used for other attributes like depth, width, height, voltage, and wattage.

### 3. Unit Conversion
- **Standardization**: Extracted values are standardized to a consistent format.
- **Unit Mapping**: A dictionary maps various abbreviations to their full forms (e.g., 'kg' to 'kilogram', 'lbs' to 'pound').

## 🧰 Machine Learning Models Used
In this project, the following tools and techniques were utilized:

### Optical Character Recognition (OCR)
- **Tesseract**: An open-source OCR tool used for extracting textual information from images.

### Regex-Based Feature Extraction
- **Regex Patterns**: A rule-based approach was chosen to efficiently handle structured patterns in text, without employing traditional machine learning models such as decision trees or neural networks.

## 🔬 Experiments Conducted
### 1. Text Extraction Using Tesseract
- **Pre-Processing**: Experimented with different image pre-processing techniques (e.g., contrast, brightness adjustments) to enhance OCR accuracy.

### 2. Regex Optimization
- **Pattern Refinement**: Iteratively refined regex patterns to improve extraction accuracy and handle various formats and OCR errors.

### 3. Handling Edge Cases
- **Challenges Addressed**:
  - Images without relevant information.
  - OCR errors leading to missing or incorrect characters.
  - Products with complex layouts where text and numbers were not easily separable.

## 🏁 Conclusion
The project demonstrated the effective application of OCR and regex for extracting product-related entity values from images. By leveraging these techniques, the system successfully parsed attributes like weight, dimensions, and voltage from images. This approach is particularly valuable for datasets with minimal textual descriptions.

### Future Work
- **NLP Models**: Potential integration of Natural Language Processing models to enhance text processing.
- **Deep Learning**: Exploration of deep learning techniques to improve OCR accuracy on noisy or complex images.

The combination of Tesseract OCR and regex-based feature extraction provides an efficient and accurate solution for extracting structured data from unstructured image content.


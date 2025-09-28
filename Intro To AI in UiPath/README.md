# AI_in_UiPath_Tasks Documentation

This project demonstrates various AI and automation tasks using UiPath, including Document Understanding, Communication Mining, and Generative AI. Below is a comprehensive overview of the project structure, key files, and their purposes.

## Project Structure

```
AI_in_UiPath_Tasks/
├── AI_Center_DU_Output.xlsx
├── Document Understanding Model Evaluation.png
├── Main.xaml
├── project.json
├── Test.xaml
├── 0_Material/
│   ├── 0.1_DU_Dataset/
│   │   ├── batch1-0001.jpg
│   │   ├── ...
│   │   └── invoice_Adrian Barton_35579.pdf
│   └── 0.2_ComsMining_Dataset/
│       └── uipath_comm_mining_dummy_5000.csv
├── 1_AI_Center/
│   └── 1.2_AI_Center_DocProcessing.xaml
├── 2_Document_Understanding/
│   └── 2.1_IDP_DU.xaml
├── 3_Communication_Mining/
│   └── 3.1_ComsMining.xaml
├── 4_Generative_AI/
│   └── 4.1_Gen_AI.xaml
└── DocumentProcessing/
    ├── IntelligentKeywordLearningFile.json
    └── taxonomy.json
```

## Folder and File Descriptions

### Root Files
- **AI_Center_DU_Output.xlsx**: Output results from Document Understanding (DU) models.
- **Document Understanding Model Evaluation.png**: Visual evaluation of DU model performance.
- **Main.xaml**: Main UiPath workflow entry point.
- **project.json**: Project configuration and dependencies.
- **Test.xaml**: Test workflow for validating components.

### 0_Material/
- **0.1_DU_Dataset/**: Contains sample images and PDF invoices for Document Understanding tasks.
- **0.2_ComsMining_Dataset/**: Contains communication mining dataset (CSV) for text analytics.

### 1_AI_Center/
- **1.2_AI_Center_DocProcessing.xaml**: UiPath workflow for processing documents using AI Center models.

### 2_Document_Understanding/
- **2.1_IDP_DU.xaml**: Workflow for Intelligent Document Processing (IDP) and Document Understanding.

### 3_Communication_Mining/
- **3.1_ComsMining.xaml**: Workflow for mining and analyzing communication data.

### 4_Generative_AI/
- **4.1_Gen_AI.xaml**: Workflow demonstrating generative AI capabilities (e.g., text generation).

### DocumentProcessing/
- **IntelligentKeywordLearningFile.json**: Configuration for keyword learning in document processing.
- **taxonomy.json**: Taxonomy definition for document classification and extraction.

## How to Use
1. **Open the Project in UiPath Studio**: Load `Main.xaml` or any specific workflow to explore or run.
2. **Explore Datasets**: Use the sample data in `0_Material/` for testing workflows.
3. **Run Workflows**: Execute workflows in each numbered folder to see different AI capabilities:
   - Document Understanding (2_Document_Understanding)
   - Communication Mining (3_Communication_Mining)
   - Generative AI (4_Generative_AI)
4. **Review Outputs**: Check output files and logs for results and evaluation.

## Project Highlights
- **End-to-End Document Processing**: From raw documents to structured data extraction.
- **AI Center Integration**: Leverage UiPath AI Center for model deployment and inference.
- **Communication Mining**: Analyze large-scale communication data for insights.
- **Generative AI**: Demonstrate text generation and AI-powered automation.

## Credits
Developed as part of Raya RPA Training for AI in UiPath.

---

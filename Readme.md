Overview
 The scope of this exercise is to build a simple step within a data pipeline to help with
 data collection and transformation for an AI assistant based system. The primary data
 source will be a PDF document for this pipeline, and multiple documents can be used.
 The objective is that these steps are delivering a RAG based context for the AI assistant
 to answer questions based on the contents within the document(s).
 Exercise
 1. Pick a source document or can be a handful of documents that are PDF format.
 This will be the primary data source for this exercise. You can use any PDFs from
 this location: https://arxiv.org/list/cs/recent Or you can use any PDF of your
 choice for this exercise.
 2. Read the file from a source location (can be an S3 bucket or a local file location).
 3. The document from this location is parsed, broken into text chunks based on
 either a fixed length or paragraph.
 4. Implement any preprocessing steps as you see necessary based on the sample
 document. These will be data cleansing tasks that might be necessary.
 5. Create vector embeddings out of the text chunks that are extracted. If there are
 any images in the document, those can be ignored. You can use any
 embeddings model for the vectorization. ChromaDB can be used to store the
 embeddings and any other choices can be used.
 6. Write a function to search these vectors with a query to return similar results. In
 this function, convert the query to vector form and return results based on the
 nearest similar result.
 Please use any open source tools as necessary for this exercise. The code can be
 delivered via github repo or a zip file.


How to run the Notebook.
1. There is an ipython notebook. It contains self explanatory Markdown cells to naviagte through the notebook to complete the this excercise.
2. I have used the "MS_2022_Annual_Report.pdf" file as input to create the vector data store.
3. I have used python packages PyPDF2, langchain, chromadb, langchain-text-splitters and sentence_transformers to implement this excercise
4. We can use the following things for imporvments
> We can create summary from every chunks & can store that as metadata in vector store to get better similar vector match.
> We can try with different indexing techniques apart from the one I used {"hnsw:space"}
> We can try differnet similarity finds techniques apart from {"cosine"}

Thanks!

# Application: Automatic Attendance Tracking at ASU

The developed face recognition system can be effectively used for automatic attendance tracking in classrooms at Arizona State University (ASU).

Face recognition is a popular task in computer vision and it involves identifying or verifying the identity of an individual using their face. In this project, we use a combination of two neural network models, MTCNN for face detection and Facenet for extracting face embeddings. These models are pre-trained and we then fine-tune them to achieve high accuracy on our specific task.


## Scenario and Workflow

Consider a classroom scenario where each student has a unique ID and has their face images stored in the database. The system can be deployed on a device with a camera at the entrance of the classroom.

1. As each student enters the classroom, their face is detected and captured by the camera.
2. The captured image is then fed into our face recognition system which uses MTCNN for face detection and Facenet for generating face embeddings.
3. The system compares the generated face embeddings with the stored embeddings in the database using Euclidean distance. If a match is found within a certain threshold, it identifies the student.
4. The system then automatically marks the attendance for that student in the system.

## Benefits

This system can greatly simplify the process of taking attendance, saving a significant amount of time for instructors. Additionally, it can also help reduce errors that can occur in manual attendance marking.

Automatic attendance tracking also adds a layer of convenience for students as they do not need to manually sign any attendance sheets. 

## Privacy Considerations

While implementing such a system, it is important to consider and respect the privacy of the students. Any face data used should be obtained with the students' consent. Also, data security measures should be implemented to ensure the stored face embeddings are not accessible by unauthorized persons.

## Conclusion

With the combination of MTCNN and Facenet, we can create an automatic attendance tracking system that is not only effective but also efficient, making it a potentially valuable tool for educational institutions like ASU.```

## Multi-task Cascaded Convolutional Networks (MTCNN)

The first step in face recognition is to locate the face in the image. This is the job of a face detector. In this project, we use Multi-task Cascaded Convolutional Networks (MTCNN), which is an effective model for face detection. It proposes boxes in an image and classifies each proposal box as a face or not a face.

## Facenet

Once we have the face from the image, we then use Facenet model to generate a face embedding. Facenet is a face recognition system that was described by Florian Schroff, et al. at Google in their 2015 paper titled “FaceNet: A Unified Embedding for Face Recognition and Clustering.” It achieved state-of-the-art results on the LFW, YTF, and IJB-A benchmarks.

Facenet doesn't output a label for the face, instead it outputs a 128-dimensional vector (embedding) that provides a unique representation of the face. These embeddings can then be easily compared to measure the similarity of faces.

## Calculating Similarity Using Euclidean Distance

We use the Euclidean distance between two face embeddings to quantify the similarity between faces. In simple terms, face embeddings are plotted in a 128-dimensional space and the Euclidean distance is the straight-line distance between two points (embeddings) in this space.

If the Euclidean distance is below a certain threshold, the faces are considered to be the same.

## Conclusion

By combining MTCNN and Facenet, we can build an effective face recognition system that can accurately detect faces in images and then recognize those faces based on their unique embeddings.```

# Camera-Based Retail Product Verification: Case Study

**Haluk Doğaç Ergüvenç · AI software engineering · October 2025–August 2026**

## The problem

On a self-service retail scale, a customer places an item on the weighing surface and selects a product code, or PLU, on the screen. Selecting a different product can produce an incorrectly priced label. The project aimed to detect this mismatch by comparing the selected product with a camera image of the item.

## My role

I independently handled the AI development during approximately 10 months of practical engineering work. My responsibilities covered data workflows, model training, and inference integration. I also contributed to the backend and management interface supporting verification.

The product scope included approximately 40 classes. The work combined **Python, PyTorch, ResNet18, OpenCV, FastAPI, MongoDB, React, and Tailwind CSS**.

## User workflow

1. The customer places a product on the scale and waits for the weight to stabilize.
2. The customer selects the product on the scale's screen.
3. The camera captures an image of the product.
4. The verification workflow compares the image with the selected product.
5. The system provides a match or mismatch assessment for review.

The scope of this case study is the verification workflow. It does not describe a particular rule for blocking label printing or overriding the scale's behavior.

## Engineering work

### Data and models

I developed workflows for collecting product images, organizing PLU-indexed data, training models, maintaining an embedding store, and evaluating images in batches.

I used PyTorch for image classification, including a ResNet18 classifier, and developed embedding-based verification. These approaches supported the task of relating a product image to the product selected by the user.

### Backend and inference

I integrated trained local models into a FastAPI backend. The application supported offline inference as well as cloud vision APIs through a hybrid architecture. MongoDB supported the application's data workflows, and OpenCV was used for camera and image processing.

### Management interface

I developed a React and Tailwind CSS interface for managing product codes, changing operating modes, inspecting metrics, and reviewing captured images. This provided a way to work with collected data and inspect verification results alongside the live workflow.

## Pilot outcome

The system reached a store pilot and was tested by store managers. The pilot is the confirmed stage of deployment described here.

After the pilot, the customer decided not to continue using the feature. This case study does not attribute that decision to a technical or commercial cause.

This case study presents the engineering scope and my contributions. It does not report numerical accuracy or latency because the measurement conditions and evaluation records have not been established for publication.

## What this work demonstrates

- Connecting computer vision models to an application backend and user interface.
- Building a workflow from image collection through training, evaluation, and live verification.
- Supporting local inference and cloud-based analysis within the same application.
- Taking responsibility for AI development in a project tested outside a development environment.

Implementation code and store data are not included here.

## About me

I'm a 2025 graduate of an English-taught Computer Engineering program, based in İstanbul, Türkiye. I'm seeking junior Python backend, AI application, or full-stack engineering roles: office or hybrid work in İstanbul, or fully remote roles open to candidates based in Türkiye.

[LinkedIn](https://www.linkedin.com/in/haluk-dogac-erguvenc) · [GitHub](https://github.com/DogacErguvenc)

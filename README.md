# AI_Deep_Learning_Classification

Exploring Neural Style Transfer & Localized Style Transfer techniques in Persons Images

The domain chosen for this study is the result after the authors used an app called Prisma. Prisma allows you to apply painting styles of famous painters to your own photos. The authors further investigated the Neural Style Transfer problem and got inspired by the paper ’A Neural Algorithm of Artistic Style’ who came out in 2015. In this project, we will explore the Deep Learning capabilities for Neural Style Transfer, not only by generating an entire stylised image, but also Class-based Neural Style Transfer.

We believe that these techniques can shed the light on the roots of the creative process in general.
In this sense, our aim is to investigate the vanilla style transfer model, apply modifications to the original architecture, and with the help of transfer learning and fine-tuning attempt to get more aesthetic results. 
Furthermore, we describe our instance segmentation model that we adopted for the localized style transfer, and we show some benchmarks.

For the chosen topic, a subset of the COCO dataset will be considered, consisting approximately of 67000 images and their annotations from the class ‘person’. The whole dataset is publicly available in the following link, http://cocodataset.org/#download

The filtered dataset was derived after creating two scripts. Initially we downloaded the whole Coco dataset and we applied code to draw out only the images that were annotated with the “person” category. In like manner, the annotations from images that do not exist had to be removed, since we realised that we cannot apply any training in our models if images and annotations do not match. 

Regarding the Neural Style Transfer technique, we used pretrained VGG19 and VGG16 to further train the selected input images and generate a stylised output image. First and foremost we selected these models because they are large and we can gain a better understanding of how exactly CNNs recognize specific patterns of objects.

Neural Style Transfer works in reverse than a normal CNN. It can reconstruct high quality images in the lower layers while keeping the high-level content in later layers.

For our instance segmentation task, we downloaded from the model zoo various weights from models that were pretrained on COCO. Detectron2 and DeepLabv3 frameworks were used along with R50FPN_MaskRCNN and R101FPN_MaskRCNN. 



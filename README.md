# Bioactivity

Bioactivity or pharmacological activity is the capacity of a specific molecular entity to achieve a defined biological effect on a target (drug action). It is measured in terms of potency or the concentration of a molecular entity needed to produce the effect.

The 4 main targets for drug action of a molecular entity are: receptors, ion channels, enzymes and carrier molecules. In each of these four cases, most drugs are effective beacause they bind to particular target proteins. In this repository the target is a Proteasome subunit called beta type-5 which is a protein encoded by the PSMB5 gene.

PSMB5 plays a key role in the maintenance of protein homeostasis by removing misfolded or damaged proteins that could impair cellular functions, and by removing proteins whose functions are no longer required.

### Proteasome complex with a highly ordered ring-shaped 20S core structure in humans:

![Proteasome complex](https://user-images.githubusercontent.com/91697343/144529179-dce915e8-d6dd-44d0-b363-6ddfef946f12.png)


### Subunit beta type-5 (our target)!

![PSMB5 subunit](https://user-images.githubusercontent.com/91697343/144529598-8e45fd8e-8352-4ae5-b8bf-feb2f3a2b3ca.jpeg)

The target data is collected from ChEMBL(dataCollection_ChEMBL). From this website it is posible to find pharmacological target data to evaluate bind molecules that influence their activity. This is a key part to know what kind of measure, concentration or ‘potency’ is used in the substances that are going to interact with the targets. In this repo the IC50 or half maximal inhibitory concentration is the one we are going to work with.  

It is important to prepare (active-inactive compounds) and transform (pIC50) the dataset for accurate analysis and machine learning models. Molecular descriptors are also related and necesary to achive this. 
They are a functionally complete set which express a large number features of molecules used to quantitatively describe the physical and chemical information of each. An example of molecular descriptiors is LogP which is a cuantitative representation of lipophilicity of the molecules. In this repository the PaDEL descriptor is selected to transform chemical information encoded within a representation of a molecule into useful numbers (binary) to be applied in a model. Random forest is chosen because it avoid overfitting and deal with imbalanced classes properly.

https://github.com/grammaloreto/Bioactivity/tree/main/Active-Inactive_types
https://github.com/grammaloreto/Bioactivity/tree/main/MeasurementTransformation
https://github.com/grammaloreto/Bioactivity/tree/main/descriptors4binaryDF

Finally after running the model one of the active compounds (Bortezomib) is picked to make an anlysis and find similar molecules. Is well know that this molecule is a proteasome (our target) inhibitor used to treat multiple myeloma and mantle cell lymphoma. Currently most drugs are characterized for attack more than one target so it is pertinent to find more entities where we can use this molecule or their derivates. 

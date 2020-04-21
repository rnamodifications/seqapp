# Direct Sequencing of tRNA-Phe using Anchor-based Algorithm

Copyright (c) 2020 Wenjia Li, Shenglong Zhang, New York Institute of Technology

This software is licensed under the the MIT License. Contact for other licensing 
terms.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## General Introduction

This software provides a proof-of-concept implementation of an anchor-based algorithm 
that can de novo and directly sequence a specific tRNA like tRNA-Phe using MFE data 
output from LC-MS.


### Requirements

You must have Java SE Development Kit (JDK) version "12.0.1" or above and Maven, 
and you are also recommended to use IDEs such as Eclipse or IntelliJ to open and 
run this software.


### Installation

Once you download and install the appropriate JDK, go to the root folder of the project,
and run the following command in the terminal: 

```bash
mvn package
```

You will then find a file named `sequencing-0.0.1-SNAPSHOT.war` in the `target/` folder.
This file should be placed to the `/webapps/` in the web-based sequencing app folder.


### Usage

To run the software directly from Java, you can open the project from an IDE.

The FindSequence.java file in the software contains a main method where you can execute it. In the
main method, there is a statement as follows.

String fileName = "D://seq_app_src/MFE_data/1114s05_3forms_TableS1-3.txt";

You can replace the fileName with any data file that has the same format as the sample data files 
in the software package. Note that the full file path is required to allow the software locate the 
data file and then read out sequence successfully.

In the IDE such as Eclipse and IntelliJ, you can simply navigate to the FindSequence.java file, and
click the "Run" button or menu item to run the whole software.

### Parameters

<anchor_bank.csv>: The anchor dataset filename
	Filename of a list of anchor in the format of "AnchorName	AnchorMass"

<base_bank.csv>: The base and modification dataset filename
	Filename of a list of bases and their known modifications in the format of "BaseName	BaseMass"

<directory>: The directory to output the result for final sequence reads

<fasta_directory>: The directory to output the result in terms of the FASTA format



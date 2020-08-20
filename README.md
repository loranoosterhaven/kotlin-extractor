# KotlinExtractor: Invocation tracing to extract Kotlin language features

## Abstract

Java programming language has been long used to develop native Android mobile applications. Three years ago, Google has announced official support for Kotlin programming language for Android development. Last year, Google announced that Kotlin became its preferred language for Android app developers. Ever since, many companies and freelancers have switched into using Kotlin partially or entirely. Yet, the true security and privacy implications of this shift has not been thoroughly studied. This work is considered the first step towards achieving that. In this work \emph{KotlinExtractor} has been developed to directly extract Kotlin language features from Android Application Packages (APKs) using the invocation tracing technique.

KotlinExtractor was validated to extract accurate results using several large datasets of Android apps combined with GitHub repository language statistics. KotlinExtractor is able to estimate the percentage of Kotlin code inside an application with a mean error of 3.1%. Using a combination of invocation tracing and pattern scanning, 10 different Kotlin language features are identified successfully within a dataset of obfuscated Android applications. No cases were found throughout this research where KotlinExtractor incorrectly identified an application as having traces of Kotlin code.

We believe that by combining the output of KotlinExtractor with the output of existing vulnerabilities and security scanners, security researchers would be able to accurately measure the security and privacy implications of using Kotlin.

## Authors 

- Loran Oosterhaven
- Fadi Mohsen (supervisor)
- Fatih Turkmen (second supervisor)
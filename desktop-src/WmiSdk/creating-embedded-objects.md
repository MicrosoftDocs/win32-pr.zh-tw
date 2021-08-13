---
description: 使用内嵌物件建立實例時，請執行下列工作：
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: 建立内嵌物件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2e54e16005669ebd77b0bc08e5d3174f7aa5fadee2a47477920e91aaa2ae155b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464168"
---
# <a name="creating-embedded-objects"></a>建立内嵌物件

使用内嵌物件建立實例時，請執行下列工作：

-   您必須將内嵌物件宣告為強型別或弱式類型。

    強型別物件指向特定類別的物件，並使用類別名稱。 弱式型別物件指向未指定類別的物件，並使用 **object** 關鍵字。 這兩個物件都對應至 **VT \_ 未知** 型別。

-   您可以在初始化和宣告中使用 **Null** 做為内嵌物件和路徑的預設值。
-   內嵌物件路徑時，請勿在內嵌路徑的元素之間放置空白字元。 例如，物件路徑 "Class1Index = 3;" 不包含屬性名稱 "Class1index" 和所指派值（也就是 "3"）之間的空格。

下列類別宣告示範如何宣告強型別和弱式類型的内嵌物件。

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

下列範例說明如何在類別宣告中宣告内嵌物件。

``` syntax
Class Class1 
{ 
     [key] sint32 Class1Index;
};

Class Class2 
{
    [key] sint32 Class2Index;
    Class1 EmbedObject1 = instance of Class1{Class1Index=3;};
};

Class Class3
{
    [key] sint32 Class3Index;
    Class2 EmbedObject2 = instance of Class2 {Class2Index=4;};
};
```

下列範例描述的是一個屬性（強型別物件）和另一個屬性（弱型別物件陣列）的初始化。

``` syntax
Class EmbedClass1
{
    [key] sint32 intval;
};

Class EmbedClass2
{
    [key] string sval;
};

Class ContainerClass
{
    [key] sint32 intval;
    EmbedClass1 SingleObject;
    Object ArrayObject[];
};

Instance of ContainerClass
{
    intval = 33;
    SingleObject = instance of EmbedClass1 {intval=99;};
    ArrayObject = {instance of EmbedClass2 {sval="something";},
                   instance of EmbedClass1 {intval=100;}};
};
```

 

 




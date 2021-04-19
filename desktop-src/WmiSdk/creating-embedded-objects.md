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
ms.openlocfilehash: a76a70fa0e01068622a4f4cdbbbfb6c992b67f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983830"
---
# <a name="creating-embedded-objects"></a><span data-ttu-id="b3e5e-103">建立内嵌物件</span><span class="sxs-lookup"><span data-stu-id="b3e5e-103">Creating Embedded Objects</span></span>

<span data-ttu-id="b3e5e-104">使用内嵌物件建立實例時，請執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="b3e5e-104">When creating an instance with embedded objects, perform the following tasks:</span></span>

-   <span data-ttu-id="b3e5e-105">您必須將内嵌物件宣告為強型別或弱式類型。</span><span class="sxs-lookup"><span data-stu-id="b3e5e-105">You must declare an embedded object as strongly typed or weakly typed.</span></span>

    <span data-ttu-id="b3e5e-106">強型別物件指向特定類別的物件，並使用類別名稱。</span><span class="sxs-lookup"><span data-stu-id="b3e5e-106">A strongly typed object points to an object of a specific class and uses the class name.</span></span> <span data-ttu-id="b3e5e-107">弱式型別物件指向未指定類別的物件，並使用 **object** 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="b3e5e-107">A weakly typed object points to an object of an unspecified class and uses the **object** keyword.</span></span> <span data-ttu-id="b3e5e-108">這兩個物件都對應至 **VT \_ 未知** 型別。</span><span class="sxs-lookup"><span data-stu-id="b3e5e-108">Both objects map to the **VT\_UNKNOWN** type.</span></span>

-   <span data-ttu-id="b3e5e-109">您可以在初始化和宣告中使用 **Null** 做為内嵌物件和路徑的預設值。</span><span class="sxs-lookup"><span data-stu-id="b3e5e-109">You can use **NULL** for the default value of embedded objects and paths in initializations and declarations.</span></span>
-   <span data-ttu-id="b3e5e-110">內嵌物件路徑時，請勿在內嵌路徑的元素之間放置空白字元。</span><span class="sxs-lookup"><span data-stu-id="b3e5e-110">When embedding an object path, do not place white space between the elements of the embedded path.</span></span> <span data-ttu-id="b3e5e-111">例如，物件路徑 "Class1Index = 3;" 不包含屬性名稱 "Class1index" 和所指派值（也就是 "3"）之間的空格。</span><span class="sxs-lookup"><span data-stu-id="b3e5e-111">For example, the object path "Class1Index=3;" contains no space between the property name "Class1index" and the value being assigned, which is "3".</span></span>

<span data-ttu-id="b3e5e-112">下列類別宣告示範如何宣告強型別和弱式類型的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="b3e5e-112">The following class declaration shows you how to declare strongly typed and weakly typed embedded objects.</span></span>

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

<span data-ttu-id="b3e5e-113">下列範例說明如何在類別宣告中宣告内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="b3e5e-113">The following examples describe how to declare embedded objects within a class declaration.</span></span>

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

<span data-ttu-id="b3e5e-114">下列範例描述的是一個屬性（強型別物件）和另一個屬性（弱型別物件陣列）的初始化。</span><span class="sxs-lookup"><span data-stu-id="b3e5e-114">The following example describes the initialization of one property that is a strongly typed object and another property that is an array of weakly typed objects.</span></span>

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

 

 




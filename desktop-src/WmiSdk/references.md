---
description: MOF 參考關鍵字字組描述物件路徑，並對應至 VT \_ BSTR Automation 型別。
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: " (WMI) 的參考"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30722910de761f3d2111a3218cf364f49ccb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850471"
---
# <a name="references-wmi"></a><span data-ttu-id="bc1f8-103"> (WMI) 的參考</span><span class="sxs-lookup"><span data-stu-id="bc1f8-103">References (WMI)</span></span>

<span data-ttu-id="bc1f8-104">MOF **參考** 關鍵字字組描述物件路徑，並對應至 VT \_ BSTR Automation 型別。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-104">The MOF **ref** key word describes an object path and maps to a VT\_BSTR Automation type.</span></span> <span data-ttu-id="bc1f8-105">物件路徑可以是伺服器和命名空間的完整路徑，或相同命名空間中另一個物件的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-105">The object path can be either a full path to a server and namespace, or a relative path to another object in the same namespace.</span></span> <span data-ttu-id="bc1f8-106">您可以使用 **ref** 關鍵字來將兩個或多個類別連結在一起。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-106">You can use a **ref** key word to link two or more classes together.</span></span> <span data-ttu-id="bc1f8-107">WMI 支援兩種類型的物件路徑，用來定義 WMI 內的一般或特定路徑。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-107">WMI supports two types of object paths, which use to define general or specific paths within WMI.</span></span>

<span data-ttu-id="bc1f8-108">**參考** 關鍵字的主要目的是要減少完全存在於 WMI 儲存機制中的物件之間的傳輸時間和編碼。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-108">The main purpose of the **ref** key word is to reduce transport time and encoding between objects that exist entirely within the WMI repository.</span></span> <span data-ttu-id="bc1f8-109">您也可以使用 **ref** 關鍵字來建立兩個類別之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-109">You can also use the **ref** key word to create an association between two classes.</span></span> <span data-ttu-id="bc1f8-110">如需詳細資訊，請參閱宣告 [關聯類別](declaring-an-association-class.md)。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-110">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span> <span data-ttu-id="bc1f8-111">如果參考的專案位於相同的 MOF 檔案內，請使用別名來初始化 **參考** 值。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-111">If the referenced item is located within the same MOF file, use an alias to initialize the **ref** value.</span></span> <span data-ttu-id="bc1f8-112">如需詳細資訊，請參閱 [建立別名](creating-an-alias.md)。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-112">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

> [!Note]  
> <span data-ttu-id="bc1f8-113">當 **ref** 關鍵字套用至索引鍵屬性時，您可以透過物件字串值來區分物件參考，而不是以取值的值來區分。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-113">When a **ref** key word is applied to a key property, you can distinguish object references by the object string value instead of by the dereferenced value.</span></span>

 

<span data-ttu-id="bc1f8-114">MOF 支援弱式型別和強型別物件路徑的概念。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-114">MOF supports the concept of a weakly typed and strongly typed object path.</span></span> <span data-ttu-id="bc1f8-115">弱式類型的物件路徑指向未指定類別的物件，並使用 **ref** 關鍵字搭配 [object](object.md) 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-115">A weakly typed object path points to an object of an unspecified class and uses the **ref** key word with the [OBJECT](object.md) keyword.</span></span> <span data-ttu-id="bc1f8-116">強型別物件指向特定類別的物件，並使用 **ref** 搭配類別名稱。</span><span class="sxs-lookup"><span data-stu-id="bc1f8-116">A strongly typed object points to an object of a specific class and uses **ref** with the class name.</span></span> <span data-ttu-id="bc1f8-117">下列範例說明可指向任何類別或類別實例的弱式型別 **RefToAnyClass** 參考，以及只能指向 **ClassX** 類別或實例的 **RefToClassX** 參考：</span><span class="sxs-lookup"><span data-stu-id="bc1f8-117">The following example describes a weakly typed **RefToAnyClass** reference that can point to any class or class instance, and a **RefToClassX** reference that can point only to a **ClassX** class or instance:</span></span>

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

<span data-ttu-id="bc1f8-118">下列範例說明兩個實例，以及參考先前實例的關聯物件：</span><span class="sxs-lookup"><span data-stu-id="bc1f8-118">The following example describes two instances and an association object that references the previous instances:</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 




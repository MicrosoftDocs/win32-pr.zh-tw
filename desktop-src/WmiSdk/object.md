---
description: 物件資料類型是 WMI 類別物件，用來宣告弱型別關聯和内嵌物件。
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c257b45833204a873292da467d484fab97b22b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689435"
---
# <a name="object"></a><span data-ttu-id="68b28-103">OBJECT</span><span class="sxs-lookup"><span data-stu-id="68b28-103">OBJECT</span></span>

<span data-ttu-id="68b28-104">物件資料類型是 WMI 類別物件，用來宣告弱型別關聯和内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="68b28-104">The OBJECT data type is a WMI class object use to declare weakly typed associations and embedded objects.</span></span> <span data-ttu-id="68b28-105">在您建立類別的實例之前，您不會定義弱型別物件的特定類別。</span><span class="sxs-lookup"><span data-stu-id="68b28-105">You do not define the specific class for a weakly typed object until you create an instance of the class.</span></span> <span data-ttu-id="68b28-106">以物件資料類型定義的内嵌物件可以包含任何 WMI 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="68b28-106">Embedded objects defined with the OBJECT data type can contain instances of any WMI class.</span></span> <span data-ttu-id="68b28-107">如需詳細資訊，請參閱 [内嵌物件](embedded-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="68b28-107">For more information, see [Embedded Objects](embedded-objects.md).</span></span>

<span data-ttu-id="68b28-108">下列範例會定義和建立兩個類別的實例，其中一個類別包含 OBJECT 類型的内嵌物件：</span><span class="sxs-lookup"><span data-stu-id="68b28-108">The following example defines and creates instances of two classes, one of which contains an embedded object of type OBJECT:</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

class CompositeClass
{
    [key] string aKey;   
    object EmbObj;       // Weakly typed
};

class EmbClass

{
  [key] string aKey;
};

instance of CompositeClass
{
    aKey = "CompositeClass Key";
    EmbObj = 
        instance of EmbClass
        {
           aKey = "key for embedded object";
        };
};
```

 

 




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
# <a name="object"></a>OBJECT

物件資料類型是 WMI 類別物件，用來宣告弱型別關聯和内嵌物件。 在您建立類別的實例之前，您不會定義弱型別物件的特定類別。 以物件資料類型定義的内嵌物件可以包含任何 WMI 類別的實例。 如需詳細資訊，請參閱 [内嵌物件](embedded-objects.md)。

下列範例會定義和建立兩個類別的實例，其中一個類別包含 OBJECT 類型的内嵌物件：

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

 

 




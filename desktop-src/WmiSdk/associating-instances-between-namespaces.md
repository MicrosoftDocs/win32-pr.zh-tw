---
description: 相關檢視類別可讓您在位於不同命名空間的類別上，使用查詢的 ASSOCIATORS OF。
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: 在命名空間之間建立實例的關聯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d743b835d28af4fe0a8dd5d09858b2ba6ff0abacd0f35219c3dd90d39d0810d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557016"
---
# <a name="associating-instances-between-namespaces"></a>在命名空間之間建立實例的關聯

相關檢視類別可讓您在位於不同命名空間的類別上，使用查詢 [的 associators of](associators-of-statement.md) 。

下列程式描述如何在命名空間之間建立實例的關聯。

**若要在命名空間之間建立實例的關聯**

1.  使用 [**關聯**](meta-qualifiers.md) 字串辨識符號來開始您的類別定義。

    **JoinOn**、 [**Association**](meta-qualifiers.md)和 **Union** 限定詞都是互斥的。

2.  建立查詢，以使用 [**ViewSources**](viewsources-qualifier.md) 限定詞來定義 view 類別中所使用的來源實例。
3.  使用 [**ViewSpaces**](viewspaces-qualifier.md) 限定詞來定義來源實例所在之命名空間的名稱和位置。
4.  使用 [**PropertySources**](propertysources-qualifier.md) 限定詞，在您的 [關聯] view 類別中定義您想要的屬性。

    如有必要，您可以使用 [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) 限定詞，將任何屬性標記為屬於來源類別。

5.  使用 **直接** 辨識符號標記任何相關的屬性。

    **直接** 辨識符號會防止 View 提供者將標記的關聯參考對應到視圖參考。

下列程式碼範例示範如何建立相關檢視類別。

``` syntax
[union,
ViewSources {"SELECT * FROM Win32_OperatingSystem"},
    ViewSpaces {"\\\\.\\root\\cimv2"},
    dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Union_OS_For_AssociationExample
{
    [key, PropertySources{"Name"}]
    string Name;

    [PropertySources{"Version"}]
    string Version;

    [PropertySources{"BuildNumber"}]
    string BuildNumber;
};

[
Association,
ViewSources {"SELECT * FROM Win32_SystemOperatingSystem"}, 
ViewSpaces {"\\\\.\\root\\cimv2"},
dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Association_SystemViewOperatingSystem
{
    [Direct, key, PropertySources{"GroupComponent"}]
    Win32_ComputerSystem ref Computer;
    
    [key, PropertySources{"PartComponent"}]
    Union_OS_For_AssociationExample ref OperatingSystem;
};
```

 

 




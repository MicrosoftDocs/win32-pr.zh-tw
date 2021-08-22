---
description: 定義自訂屬性。
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: 定義自訂屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b78516913c898e3b3d814e96a40d227cc3cc1cc70c13a290949f91eb9f447c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348048"
---
# <a name="defining-custom-properties"></a>定義自訂屬性

**定義自訂屬性**。

如果 Windows 的影像取得需要 (WIA) 迷你驅動程式來定義自訂屬性，則應該將 [wia \_ 私 \_ 用 DEVPROP] 屬性用於自訂根專案屬性，而 [wia \_ 私用 \_ ITEMPROP] 屬性則應該用於其他專案屬性。 這些常數定義于 *wiadef* 中。

下列範例程式碼顯示三個根專案屬性的定義。 第一個自訂根項目屬性的屬性識別碼（自訂 \_ 根項目 \_ \_ 1）是根據 WIA 私用 \_ DEVPROP 所定義 \_ 。 其他根專案屬性的屬性識別碼是根據 WIA \_ 私用 \_ DEVPROP + 1、wia 私用 \_ \_ DEVPROP + 2 等專案來定義。 如果需要額外的自訂根專案屬性，則可以繼續模式。


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



下一個範例會顯示三個自訂子專案屬性和屬性識別碼的定義。 第一個自訂子專案屬性的屬性識別碼（自訂子系屬性 \_ \_ \_ 1）是根據 WIA 私用 ITEMPROP 所定義 \_ \_ 。 其他子專案屬性的屬性識別碼是根據 WIA \_ 私用 ITEMPROP + 1 等專案來定義 \_ 。 如同之前，如果需要更多的自訂子專案屬性，就可以繼續模式。


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



自訂 WIA 屬性必須有與自訂屬性識別碼相關聯的自訂屬性名稱。 下列範例程式碼顯示三個自訂根專案屬性名稱的定義。  (這些屬性名稱會與上一個範例中所建立的自訂屬性識別碼搭配使用，其中自訂的根項目 1 STR 中包含的自訂屬性名稱 \_ \_ \_ \_ 會與自訂根專案屬性識別碼自訂根 \_ 元素1相關聯 \_ \_ 。 ) 


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> WIA 屬性名稱 *不* 會以多種語言當地語系化。 這是因為使用屬性識別碼或屬性名稱的應用程式可以讀取 WIA 屬性。 如果使用名稱，則它必須是常數，就如同屬性識別碼一樣。

 

 

 




---
description: 您可以使用系統登錄提供者作為實例或屬性提供者。
ms.assetid: 0a8198c0-57c1-4d96-9965-3867c8c0e738
ms.tgt_platform: multiple
title: 使用系統登錄提供者作為屬性提供者
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64fc701843438b4d173b1914ed2ac86214fe685e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978252"
---
# <a name="use-the-system-registry-provider-as-a-property-provider"></a>使用系統登錄提供者作為屬性提供者

您可以使用 [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 作為實例或屬性提供者。

如果您選擇存取屬性提供者介面，則必須標記您的 WMI 類別以指出您的意圖。

**使用 system registry provider 做為屬性提供者**

-   使用 **DynProps**、 [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)和 **PropertyCoNtext** standard 限定詞定義您的 WMI 類別。

    **DynProps** 辨識符號會將類別識別為具有由 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)辨識符號所識別之屬性提供者所維護的屬性。 **PropertyCoNtext** 限定詞會指定屬性要儲存的登錄值名稱。 **PropertyCoNtext** 限定詞的格式與 **ClassCoNtext** 辨識符號的格式相同，具有額外的 *valuename* 和 *運算式* 值。

    ``` syntax
    MACHINE_NAME | Subtree\\KeyPath [|valuename [expression]]
    ```

    *Valuename* 和 *expression* 都是選擇性的。 只有當登錄值具有名稱時，才會使用 *valuename* 設定。 *運算式* 也是選擇性的，並且用於資源描述中繼資料。 如需詳細資訊，請參閱描述登錄的 [資源](describing-a-resource-for-the-registry.md)。

    下列程式碼範例顯示類別如何使用系統登錄提供者做為屬性提供者，以維護其非索引鍵屬性。

    ``` syntax
    [DYNPROPS]
    class PropReg {

        [KEY]  STRING  MyKey;
        STRING Logging;
        STRING Events;
        uint32 Resource1;
    };

    [DYNPROPS]
    instance of PropReg
    {
      MyKey = "a";

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|Logging"), Dynamic, Provider("RegPropProv")]  Logging;

      [PropertyContext("local|hkey_local_Machine\\software\\microsoft\\
       wbem\\cimom|EnableEvents"), Dynamic, Provider("RegPropProv")]
       Events;

      [PropertyContext("local|hkey_local_Machine\\hardware\\
       ResourceMap\\Hardware Abstraction Layer\\PC Compatible Eisa/isa 
       hal|.raw(\"Internal\")(0)(0)(\"interrupt.vector\")"), Dynamic, 
       Provider("RegPropProv")]  Resource1;
    };
    ```

 

 

---
description: 用來保存登錄資料的類別會以數個標準限定詞來定義。
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: 使用限定詞定義登錄類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848745"
---
# <a name="defining-a-registry-class-with-qualifiers"></a>使用限定詞定義登錄類別

用來保存登錄資料的類別會以數個標準限定詞來定義。

以下是標準限定詞的清單：

-   [動態](standard-wmi-qualifiers.md) 和 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)

    您可以將 **動態** 限定詞附加至類別或實例。 **動態** 辨識符號會將類別或實例標示為由提供者動態管理。 當 **動態** 出現在類別或實例上時，也必須顯示 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 限定詞。 **提供者** 辨識符號會識別必須管理動態類別或實例的特定提供者。

-   [ClassCoNtext](standard-wmi-qualifiers.md)

    **ClassCoNtext** 限定詞會附加至類別。 它會指定包含類別所代表之資訊的登錄機碼路徑。

    **ClassCoNtext** 限定詞的格式如下。

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    如果 KeyPath 的值包含含有子機碼的索引鍵，則其值可能很長。

    下列範例顯示包含特定電腦傳輸裝置路徑的 **ClassCoNtext** 限定詞。

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

下列類別定義的範本說明如何使用 **動態**、 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)和 **ClassCoNtext** 的限定詞。 **提供** 者辨識符號所命名的提供者是實例系統登錄提供者。 請注意，登錄路徑不區分大小寫，如同辨識符號名稱。

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

管理應用程式也可以使用系統登錄提供者來取得和修改特定金鑰的登錄資料。

 

 




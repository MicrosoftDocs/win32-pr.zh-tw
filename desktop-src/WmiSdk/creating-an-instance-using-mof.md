---
description: 您可以使用受控物件格式 (MOF) ，在 Windows 管理服務中宣告類別的基本實例。 您也可以覆寫實例的預設值。 如需詳細資訊，請參閱設定實例屬性值。
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: 使用 MOF 建立實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5078c5fcddaab4e8437a33e8cb3210d515360fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975032"
---
# <a name="creating-an-instance-using-mof"></a>使用 MOF 建立實例

您可以使用受控物件格式 (MOF) ，在 Windows 管理服務中宣告類別的基本實例。 您也可以覆寫實例的預設值。 如需詳細資訊，請參閱 [設定實例屬性值](#setting-an-instance-property-value)。

下列程式描述如何使用 MOF 程式碼宣告類別的基本實例。

**使用 MOF 程式碼宣告類別的基本實例**

1.  使用關鍵字的 **實例** ，後面接著類別名稱、大括弧和分號。

    下列程式碼範例顯示如何宣告類別的實例。

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  完成之後，請使用 MOF 編譯器將您的 MOF 程式碼插入 WMI 存放庫。

    如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

類別的實例包含類別的所有屬性。 如果類別是衍生類別，則實例會包含屬於階層中所有較高類別的屬性。 建立實例的每個類別都有一或多個索引鍵屬性。 您無法使用超過256的索引鍵來建立實例。

## <a name="setting-an-instance-property-value"></a>設定實例屬性值

因為 WMI 強型別屬性，所以您無法修改屬性類型。 不過，您可以在實例中設定屬性值。 當類別將預設值指派給屬性時，WMI 會將預設值指派給每個實例。 您可以在實例宣告中覆寫這個值。

下列程式描述如何使用 MOF 程式碼設定屬性值或覆寫預設值。

**使用 MOF 程式碼設定屬性值或覆寫預設值**

1.  在實例宣告的大括弧之間放置指派語句。

    下列程式碼範例顯示如何設定屬性值。

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    WMI 不需要您在建立實例時設定任何屬性。 例外狀況是以 [**金鑰**](key-qualifier.md) 辨識符號標記的任何屬性。 因為 WMI 會使用索引鍵屬性來唯一識別實例，所以您必須在遇到時設定所有索引鍵屬性。 相反地，您不能在實例宣告中設定系統屬性。 相反地，WMI 會在必要時將適當的值指派給系統屬性。

2.  完成之後，請呼叫 MOF 編譯器以將您的 MOF 程式碼插入 WMI 存放庫。

    如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

下列程式碼範例顯示實例如何指定類別所定義之屬性的資料。

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

在上述範例中，類別會定義三個屬性：字元字串、32位帶正負號的整數，以及32位不帶正負號的整數。 實例會提供每個屬性的資料值。

 

 




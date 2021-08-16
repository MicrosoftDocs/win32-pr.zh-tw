---
description: Union view 類別是來源類別實例的邏輯聯集。 Union view 類別包含來源類別的所有實例，除非您在來源查詢中包含 WHERE 子句，以限制實例。
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: 建立聯集視圖類別
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3408e3aaec9ee809711b3f400c77ffab5ab2b376eaace3311bd0367f61937c30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612388"
---
# <a name="creating-a-union-view-class"></a>建立聯集視圖類別

Union view 類別是來源類別實例的邏輯聯集。 Union view 類別包含來源類別的所有實例，除非您在來源查詢中包含 WHERE 子句，以限制實例。

當您想要查看位於不同命名空間或不同電腦上的類似或相同類別的實例時，聯集視圖類別相當有用。 例如，您可以建立包含要監視之不同磁片磁碟機實例的聯集類別。

您也可以將等位視圖類別的屬性作為所有來源類別實例中不存在的屬性作為基礎。 如果來源類別實例沒有相同的屬性，則 union 類別實例的屬性值為 **Null**。 例如，如果某個硬碟機有 **溫度** 屬性，但另一個硬碟沒有，您仍然可以建立兩者之間的聯集。

下列程式描述如何建立聯集視圖類別。

**若要建立聯集視圖類別**

1.  使用聯 [**集**](qualifiers-specific-to-the-view-provider.md) 字串辨識符號來開始您的類別定義。

    [**JoinOn**](qualifiers-specific-to-the-view-provider.md)、 **Association** 和 **Union** 限定詞都是互斥的。

2.  建立查詢，以使用 [**ViewSources**](viewsources-qualifier.md) 限定詞來定義 view 類別中所使用的來源類別。
3.  使用 [**ViewSpaces**](viewspaces-qualifier.md) 限定詞來定義來源類別所在之命名空間的名稱和位置。
4.  使用 [**PropertySources**](propertysources-qualifier.md) 限定詞，定義對應至來源類別中屬性的屬性。

    如有必要，您可以使用 [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) 限定詞，將任何屬性標記為屬於來源類別。

5.  定義您的等位視圖類別之來源類別的索引鍵屬性。

    每個來源類別都必須有與 [**CIMType**](swbemproperty-cimtype.md)相符的相同索引鍵屬性數目。 此外，您的等位視圖類別的索引鍵必須可唯一識別所有來源實例。 在某些情況下，您可能需要指定系統屬性，以確保實例是唯一的。 例如，如果您在兩個不同的命名空間中，從兩個相同類別的聯集建立一個視圖，您可以在 view 類別中包含 [**\_ \_ Namespace**](--namespace.md)屬性做為索引鍵，以區分這兩個實例。 如果您在相同的命名空間中使用兩個類似的類別來建立視圖，則可以使用 **\_ \_ 類別** 屬性來區分兩者。 重新命名視圖中的任何系統屬性，讓您可以避免與 view 類別的系統屬性發生衝突。

6.  使用 [**MethodSource**](qualifiers-specific-to-the-view-provider.md) 限定詞定義任何您想要的方法。

    不同于其他視圖類別，您可以建立方法來修改聯集視圖。

下列程式碼範例描述聯集視圖類別。

``` syntax
[Union, ViewSources{"SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM LocalDisk", 
    "SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM RemoteDisk"}, 
    ViewSpaces{"\\\\.\\Root\\LocalNamespace","\\\\.\\Root\\RemoteNamespace"}, 
    dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class UnionOfDrives

{
    [PropertySources{"Description", "Description"}] string des;
    [PropertySources{"DeviceID", "DeviceID"}, key] String did;
    [PropertySources{"__Namespace", "__Namespace"}, key] String KEYID;
    [PropertySources{"FileSystem", "FileSystem"}] String fsystem ;
    [PropertySources{"FreeSpace", "FreeSpace"}] uint64 fspace;
    [PropertySources{"VolumeName", "VolumeName"}] String vname;
};
```

 

 




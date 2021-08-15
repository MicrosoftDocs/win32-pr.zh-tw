---
description: ICEM10 會確認合併模組只包含屬性資料表中允許的屬性。
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bb9634ecec212954031e665fa0ebdc3c19856a9bcd02d894eb6e579455d059b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129408"
---
# <a name="icem10"></a>ICEM10

ICEM10 會確認合併模組只包含 [屬性資料表](property-table.md)中允許的屬性。 屬性工作表中不允許下列產品特定屬性：

-   [**ProductLanguage 屬性**](productlanguage.md)
-   [**ProductCode 屬性**](productcode.md)
-   [**ProductVersion 屬性**](productversion.md)
-   [**ProductName 屬性**](productname.md)
-   [**Manufacturer 屬性**](manufacturer.md)

## <a name="result"></a>結果

當合併模組包含 [屬性資料表](property-table.md)中不允許的屬性時，ICEM10 會張貼錯誤。

## <a name="example"></a>範例

ICEM10 會針對包含所顯示資料庫專案的模組，張貼下列錯誤訊息。

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

下表顯示部分 [屬性資料表](property-table.md)。



| 屬性                                   | 值    |
|--------------------------------------------|-----------|
| Color                                      | 紅色       |
| [**製造商**](manufacturer.md)       | Microsoft |
| [**ProductLanguage**](productlanguage.md) | 1033      |



 

下列程式說明如何修正錯誤。

**若要修正錯誤**

1.  從 [屬性工作表](property-table.md)中移除「[**製造商**](manufacturer.md)」屬性。
2.  從 [屬性資料表](property-table.md)中移除 '[**ProductLanguage**](productlanguage.md)' 屬性。

## <a name="table-used-during-execution"></a>執行期間所使用的資料表

在執行期間，會使用 [屬性資料表](property-table.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 




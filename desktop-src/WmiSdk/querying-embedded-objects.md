---
description: 查詢包含内嵌物件的事件類別時，您有幾個選項可供查詢所用的表單使用。 查詢所傳回的結果會根據您所使用的查詢格式而有所不同。
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: 查詢内嵌物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed2e13bd9d9dc798891a723a6fed1b1734e1735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692204"
---
# <a name="querying-embedded-objects"></a>查詢内嵌物件

查詢包含内嵌物件的事件類別時，您有幾個選項可供查詢所用的表單使用。 查詢所傳回的結果會根據您所使用的查詢格式而有所不同。

## <a name="class-definitions"></a>類別定義

下列範例顯示在本主題中用於 WQL 查詢的類別定義。

``` syntax
class MyClass
{
   string Prop1;
   string Prop2;
};

class MyEvent : __ExtrinsicEvent
{
   MyClass E1;
   MyClass E2;
};
```

## <a name="examples"></a>範例

下列查詢會傳回內嵌式類別（ **E1** 和 **E2**），每個都有 **Prop1** 和 **this.prop2** 填入資料。

`SELECT * FROM MyEvent`

下列查詢會傳回 **E1** embedded 物件，但 **Prop1** 和 **this.prop2** 都不會填入資料。

`SELECT E1 FROM MyEvent`

下列查詢會傳回內嵌類別 **E1** ，其中只包含填入資料的 **Prop1** 。

`SELECT E1.Prop1 FROM MyEvent`

下列查詢會傳回內嵌式類別（ **E1** 和 **E2**），每個都有 **Prop1** 和 **this.prop2** 填入資料。

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

這相當於使用星號 () 的第一個查詢， \* 而不是指定每個物件和屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 WQL 查詢](querying-with-wql.md)
</dt> </dl>

 

 




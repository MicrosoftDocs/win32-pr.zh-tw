---
description: ICE52 會檢查 AppSearch 資料表中的私用屬性。 請參閱關於屬性。
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96f514f38e44a802b092acff53ac14f10c5e5d32c03888b7d45540443d34be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044038"
---
# <a name="ice52"></a>ICE52

ICE52 會檢查 [AppSearch 資料表](appsearch-table.md)中的私用屬性。 請參閱 [關於屬性](about-properties.md)。

使用 Windows 2000 時，AppSearch 資料表的屬性資料行中設定的所有屬性都必須是公用屬性。

## <a name="result"></a>結果

如果 AppSearch 資料表中有私用屬性，ICE52 會張貼警告。

## <a name="example"></a>範例

ICE52 會針對所顯示的範例張貼下列警告。

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[AppSearch 資料表](appsearch-table.md)



| 屬性  | 簽名  |
|-----------|------------|
| PROPERTY1 | Signature1 |
| Property2 | Signature2 |



 

若要修正自訂公用屬性的這個警告變更： PROPERTY2。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




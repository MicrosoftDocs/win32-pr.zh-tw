---
description: ICE52 會檢查 AppSearch 資料表中的私用屬性。 請參閱關於屬性。
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851175"
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

 

 




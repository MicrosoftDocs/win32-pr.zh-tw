---
description: ICE11 可搭配並行安裝使用。 不建議將並行安裝用於安裝應用程式，以供公開發行。 如需並行安裝的詳細資訊，請參閱並行安裝。
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944537"
---
# <a name="ice11"></a>ICE11

ICE11 可搭配並行安裝使用。 不建議將並行安裝用於安裝應用程式，以供公開發行。 如需並行安裝的詳細資訊，請參閱 [並行安裝](concurrent-installations.md)。

## <a name="result"></a>結果

ICE11 會驗證並行安裝自訂動作之 [CustomAction 資料表](customaction-table.md) 的來源資料行。 來源資料行必須包含 (MSI 產品代碼) 的有效 [GUID](guid.md) 。

如果 CustomAction 資料表的來源資料行針對並行安裝自訂動作所撰寫的錯誤，ICE11 會張貼錯誤。

## <a name="example"></a>範例

ICE 會針對所顯示的範例張貼下列錯誤訊息。

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

[屬性工作表](property-table.md) (部分) 



| 屬性        | 值                                  |
|-----------------|----------------------------------------|
| **ProductCode** | {BFB69273-F0AE-45C4-9853-0AF946714768} |



 

[CustomAction 資料表](customaction-table.md) (部分) 



| CustomAction | 類型 | 來源                                 |
|--------------|------|----------------------------------------|
| CA1          | 39   | {BFB69273-F0AE-45C4-9853-0AF946714768} |
| CA2          | 39   | {BFB69273-F0AE-55c5-9853-0AF946714768} |
| CA3          | 39   | {BFB69273-F0AE-66C6-9853-0AF946714768} |
| CA4          | 39   | ProductCode                            |



 

若要修正錯誤，在 CA1 中，您無法同時安裝「基底套件」。 這會導致遞迴安裝。 您應該移除此專案，或是將來源資料行變更為與基底套件的 GUID 不同的已公告 MSI 的 GUID。 若為 CA2，請將 GUID 的所有字元設為大寫。 最後，將 CA4's 來源資料行變更為參考公告 MSI 的有效 GUID。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[並行安裝](concurrent-installations.md)
</dt> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




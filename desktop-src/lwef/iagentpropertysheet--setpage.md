---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120743"
---
# <a name="iagentpropertysheetsetpage"></a>IAgentPropertySheet::SetPage

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

設定 Microsoft Agent 屬性工作表的目前頁面。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*
</dt> <dd>

設定屬性目前頁面的 BSTR。 參數可以是下列其中一項。



|                 | 描述            |
|-----------------|------------------------|
| **詞性**    | 語音輸入頁面。 |
| **出**    | 輸出頁面。       |
| **版權法** | 著作權頁面。    |



 

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentPropertySheet::GetPage**](iagentpropertysheet--getpage.md)


 

 





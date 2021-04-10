---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673768"
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



|                 |                        |
|-----------------|------------------------|
| **詞性**    | 語音輸入頁面。 |
| **出**    | 輸出頁面。       |
| **版權法** | 著作權頁面。    |



 

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentPropertySheet::GetPage**](iagentpropertysheet--getpage.md)


 

 





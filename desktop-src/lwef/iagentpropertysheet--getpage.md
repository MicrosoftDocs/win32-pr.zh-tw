---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372261"
---
# <a name="iagentpropertysheetgetpage"></a>IAgentPropertySheet::GetPage

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

抓取 Microsoft Agent 屬性工作表的目前頁面。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*
</dt> <dd>

如果視窗未開啟) ，則為接收屬性工作表目前頁面 (上次查看頁面的變數位址。 參數可以是下列其中一項：



|                 |                        |
|-----------------|------------------------|
| **詞性**    | 語音輸入頁面。 |
| **出**    | 輸出頁面。       |
| **版權法** | 著作權頁面。    |



 

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentPropertySheet::SetPage**](iagentpropertysheet--setpage.md)


 

 





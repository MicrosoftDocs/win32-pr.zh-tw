---
title: IAgentCharacterEx GetAutoPopupMenu
description: IAgentCharacterEx GetAutoPopupMenu
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b9e23f9c8d9f6fefcc7b2606ebd18ab31ff93c8f8f82c1faf692f92545662d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477976"
---
# <a name="iagentcharacterexgetautopopupmenu"></a>IAgentCharacterEx::GetAutoPopupMenu

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetAutoPopupMenu(
   long * pbAutoPopupMenu  // address of auto pop-up menu display setting
);
```

抓取伺服器是否自動顯示字元的快顯功能表。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*
</dt> <dd>

如果 Microsoft 代理程式伺服器自動處理顯示字元的快顯功能表，則為收到 **True** 之變數的位址，否則為 **False** 。

</dd> </dl>

當這個屬性設定為 **False** 時，您的應用程式必須使用 [**IAgentCharacterEx：： ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) 方法來顯示快顯功能表。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx：： SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)、 [ **IAgentCharacterEx：： ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 





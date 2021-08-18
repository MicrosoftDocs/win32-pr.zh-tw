---
title: IAgentCharacterEx SetAutoPopupMenu
description: IAgentCharacterEx SetAutoPopupMenu
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a616bd95836d8f8131aaccabe0bb6db4f35a5caf22c480c17908935d80f2b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477956"
---
# <a name="iagentcharacterexsetautopopupmenu"></a>IAgentCharacterEx::SetAutoPopupMenu

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

設定伺服器是否自動顯示字元的快顯功能表。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*
</dt> <dd>

自動快顯功能表顯示旗標。 如果此參數為 **True**，當使用者以滑鼠右鍵按一下字元或字元的工作列圖示時，Microsoft Agent 會自動顯示該字元的快顯功能表。

</dd> </dl>

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

藉由將這個屬性設定為 **False**，您就可以建立自己的功能表處理行為。 若要在將這個屬性設定為 **False** 之後顯示功能表，請使用 [**IAgentCharacterEx：： ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) 方法。

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx：： GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md)、 [ **IAgentCharacterEx：： ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 





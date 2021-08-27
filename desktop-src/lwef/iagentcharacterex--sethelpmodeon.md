---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacbdf9c0ea9737bb73ba7a99e0839e1435379e42536a82aa30c2ca034a28860
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062028"
---
# <a name="iagentcharacterexsethelpmodeon"></a>IAgentCharacterEx::SetHelpModeOn

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

為字元設定即時線上說明模式。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*
</dt> <dd>

說明模式旗標。 如果此參數為 **True**，Microsoft Agent 會開啟字元的說明模式。

</dd> </dl>

當您將這個屬性設定為 **True** 時，滑鼠指標會在移至字元上方或移至字元的快顯功能表時，變更為內容相關的說明影像。 當使用者按一下或拖曳字元，或在字元的快顯功能表中按一下專案時，伺服器會觸發 [**IAgentNotifySinkEx：： HelpComplete**](iagentnotifysinkex--helpcomplete.md) 事件並離開說明模式。

在 [說明] 模式中，除非 [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md)屬性傳回 **True**，否則伺服器不會傳送 [**Click**](click-event.md)、 [**DragStart**](/windows/desktop/lwef/dragstart-event)、 [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)和 [**命令**](command-event.md)事件。 在這種情況下，伺服器會傳送 **Click** 事件 (不會離開說明模式) ，而只是針對滑鼠右鍵，如此您就可以顯示快顯功能表。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx：： GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md)、 [ **IAgentNotifySinkEx：： HelpComplete**](iagentnotifysinkex--helpcomplete.md)


 

 
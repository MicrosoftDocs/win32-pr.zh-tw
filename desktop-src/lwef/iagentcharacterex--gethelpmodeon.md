---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb78cf535fbfd7e28ab797c887c8e1548d3fd18dce03fb6b64d888c7e304c0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750783"
---
# <a name="iagentcharacterexgethelpmodeon"></a>IAgentCharacterEx::GetHelpModeOn

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

抓取是否為字元的即時線上說明模式。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*
</dt> <dd>

如果字元的說明模式為 on，則為收到 **True** 之變數的位址，否則為 **False** 。

</dd> </dl>

當這個屬性設定為 **True** 時，滑鼠指標會在移至字元上方或移至字元的快顯功能表時，變更為內容相關的說明影像。 當使用者按一下或拖曳字元，或在字元的快顯功能表中按一下專案時，伺服器會觸發 [**IAgentNotifySinkEx：： HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) 事件並離開說明模式。

在 [說明] 模式中，除非 [**ragcomplete**](https://www.bing.com/search?q=**GetAutoPopupMenu**)屬性傳回 **True**，否則伺服器不會傳送 [**IAgentNotifySink：： Click**](iagentnotifysink--click.md)、 [**IAgentNotifySink：:D Ragstart**](iagentnotifysink--dragstart.md)、 [**IAgentNotifySink：:D IAgentNotifySink**](iagentnotifysink--dragcomplete.md)和 [**GetAutoPopupMenu：：命令**](iagentnotifysink--command.md)事件。 在這種情況下，伺服器會傳送 **IAgentNotifySink：： Click** 事件 (不會離開說明模式) ，而只有滑鼠右鍵可讓您顯示快顯功能表。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)


 

 





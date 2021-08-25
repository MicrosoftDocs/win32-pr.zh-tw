---
description: 顯示輸入面板的總覽。
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: 顯示輸入面板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f491a8b2ddcea42588c38f7cfa7106a2e8f48ff1849ab8cd406718511a4cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940788"
---
# <a name="displaying-the-input-panel"></a>顯示輸入面板

\[針對 managed 程式碼) ， [**PenInputPanel**](peninputpanel-class.md)已被 [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([>textinput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) 。 請參閱 [文字輸入面板](programming-the-text-input-panel.md)的程式設計。\]

控制項的各種焦點事件順序如下所示：

-   [控制項。輸入](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [控制項. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [控制項。離開](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [控制。正在驗證](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [控制項。已驗證](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [控制項. LostFocus](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

控制項中設定控制項時，並不保證控制項的焦點是由 [控制項所](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) 撰寫。 [請輸入](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) 事件處理常式。 控制項。輸入事件是將 [PenInputPanel](/previous-versions/ms583923(v=vs.100)) 物件附加至控制項的最佳位置，但 [control。 GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) 事件是變更 [PenInputPanel Visible](/previous-versions/ms571984(v=vs.100)) 屬性的最佳位置。

 

 

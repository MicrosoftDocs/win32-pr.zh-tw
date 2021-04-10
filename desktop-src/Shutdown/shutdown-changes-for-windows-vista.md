---
description: 下表摘要說明 Windows Vista 和 Windows XP 關機之間的差異。
ms.assetid: da7985d2-85c8-47e1-a172-c9e92f450e24
title: Windows Vista 的關機變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e04bb20099349ce378384cf01c39e53ca03a896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026801"
---
# <a name="shutdown-changes-for-windows-vista"></a>Windows Vista 的關機變更

下表摘要說明 Windows Vista 和 Windows XP 關機之間的差異。



| 功能                 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                | Windows Vista                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 封鎖關機       | 應用程式可能會延遲5秒回應 [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) ，然後系統可讓使用者終止應用程式。 傳回 **TRUE** 以回應 **wm \_ QUERYENDSESSION** 的應用程式，可能會延遲5秒回應 [**wm \_ ENDSESSION**](wm-endsession.md) ，然後系統可讓使用者終止應用程式。 | 應用程式可能會延遲5秒回應 [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) ，然後系統可讓使用者繼續或取消關機。 傳回 **TRUE** 以回應 **wm \_ QUERYENDSESSION** 的應用程式，可能會延遲5秒回應 [**wm \_ ENDSESSION**](wm-endsession.md) ，然後系統可讓使用者繼續或取消關機。                                                                                                      |
| 取消關機      | 如果應用程式在回應 [**WM \_ QUERYENDSESSION**](wm-queryendsession.md)時傳回 **FALSE** ，在大部分情況下都會取消關閉。 但是，不會顯示任何 UI，因此使用者可能不會察覺到關機已取消。                                                                                                                                                      | 如果應用程式傳回 **FALSE** 以回應 [**WM \_ QUERYENDSESSION**](wm-queryendsession.md)，它仍然會出現在關機 UI 中。 請注意，系統不允許沒有可見視窗的主控台應用程式或應用程式取消關閉。 如果這些應用程式不會在5秒內回應 **wm \_ QUERYENDSESSION** 或 [**WM \_ ENDSESSION**](wm-endsession.md) ，或在回應 **wm \_ QUERYENDSESSION** 時傳回 **FALSE** ，則會自動終止這些應用程式。 |
| 關機使用者介面 | 系統會顯示每個應用程式封鎖關機的對話方塊。 如果使用者按一下 [ **立即結束** ] 按鈕，就會終止應用程式。 如果使用者按一下 [ **取消** ] 按鈕，就會取消關機，而應用程式會繼續執行。                                                                                                                                    | 系統會顯示全螢幕 UI，可識別封鎖關機的所有應用程式，以及其在使用 [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)) 註冊原因時 (的原因。                                                                                                                                                                                                                                                                    |



 

## <a name="best-practices"></a>最佳做法

-   應用程式不應封鎖關機。 儘快回應 [**wm \_ QUERYENDSESSION**](wm-queryendsession.md) ，並延後清除活動，直到處理 [**WM \_ ENDSESSION**](wm-endsession.md) 訊息為止。
-   必須封鎖關機的應用程式應該使用新的 [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) 函式來註冊說明使用者原因的字串。 使用者可以決定是要繼續還是取消關機。
-   應用程式無法依賴無法封鎖關機。

 

 




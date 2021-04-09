---
description: Windows Installer 包含在動作顯示對話方塊中顯示進度指標的功能。
ms.assetid: cfc2d974-4f2d-4f52-9835-eab1dc091c9b
title: 撰寫 ProgressBar 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b872ed2dd36fb8ed04ee48fd69e4680fce002a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848961"
---
# <a name="authoring-a-progressbar-control"></a>撰寫 ProgressBar 控制項

Windows Installer 包含在動作顯示對話方塊中顯示進度指標的功能。 [ProgressBar 控制項會](progressbar-control.md)以圖形表示個別元件的安裝，以及報表在安裝完成之前，相對於剩餘時間或大約總剩餘時間的總時間。

為了判斷安裝所預期的總時間，安裝程式會在執行腳本產生期間追蹤每個動作所預期的總進度刻度。 當腳本產生完成時，會儲存進度滴答總計，並開始安裝。

詳細說明進度刻度數量的進度訊息會傳送至使用中的訊息處理常式，因為腳本中的每個動作都會執行。 在每個進度訊息中，安裝程式會將 [SetProgress ControlEvent](setprogress-controlevent.md) 廣播到目前作用中的對話方塊。 在腳本執行期間，您應該撰寫 UI 順序來建立動作顯示對話方塊，以接收來自安裝程式的 SetProgress ControlEvent 訊息。

當 [動作顯示] 對話方塊收到 SetProgress ControlEvent 時，它會檢查 [EventMapping 資料表](eventmapping-table.md) 是否有任何訂閱該 ControlEvent 的控制項。 [動作顯示] 對話方塊上的 ProgressBar 控制項是使用 [屬性] 資料行中指定的進度控制項屬性訂閱。 進度控制項屬性指定 ProgressBar 控制項將會傳遞 "ticksSoFar" 和 "totalTicks" 值，以及 SetProgress ControlEvent。 進度列控制項使用這種資訊，從左至右將安裝和從右至左往左移動圖形列，以進行 [復原](rollback-installation.md) 作業。

此外，安裝程式會在每個進度訊息上廣播 [TimeRemaining ControlEvent](timeremaining-controlevent.md) 。 安裝的剩餘時間總計是藉由先計算執行速率來決定，也就是已耗用的總滴答數除以安裝開始之後的總時間。 剩餘的總刻度除以執行速率，可提供大約的剩餘時間。

當動作顯示對話方塊收到 TimeRemaining ControlEvent 時，它會再次在 EventMapping 資料表中尋找任何已訂閱的控制項。 為了顯示剩餘的時間，必須使用 [屬性] 資料行中指定的[TimeRemaining 控制項屬性](timeremaining-control-attribute.md)，將[文字控制項](text-control.md)訂閱給 TimeRemaining ControlEvent。

訂閱的文字控制項會查詢 [UIText 資料表](uitext-table.md) 中名為 "TimeRemaining" 的參數化範本字串。 這個字串有兩個參數， \[ 1 \] 表示分鐘， \[ 2 \] 秒。 文字控制項會將每個值轉換為分鐘和秒，並評估 TimeRemaining 範本字串，並以新的資訊更新文字控制項。

如果 UI 顯示層級設定為 [基本] 或 [較低]，安裝程式會顯示預設對話方塊，其中包含進度列和 [TimeRemaining 文字] 欄位。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

 

 




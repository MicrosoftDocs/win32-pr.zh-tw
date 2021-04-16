---
description: 下列範例說明如何撰寫會彈出的條件訊息方塊，並警告使用者在使用者提前啟用顯示的控制項時，背景工作仍在執行中。
ms.assetid: 4a99a96b-50c2-42eb-82ad-acdfa186a71f
title: 撰寫「請稍候。 . ." 訊息方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5f0cb1e4f1a0224c3b71d42d6fc63c1940483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513237"
---
# <a name="authoring-a-conditional-please-wait-message-box"></a>撰寫條件式「請稍候 ...」訊息方塊

下列範例說明如何撰寫會彈出的條件訊息方塊，並警告使用者在使用者提前啟用顯示的控制項時，背景工作仍在執行中。

此範例也會說明如何使用 [SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) 來保護會觸發動作的控制項，而該控制項會根據背景工作完成而觸發動作。

在此範例中，包含三個按鈕控制項的 [選項對話方塊](selection-dialog.md) ，在安裝過程中，會對使用者顯示標示為 [ **立即安裝** **]、[下一步]** 和 [ **磁片費用** ]。 但是，安裝程式在顯示此對話方塊時，也會在背景中執行磁碟空間的成本工作。 作者希望從啟用中保護這些按鈕，並希望當使用者在完成成本之前按一下任何按鈕時，想要有 [請等候] 訊息方塊。 作者也希望這個訊息方塊包含 [ **取消** ] 按鈕，並在背景工作完成時立即消失。

**顯示對話方塊，要求使用者在背景磁片成本已完成時等候**

1.  您可以使用安裝程式的撰寫功能，將名為 **WaitForCosting** 的新強制回應對話方塊新增至 [對話方塊資料表](dialog-table.md)中。 對話方塊應該會顯示文字字串，指出「請稍候，正在完成磁碟空間的成本。」
2.  將單一推播按鈕控制項新增至這個對話方塊，並將其撰寫至 [控制項資料表](control-table.md)，以將其標示為 [**取消**]。
3.  將 **「取消」** 推播按鈕連結到 ControlEvent，藉由在 [ControlEvent 資料表](controlevent-table.md)中撰寫 [EndDialog ControlEvent](enddialog-controlevent.md)來關閉 [ **WaitForCosting** ] 對話方塊。 將 EndDialog 控制項事件的引數設定為 Exit。
4.  將 [SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md)連結至 [**立即安裝**]、 **[下一步**]，以及顯示在 [[選取範圍] 對話方塊](selection-dialog.md)中的 [**磁片成本**] 推播按鈕控制項。 將 [ControlEvent] 資料表中這個 ControlEvent 的引數設定為 [ **WaitForCosting** ] 對話方塊，並將資料表的 [條件] 資料行中的運算式設為： [**CostingComplete**](costingcomplete.md) = 1。

 

 




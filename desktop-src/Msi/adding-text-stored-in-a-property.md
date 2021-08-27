---
description: 《撰寫條件 &0034 》一節中所述的範例 \# ：請稍候。
ms.assetid: b563e306-6d10-4298-9a71-9e749224ccd2
title: 加入儲存在屬性中的文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 965a90c5e0701c54959bb4eae26b26c07ad7b4cbae8aefa6bdf346542b6a5cf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105448"
---
# <a name="adding-text-stored-in-a-property"></a>加入儲存在屬性中的文字

標題為「撰寫條件式」一節中所述的範例， [請稍候 .。。「訊息方塊](authoring-a-conditional-please-wait-------message-box.md) 會顯示一個對話方塊，其中包含下列文字：「請稍候，磁碟空間的成本已完成」。 只要將 [文字控制項](text-control.md) 放在對話方塊上，然後在 [控制項資料表](control-table.md)的文字資料行中輸入文字字串，就可以完成這項工作。 在此情況下，字型樣式的相關資訊必須內嵌在字串中。 作者必須在字元字串前面加上 {style} 來設定字型和字型樣式 \\ **。 其中 *style* 是在文字文字 [資料表](textstyle-table.md)的文字資料行中所列的字型樣式識別碼。 在 [安裝範例](an-installation-example.md)中，會說明此新增文字的方法數次。

使用者介面的作者也可以將文字儲存在屬性中。 下列範例將說明這一點，並顯示如何使用事件顯示替代文字字串。

當背景工作正在執行時，此範例中的目標會再次出現 **WaitForCosting** 對話方塊。 與新案例的差異在於，如果使用者取消 [ **WaitForCosting** ] 對話方塊，然後嘗試在背景工作第二次完成之前啟動控制項，則 [ **WaitForCosting** ] 方塊會再次顯示替代訊息：「磁碟空間的成本仍在執行中。 您可以繼續等候，或返回主要選取方塊來結束此順序。」

**顯示顯示替代訊息的 [請稍候] 對話方塊**

1.  首先，將 [條件式 **WaitForCosting** ] 對話方塊新增至選取專案對話方塊，如 [撰寫條件式「請稍候」所述：] 訊息方塊](authoring-a-conditional-please-wait-------message-box.md)。
2.  藉由在 [控制資料表](control-table.md)中撰寫記錄，將 [文字控制項](text-control.md)放在 [ **WaitForCosting** ] 對話方塊上。 在對話方塊資料行中，輸入 **WaitForCosting** 對話方塊的識別碼 \_ 。 在控制項資料行中輸入文字控制項的識別碼。 將控制項的類型指定為類型資料行中的文字。
3.  在[控制資料表](control-table.md)的 X 和 Y 資料行中輸入控制項左上角的水準和垂直座標，以指定文字控制項的[位置控制項屬性](position-control-attribute.md)。 使用圖元作為距離單位。
4.  在 [控制資料表](control-table.md)的 [寬度] 和 [高度] 資料行中輸入這些維度，以指定文字控制項的寬度和高度。 使用圖元作為長度單位。
5.  控制資料表的下一個資料行的屬性和控制 \_ 不會影響文字控制項，在此情況下可以保留空白。
6.  指定與位旗標相關聯之文字控制項的控制項屬性。 將個別位值加在一起，然後將總計輸入控制資料表的 [屬性] 資料行中。 這些是 [可見](visible-control-attribute.md)、 [凹陷](sunken-control-attribute.md)、 [啟用](enabled-control-attribute.md)、 [透明](transparent-control-attribute.md)、 [NoWrap](nowrap-control-attribute.md)和 [NoPrefix](noprefix-control-attribute.md) 控制項屬性。 在不透明背景上顯示文字控制項的位組合，其中換行文字為0，因此輸入0或將 [屬性] 資料行保留空白。
7.  控制資料表的文字資料行可以保留空白。 文字控制項會顯示文字字串，也就是 [文字](text-control-attribute.md) 控制項屬性的值。 設定這個屬性的方法會在此程式的後續步驟中描述。
8.  在 [屬性資料表](property-table.md) 中加入記錄，以定義 FirstMessage 訊息屬性。 這個屬性是一個字串，其中包含第一個訊息的字型樣式和文字。 在 [屬性] 資料行中輸入名稱 FirstMessage。 在 [值] 欄中，輸入字串： "{ \\ WaitStyle} 請稍候，正在完成磁碟空間的成本。" 其中 WaitStyle 是文字文字 [資料表](textstyle-table.md)之文字資料行中所列其中一個字型樣式的識別碼。
9.  在 [屬性資料表](property-table.md) 中加入記錄，以定義 SecondMessage 訊息屬性。 這個屬性是一個字串，其中包含第二個訊息的字型樣式和文字。 在 [屬性] 資料行中輸入名稱 SecondMessage。 在 [值] 資料行中，輸入字串： "{ \\ WaitStyle} 磁碟空間的成本仍在執行中。 您可以繼續等候，或返回主要選取方塊來結束此順序。」
10. 在 [屬性資料表](property-table.md) 中加入記錄，以定義 WaitMessage 訊息屬性。 這個屬性是一個字串，其中包含 **WaitForCosting** 對話方塊中顯示之訊息的字型樣式和文字（如果使用者嘗試在完成成本之前啟用推播按鈕）。 在 [屬性] 資料行中輸入名稱 WaitMessage。 在屬性資料表的 [值] 資料行中，輸入： FirstMessage。
11. 將 [SetProperty ControlEvent](setproperty-controlevent.md) 新增至 [ControlEvent 資料表](controlevent-table.md) ，每次開啟 **新的選取** 對話方塊時，就會將 WaitMessage 初始化為 FirstMessage。 在對話方塊的 [選取範圍] 對話方塊中，輸入對話方塊的識別碼，此對話方塊位於對話方塊資料行中 \_ 。 在此對話方塊上輸入控制項的識別碼，此對話方塊可用來開啟 [選取範圍] 對話方塊至控制項資料 \_ 行。 \[ \] 在事件資料行中輸入 WaitMessage。 \[ \] 在 [引數] 資料行中輸入 FirstMessage。 在 [條件] 資料行中輸入1，並將 [排序] 資料行保留空白。
12. 將 [SetProperty ControlEvent](setproperty-controlevent.md) 新增至 [ControlEvent 資料表](controlevent-table.md) ，以將 Waitmessage 設定為 SecondMessage。如果使用者在完成磁碟空間的成本之前關閉 **WaitForCosting** 對話方塊。 在對話方塊資料行中，輸入 **WaitForCosting** 對話方塊的識別碼 \_ 。 在控制項資料行中輸入文字控制項的識別碼 \_ 。 \[ \] 在事件資料行中輸入 WaitMessage。 \[ \] 在 [引數] 資料行中輸入 SecondMessage。 在 [條件] 資料行中輸入 NOT [**CostingComplete**](costingcomplete.md) ，並將 [排序] 資料行保留空白。
13. 下列步驟會將文字控制項屬性連結至 ControlEvent，以產生 **WaitForCosting** 對話方塊。 這會讓安裝程式在每次使用者開啟 [ **WaitForCosting** ] 對話方塊時，將 WaitMessage 屬性的值傳遞給文字控制項屬性。
14. 將文字控制項的文字控制項屬性訂閱至 [SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) ，藉由將記錄加入 [EventMapping 資料表](eventmapping-table.md)來開啟 [ **WaitForCosting** ] 對話方塊。 在對話方塊資料行中，輸入 **WaitForCosting** 對話方塊的識別碼 \_ 。 在控制項資料行中輸入文字控制項的識別碼 \_ 。 在事件資料行中輸入 SpawnWaitDialog。 在 EventMapping 資料表的 [屬性] 資料行中輸入文字（文字控制項屬性的識別碼）。

 

 




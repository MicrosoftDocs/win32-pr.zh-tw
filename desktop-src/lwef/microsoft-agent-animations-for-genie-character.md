---
title: 適用于瓶精靈字元的 Microsoft Agent 動畫
description: 適用于瓶精靈字元的 Microsoft Agent 動畫
ms.assetid: 56c42d7a-32af-47cb-8578-0a89507a41ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f583fc6540b5fe13cc157542d69352a8ea5b31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375312"
---
# <a name="microsoft-agent-animations-for-genie-character"></a>適用于瓶精靈字元的 Microsoft Agent 動畫

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

[Microsoft Agent 瓶精靈字元](https://www.microsoft.com/downloads/details.aspx?FamilyID=da86ba4e-bc2d-4c1d-b5a0-3183fe206414)是 Microsoft Corporation 的受版權保護工作。

瓶精靈支援下表所列的動畫。 如需如何呼叫字元動畫的詳細資訊，請參閱 [Microsoft 代理程式伺服器介面程式設計](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) 和 [Microsoft Agent 控制項程式設計](programming-the-microsoft-agent-control.md) 。

如果使用 HTTP 通訊協定和控制項的 [**Get**](get-method.md) 或 Server 的 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法來存取這些字元動畫，請考慮您將如何下載這些字元動畫。 您可能會想要先取出 **顯示** 和 **說話** 狀態動畫，而不是一次下載所有動畫。 這可讓您快速顯示字元，並讓它說話，並以非同步方式關閉其他動畫。 此外，若要確保字元和動畫資料載入成功，請使用 [**RequestComplete**](requestcomplete-event.md) 事件。 如果載入要求失敗，您可以重試載入資料或顯示適當的訊息。

如果動畫的傳回動畫是使用「結束分支」**定義的，** 您就不需要明確地呼叫它。代理程式會在下一個動畫之前自動播放 **傳回動畫。** 但是，如果有列出傳回的動畫，您必須在另一個動畫之前使用 [**Play**](play-method.md)方法來 **呼叫動畫，** 以提供順暢的轉換。 如果未 **列出任何傳回** 動畫，則動畫通常會結束，而不需要過渡動畫。

字元檔包含某些動畫的音效效果，如下表所述。 只有在 Microsoft Agent 屬性工作表中啟用這個選項時，才會播放音效效果。 您也可以在應用程式中停用音效效果。



| 動畫                 | 返回動畫         | 支援說話 | 音效 | 指派至狀態                            | Description                                                    |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|----------------------------------------------------------------|
| **承認**           | 無                     | No                | **否**        | 無                                         | 節點 head                                                      |
| **警示**                 | 是，使用結束分支 | Yes               | **否**        | **聽**                                | Straightens 並引發眉毛                                |
| **宣佈**              | 是，使用結束分支 | Yes               | **否**        | 無                                         | 引發手                                                    |
| **Blink**                 | 無                     | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 眨眼眼睛                                                    |
| **困惑**              | 是，使用結束分支 | Yes               | **否**        | 無                                         | 劃痕標頭                                                 |
| **祝賀**          | 是，使用結束分支 | 是               | **是**       | 無                                         | 讚揚                                                       |
| **恭喜 \_ 2**       | 是，使用結束分支 | Yes               | **否**        | 無                                         | 提供拇指手勢手勢                                        |
| **拒絕**               | 是，使用結束分支 | Yes               | **否**        | 無                                         | 引發實習和訪談標頭                                   |
| **DoMagic1**              | 無                     | Yes               | **否**        | 無                                         | 轉向側邊並引發手                                 |
| **DoMagic2**              | 是，使用結束分支 | 否                | **是**       | 無                                         | 減少手中，雲端顯示                                    |
| **DontRecognize**         | 是，使用結束分支 | Yes               | **否**        | 無                                         | 將手交給 ear                                              |
| **說明**               | 是，使用結束分支 | Yes               | **否**        | 無                                         | 將 arm 延伸至側面                                           |
| **GestureDown**           | 是，使用結束分支 | Yes               | **否**        | **GesturingDown**                            | 手勢向下                                                  |
| **GestureLeft**           | 是，使用結束分支 | Yes               | **否**        | **GesturingLeft**                            | 左邊的手勢                                                  |
| **GestureRight**          | 是，使用結束分支 | Yes               | **否**        | **GesturingRight**                           | 手勢右邊                                                 |
| **GestureUp**             | 是，使用結束分支 | Yes               | **否**        | **GesturingUp**                              | 手勢                                                    |
| **GetAttention**          | **GetAttentionReturn**   | Yes               | **否**        | 無                                         | 波浪臂                                                     |
| **GetAttentionContinued** | **GetAttentionReturn**   | Yes               | **否**        | 無                                         | 再次波浪手臂                                               |
| **GetAttentionReturn**    | 無                     | No                | **否**        | 無                                         | 返回中性位置                                    |
| **問候**                 | 是，使用結束分支 | Yes               | **否**        | 無                                         | 弓                                                           |
| **聽力 \_ 1**            | 無                     | No                | **否**        | **聽覺**                                  | 耳延伸 (\* 迴圈動畫)                               |
| **聽力 \_ 2**            | 無                     | No                | **否**        | **聽覺**                                  | 將標頭左方 (\* 迴圈動畫)                           |
| **聽力 \_ 3**            | 無                     | No                | **否**        | **聽覺**                                  | 開啟 (\* 迴圈動畫) 的標頭                          |
| **聽力 \_ 4**            | 無                     | No                | **否**        | **聽覺**                                  | 將標頭 (\* 迴圈動畫)                          |
| [隱藏]                   | 無                     | 否                | **是**       | **隱藏**                                   | 消失于冒煙                                          |
| **Idle1 \_ 1**              | 無                     | No                | **否**        | **IdlingLevel1** IdlingLevel2                | 採用吸一口氣                                                   |
| **Idle1 \_ 2**              | 無                     | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 向右和閃爍                                       |
| **Idle1 \_ 3**              | 是，使用結束分支 | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 向左和眨眼的概覽                                        |
| **Idle1 \_ 4**              | 無                     | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 向右和閃爍                             |
| **Idle1 \_ 5**              | 是，使用結束分支 | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 概覽並閃爍                                        |
| **Idle1 \_ 6**              | 無                     | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 概覽並閃爍                                          |
| **Idle2 \_ 1**              | 無                     | No                | **否**        | **IdlingLevel2**                             | Wisp snakes                                                    |
| **Idle2 \_ 2**              | 是，使用結束分支 | No                | **否**        | **IdlingLevel2**                             | 顯示捲軸和讀取                                       |
| **Idle2 \_ 3**              | 是，使用結束分支 | No                | **否**        | **IdlingLevel2**                             | 顯示捲軸和寫入                                      |
| **Idle3 \_ 1**              | 無                     | 否                | **是**       | **IdlingLevel3**                             | 打哈欠                                                          |
| **Idle3 \_ 2**              | 是，使用結束分支 | 否                | **是**       | **IdlingLevel3**                             | 落在睡眠 (\* 迴圈動畫)                              |
| **LookDown**              | **LookDownReturn**       | No                | **否**        | 無                                         | 向下查看                                                     |
| **LookDownBlink**         | **LookDownReturn**       | No                | **否**        | 無                                         | 閃爍查看                                            |
| **LookDownReturn**        | 無                     | No                | **否**        | 無                                         | 返回中性位置                                    |
| **LookLeft**              | **LookLeftReturn**       | No                | **否**        | 無                                         | 向左查看                                                     |
| **LookLeftBlink**         | **LookLeftReturn**       | No                | **否**        | 無                                         | 靠左閃爍                                            |
| **LookLeftReturn**        | 無                     | No                | **否**        | 無                                         | 返回中性位置                                    |
| **LookRight**             | **LookRightReturn**      | No                | **否**        | 無                                         | 看起來正確                                                    |
| **LookRightBlink**        | **LookRightReturn**      | No                | **否**        | 無                                         | 靠右閃爍                                           |
| **LookRightReturn**       | 無                     | No                | **否**        | 無                                         | 返回中性位置                                    |
| **查找**                | **LookUpReturn**         | No                | **否**        | 無                                         | 查閱                                                       |
| **LookUpBlink**           | **LookUpReturn**         | No                | **否**        | 無                                         | 眨眼查閱                                              |
| **LookUpReturn**          | 無                     | No                | **否**        | 無                                         | 返回中性位置                                    |
| **MoveDown**              | 是，使用結束分支 | 否                | **是**       | **MovingDown**                               | 飛下                                                     |
| **MoveLeft**              | 是，使用結束分支 | 否                | **是**       | **MovingLeft**                               | 向左飛出                                                     |
| **MoveRight**             | 是，使用結束分支 | 否                | **是**       | **MovingRight**                              | 向右飛出                                                    |
| **上移**                | 是，使用結束分支 | 否                | **是**       | **MovingUp**                                 | 飛出                                                       |
| **高興**               | 是，使用結束分支 | Yes               | **否**        | 無                                         | 肯定和保存手合                                |
| **處理**               | 否                       | 否                | **否**        | 無                                         | 在雲端中旋轉                                             |
| **Processing**            | 是，使用結束分支 | No                | **否**        | 無                                         | 旋轉到雲端 (\* 迴圈動畫)                        |
| **讀取**                  | **ReadReturn**           | 是               | **是**       | 無                                         | 顯示捲軸、讀取和查閱                             |
| **ReadContinued**         | **ReadReturn**           | Yes               | **否**        | 無                                         | 讀取和查閱                                             |
| **ReadReturn**            | 無                     | No                | **否**        | 無                                         | 返回中性位置                                    |
| **讀取**               | 是，使用結束分支 | 否                | **是**       | 無                                         |  (迴圈動畫顯示捲軸和讀取 \*)                   |
| **RestPose**              | 無                     | Yes               | **否**        | **說**                                 | 中性位置                                               |
| **傷心**                   | 是，使用結束分支 | Yes               | **否**        | 無                                         | 悲傷運算式                                                 |
| **搜尋**                | 否                       | 否                | **否**        | 無                                         | 顯示雙筒和回合                                   |
| **搜索**             | 是，使用結束分支 | No                | **否**        | 無                                         | 顯示雙筒線，並開啟 (\* 迴圈動畫)              |
| **顯示**                  | 無                     | 否                | **是**       | **正在顯示**                                  | 出現在冒煙之外                                           |
| **StartListening**        | 是，使用結束分支 | Yes               | **否**        | 無                                         | 把手交給 ear                                               |
| **StopListening**         | 是，使用結束分支 | Yes               | **否**        | 無                                         | 將手放在整個耳                                           |
| **建議**               | 是，使用結束分支 | Yes               | **否**        | 無                                         | 顯示燈泡                                             |
| **驚訝**             | 是，使用結束分支 | Yes               | **否**        | 無                                         | 看起來很驚訝                                                |
| **認為**                 | 是，使用結束分支 | Yes               | **否**        | 無                                         | 在下巴上尋找手                                     |
| **思維**              | 否                       | 否                | **否**        | 無                                         | 以手下巴 (\* 迴圈動畫)                |
| **不確定性**             | 是，使用結束分支 | Yes               | **否**        | 無                                         | 將一方面移至下巴，並將其移至 hip，並引發 right 置頂路徑連結 |
| **波**                  | 是，使用結束分支 | Yes               | **否**        | 無                                         | 波                                                          |
| **寫入**                 | **WriteReturn**          | 是               | **是**       | 無                                         | 顯示捲軸、寫入和查閱                            |
| **WriteContinued**        | **WriteReturn**          | 是               | **是**       | 無                                         | 寫入和查閱                                            |
| **WriteReturn**           | 無                     | No                | **否**        | 無                                         | 返回中性位置                                    |
| **寫入**               | 是，使用結束分支 | 否                | **是**       | 無                                         | 顯示捲軸、寫入 (\* 迴圈動畫)                    |



 

\* 如果您播放迴圈動畫，則必須先使用 [ [**停止**](stop-method.md) ] 來清除它，然後才會播放字元佇列中的其他動畫。

 


---
title: 適用于 Peedy 字元的 Microsoft Agent 動畫
description: 適用于 Peedy 字元的 Microsoft Agent 動畫
ms.assetid: 335d915c-9cae-4850-a6bf-66ad78d533ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46682d8836fc02a8d19d5b40e8fddef4068a1d14190c2919042ff1087a745acb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888108"
---
# <a name="microsoft-agent-animations-for-peedy-character"></a>適用于 Peedy 字元的 Microsoft Agent 動畫

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

[Microsoft Agent Peedy 字元](https://www.microsoft.com/downloads/details.aspx?FamilyID=bd3c4655-79e4-4791-ab9d-abc7bbd133ef)是 Microsoft Corporation 的受版權保護工作。

Peedy 支援下表所列的動畫。 如需如何呼叫字元動畫的詳細資訊，請參閱 [Microsoft 代理程式伺服器介面程式設計](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) 和 [Microsoft Agent 控制項程式設計](programming-the-microsoft-agent-control.md) 。

如果使用 HTTP 通訊協定和控制項的 [**Get**](get-method.md) 或 Server 的 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法來存取這些字元動畫，請考慮您將如何下載這些字元動畫。 您可能會想要先取出 **顯示** 和 **說話** 狀態動畫，而不是一次下載所有動畫。 這可讓您快速顯示字元，並讓它說話，並以非同步方式關閉其他動畫。 此外，若要確保字元和動畫資料載入成功，請使用 [**RequestComplete**](requestcomplete-event.md) 事件。 如果載入要求失敗，您可以重試載入資料或顯示適當的訊息。

如果動畫的傳回動畫是使用「結束分支」**定義的，** 您就不需要明確地呼叫它。代理程式會在下一個動畫之前自動播放 **傳回動畫。** 但是，如果有列出傳回的動畫，您必須在另一個動畫之前使用 [**Play**](play-method.md)方法來 **呼叫動畫，** 以提供順暢的轉換。 如果未 **列出任何傳回** 動畫，則動畫通常會結束，而不需要過渡動畫。

如果使用 HTTP 通訊協定和控制項的 [**Get**](get-method.md) 或 Server 的 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法來存取這些字元動畫，請考慮您將如何下載這些字元動畫。 您可能會想要先取出 **顯示** 和 **說話** 狀態動畫，而不是一次下載所有動畫。 這可讓您快速顯示字元，並讓它說話，並以非同步方式關閉其他動畫。 此外，若要確保字元和動畫資料載入成功，請使用 [**RequestComplete**](requestcomplete-event.md) 事件。 如果載入要求失敗，您可以重試載入資料或顯示適當的訊息。

字元檔包含某些動畫的音效效果，如下表所述。 只有在 Microsoft Agent 屬性工作表中啟用這個選項時，才會播放音效效果。 您也可以在應用程式中停用音效效果。



| 動畫                  | 返回動畫         | 支援說話 | 音效 | 指派至狀態                            | 描述                                            |
|----------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------------|
| **承認**            | 無                     | No                | **否**        | 無                                         | 節點 head                                              |
| **警示**                  | 是，使用結束分支 | Yes               | **否**        | **聽**                                | Straightens 並引發眉毛                        |
| **宣佈**               | 是，使用結束分支 | 是               | **是**       | 無                                         | 紙飛機飛入和將                    |
| **Blink**                  | 無                     | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 眨眼眼睛                                            |
| **困惑**               | 是，使用結束分支 | 是               | **是**       | 無                                         | 眼睛旋轉                                       |
| **祝賀**           | 是，使用結束分支 | 是               | **是**       | 無                                         | 顯示藍色功能區                                   |
| **拒絕**                | 是，使用結束分支 | Yes               | **否**        | 無                                         | 訪談 head                                            |
| **DoMagic1**               | 無                     | 是               | **是**       | 無                                         | 引發魔術棒                                      |
| **DoMagic2**               | 是，使用結束分支 | 否                | **是**       | 無                                         | 降低棒，雲端顯示                             |
| **DontRecognize**          | 是，使用結束分支 | Yes               | **否**        | 無                                         | 訪談標頭，並將翼帶到 ear                      |
| **說明**                | 是，使用結束分支 | Yes               | **否**        | 無                                         | 將 arm 延伸至側面                                   |
| **GestureDown**            | 是，使用結束分支 | Yes               | **否**        | **GesturingDown**                            | 手勢向下                                          |
| **GestureLeft**            | 是，使用結束分支 | Yes               | **否**        | **GesturingLeft**                            | 左邊的手勢                                          |
| **GestureRight**           | 是，使用結束分支 | Yes               | **否**        | **GesturingRight**                           | 手勢右邊                                         |
| **GestureUp**              | 是，使用結束分支 | Yes               | **否**        | **GesturingUp**                              | 手勢                                            |
| **GetAttention**           | **GetAttentionReturn**   | 是               | **是**       | 無                                         | 利用翅膀 outstretched                       |
| **GetAttentionContinued**  | **GetAttentionReturn**   | 是               | **是**       | 無                                         | 再次跳到翅膀 outstretched                 |
| **GetAttentionReturn**     | 無                     | No                | **否**        | 無                                         | 返回中性位置                            |
| **問候**                  | 是，使用結束分支 | 是               | **是**       | 無                                         | 弓                                                   |
| **聽力 \_ 1**             | 無                     | No                | **否**        | **聽覺**                                  | 傾斜 (\* 迴圈動畫)                  |
| **聽力 \_ 2**             | 無                     | No                | **否**        | **聽覺**                                  | 將標頭左方 (\* 迴圈動畫)                   |
| **聽力 \_ 3**             | 無                     | No                | **否**        | **聽覺**                                  | 將 (迴圈動畫的標頭靠左 \*)        |
| [隱藏]                    | 無                     | 否                | **是**       | **隱藏**                                   | 飛走                                             |
| **Idle1 \_ 1**               | 無                     | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 採用吸一口氣                                           |
| **Idle1 \_ 2**               | 無                     | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 向右和閃爍                               |
| **Idle1 \_ 3**               | 無                     | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 向左和眨眼的概覽                                |
| **Idle1 \_ 4**               | 無                     | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 概覽並閃爍                                  |
| **Idle1 \_ 5**               | 無                     | No                | **否**        | **IdlingLevel1** **IdlingLevel2**<br/> | 概覽並閃爍                                |
| **Idle2 \_ 1**               | 是，使用結束分支 | No                | **否**        | **IdlingLevel2**                             | 放在太陽眼鏡上                                     |
| **Idle2 \_ 2**               | 無                     | 否                | **是**       | **IdlingLevel2**                             | 耗盡破解者                                         |
| **Idle3 \_ 1**               | 無                     | 否                | **是**       | **IdlingLevel3**                             | 打哈欠                                                  |
| **Idle3 \_ 2**               | 是，使用結束分支 | 否                | **是**       | **IdlingLevel3**                             | 落在睡眠 (\* 迴圈動畫)                      |
| **Idle3 \_ 3**               | 是，使用結束分支 | No                | **否**        | **IdlingLevel3**                             | 接聽音樂 (\* 迴圈動畫)                  |
| **LookDownLookDownReturn** |                          | No                | **否**        | 無                                         | 向下查看                                             |
| **LookDownBlink**          | **LookDownReturn**       | 否                | **是**       | 無                                         | 閃爍查看                                    |
| **LookDownReturn**         | 無                     | No                | **否**        | 無                                         | 返回中性位置                            |
| **LookDownLeft**           | **LookDownLeftReturn**   | No                | **否**        | 無                                         | 向下查閱                                        |
| **LookDownLeftBlink**      | **LookDownLeftReturn**   | 否                | **是**       | 無                                         | 靠左閃爍                               |
| **LookDownLeftReturn**     | 無                     | No                | **否**        | 無                                         | 返回中性位置                            |
| **LookDownRight**          | **LookDownRightReturn**  | No                | **否**        | 無                                         | 向下查閱                                       |
| **LookDownRightBlink**     | **LookDownRightReturn**  | 否                | **是**       | 無                                         | 靠右閃爍                              |
| **LookDownRightReturn**    | 無                     | No                | **否**        | 無                                         | 返回中性位置                            |
| **LookLeft**               | **LookLeftReturn**       | Yes               | **否**        | 無                                         | 向左查看                                             |
| **LookLeftBlink**          | **LookLeftReturn**       | 是               | **是**       | 無                                         | 靠左閃爍                                    |
| **LookLeftReturn**         | 無                     | No                | **否**        | 無                                         | 返回中性位置                            |
| **LookRight**              | **LookRightReturn**      | Yes               | **否**        | 無                                         | 看起來正確                                            |
| **LookRightBlink**         | **LookRightReturn**      | 是               | **是**       | 無                                         | 靠右閃爍                                   |
| **LookRightReturn**        | 無                     | No                | **否**        | 無                                         | 返回中性位置                            |
| **查找**                 | **LookUpReturn**         | No                | **否**        | 無                                         | 查閱                                               |
| **LookUpBlink**            | **LookUpReturn**         | 否                | **是**       | 無                                         | 眨眼查閱                                      |
| **LookUpReturn**           | 無                     | No                | **否**        | 無                                         | 返回中性位置                            |
| **LookUpLeft**             | **LookUpLeftReturn**     | No                | **否**        | 無                                         | 向左查閱                                          |
| **LookUpLeftBlink**        | **LookUpLeftReturn**     | 否                | **是**       | 無                                         | 靠左閃爍                                 |
| **LookUpLeftReturn**       | 無                     | No                | **否**        | 無                                         | 返回中性位置                            |
| **LookUpRight**            | **LookUpRightReturn**    | No                | **否**        | 無                                         | 向右查閱                                         |
| **LookUpRightBlink**       | **LookUpRightReturn**    | 否                | **是**       | 無                                         | 靠右閃爍                                |
| **LookUpRightReturn**      | 無                     | No                | **否**        | 無                                         | 返回中性位置                            |
| **MoveDown**               | 是，使用結束分支 | 否                | **是**       | **MovingDown**                               | 飛下                                             |
| **MoveLeft**               | 是，使用結束分支 | 否                | **是**       | **MovingLeft**                               | 向左飛出                                             |
| **MoveRight**              | 是，使用結束分支 | 否                | **是**       | **MovingRight**                              | 向右飛出                                            |
| **上移**                 | 是，使用結束分支 | 否                | **是**       | **MovingUp**                                 | 飛出                                               |
| **高興**                | 是，使用結束分支 | Yes               | **否**        | 無                                         | 微笑                                                 |
| **處理**                | 無                     | 否                | **是**       | 無                                         | 使用計算機                                        |
| **Processing**             | 是，使用結束分支 | 否                | **是**       | 無                                         | 使用計算機 (\* 迴圈動畫)                   |
| **讀取**                   | **ReadReturn**           | 是               | **是**       | 無                                         | 開啟雜誌、讀取和查閱                     |
| **ReadContinued**          | **ReadReturn**           | 是               | **是**       | 無                                         | 讀取和查閱                                     |
| **ReadReturn**             | 無                     | 否                | **是**       | 無                                         | 返回中性位置                            |
| **讀取**                | 是，使用結束分支 | 否                | **是**       | 無                                         | 讀取 (\* 迴圈動畫)                             |
| **RestPose**               | 無                     | Yes               | **否**        | **說**                                 | 中性位置                                       |
| **傷心**                    | 是，使用結束分支 | Yes               | **否**        | 無                                         | 悲傷運算式                                         |
| **搜尋**                 | 無                     | 否                | **是**       | 無                                         | 顯示望遠鏡並旋轉                          |
| **搜索**              | 是，使用結束分支 | 否                | **是**       | 無                                         | 顯示望遠鏡並旋轉 (\* 迴圈動畫)     |
| **顯示**                   | 無                     | 否                | **是**       | **正在顯示**                                  | 飛入                                               |
| **StartListening**         | 是，使用結束分支 | Yes               | **否**        | 無                                         | 把手交給 ear                                       |
| **StopListening**          | 是，使用結束分支 | Yes               | **否**        | 無                                         | 將手放入耳                                     |
| **建議**                | 是，使用結束分支 | 是               | **是**       | 無                                         | 顯示燈泡                                    |
| **驚訝**              | 是，使用結束分支 | 是               | **是**       | 無                                         | 看起來很驚訝                                        |
| **認為**                  | 是，使用結束分支 | Yes               | **否**        | 無                                         | 查看臉部上的翼形                             |
| **思維**               | 無                     | No                | **否**        | 無                                         | 查看臉部 (\* 迴圈動畫)        |
| **不確定性**              | 是，使用結束分支 | Yes               | **否**        | 無                                         | 仰賴至右方和 shrugs                              |
| **波**                   | 是，使用結束分支 | Yes               | **否**        | 無                                         | 波                                                  |
| **寫入**                  | **WriteReturn**          | 是               | **是**       | 無                                         | 取出鉛筆和 pad、書寫和查閱          |
| **WriteContinued**         | **WriteReturn**          | 是               | **是**       | 無                                         | 寫入和查閱                                    |
| **WriteReturn**            | 無                     | No                | **否**        | 無                                         | 返回中性位置                            |
| **寫入**                | 是，使用結束分支 | 否                | **是**       | 無                                         | 取出鉛筆和 pad、書寫 (\* 迴圈動畫)  |



 

\* 如果您播放迴圈動畫，則必須先使用 [ [**停止**](stop-method.md) ] 來清除它，然後才會播放字元佇列中的其他動畫。

 


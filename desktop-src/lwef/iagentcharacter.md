---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: 77d0ffc2-76a2-4a21-88e1-1ca85b8c5d2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d7144c6d3379a2237d3f14c955d8052ff4d20d1ff98d9c2f2637796f8b931b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962088"
---
# <a name="iagentcharacter"></a>IAgentCharacter

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

**IAgentCharacter** 定義了一個介面，可讓應用程式查詢字元屬性並播放動畫。 這些函數也可從 [**IAgentCharacterEx**](iagentcharacterex.md)取得。 您可以使用某些方法傳回要求識別碼，在字元的佇列中追蹤其狀態，並將您的程式碼與該字元的目前動畫狀態進行同步處理。

**依照 Vtable 順序的方法**



| IAgentCharacter 方法                                           | 描述                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**GetVisible**](iagentcharacter--getvisible.md)                 | 傳回 (框架) 的字元是否目前為可見。                       |
| [**SetPosition**](iagentcharacter--setposition.md)               | 設定字元框架的位置。                                         |
| [**GetPosition**](iagentcharacter--getposition.md)               | 傳回字元框架的位置。                                      |
| [**SetSize**](iagentcharacter--setsize.md)                       | 設定字元框架的大小。                                             |
| [**GetSize**](iagentcharacter--getsize.md)                       | 傳回字元框架的大小。                                          |
| [**GetName**](iagentcharacter--getname.md)                       | 傳回字元的名稱。                                                |
| [**GetDescription**](iagentcharacter--getdescription.md)         | 傳回字元的描述。                                        |
| [**GetTTSSpeed**](iagentcharacter--getttsspeed.md)               | 傳回字元目前的 TTS 輸出速度設定。                   |
| [**GetTTSPitch**](iagentcharacter--getttspitch.md)               | 傳回字元目前的 TTS 音調設定。                          |
| [**啟用**](iagentcharacter--activate.md)                     | 設定用戶端是否為使用中或字元是否最上層。                        |
| [**SetIdleOn**](iagentcharacter--setidleon.md)                   | 設定伺服器的閒置處理。                                                |
| [**GetIdleOn**](iagentcharacter--getidleon.md)                   | 傳回伺服器閒置處理的設定。                              |
| [**準備**](iagentcharacter--prepare.md)                       | 抓取字元的動畫資料。                                       |
| [**播放**](iagentcharacter--play.md)                             | 播放指定的動畫。                                                      |
| [**停止**](iagentcharacter--stop.md)                             | 停止字元的動畫。                                               |
| [**StopAll**](iagentcharacter--stopall.md)                       | 停止字元的所有動畫。                                             |
| [**等候**](iagentcharacter--wait.md)                             | 保存字元的動畫佇列。                                            |
| [**中斷**](iagentcharacter--interrupt.md)                   | 中斷字元的動畫。                                               |
| [**顯示**](iagentcharacter--show.md)                             | 顯示字元並播放 **顯示** 狀態動畫的字元。     |
| [**隱藏**](iagentcharacter--hide.md)                             | 播放字元 **隱藏** 狀態的動畫，並隱藏字元的框架。 |
| [**Speak**](iagentcharacter--speak.md)                           | 播放字元的語音輸出。                                            |
| [**MoveTo**](iagentcharacter--moveto.md)                         | 將字元框架移至指定的位置。                              |
| [**GestureAt**](iagentcharacter--gestureat.md)                   | 根據指定的位置播放 gesturing 動畫。                      |
| [**GetMoveCause**](iagentcharacter--getmovecause.md)             | 抓取字元上一次移動的原因。                                 |
| [**GetVisibilityCause**](iagentcharacter--getvisibilitycause.md) | 抓取上次變更字元可見度狀態的原因。       |
| [**HasOtherClients**](iagentcharacter--hasotherclients.md)       | 抓取字元是否有其他目前的用戶端。                        |
| [**SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md)   | 決定是否播放字元動畫的音效效果。                    |
| [**GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md)   | 抓取是否啟用字元的音效效果設定。                 |
| [**SetName**](iagentcharacter--setname.md)                       | 設定字元的名稱。                                                        |
| [**SetDescription**](iagentcharacter--setdescription.md)         | 設定字元的描述。                                                 |
| [**GetExtraData**](iagentcharacter--getextradata.md)             | 抓取字元所儲存的其他資料。                              |



 

 

 





---
title: IAgentCharacterEx
description: IAgentCharacterEx
ms.assetid: 8defc836-cc54-40c7-8afc-ec90f941861b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92a9f9c39804d6b5d3ac777457fff5b7f03823c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840360"
---
# <a name="iagentcharacterex"></a>IAgentCharacterEx

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

**IAgentCharacterEx** 衍生自 [**IAgentCharacter**](iagentcharacter.md) 介面。 它包含所有的 **IAgentCharacter** 方法，以及提供其他函式的存取權。

**依照 Vtable 順序的方法**



| IAgentCharacterEx 方法                                         | Description                                                                    |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)         | 顯示字元的快顯功能表。                                    |
| [**SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)   | 設定伺服器是否自動顯示字元的快顯功能表。    |
| [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md)   | 傳回伺服器是否自動顯示字元的快顯功能表。 |
| [**GetHelpFileName**](iagentcharacterex--gethelpfilename.md)     | 傳回字元的說明文件名。                                   |
| [**SetHelpFileName**](iagentcharacterex--sethelpfilename.md)     | 設定字元的說明文件名。                                      |
| [**SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)         | 將說明模式設定為開啟。                                                             |
| [**GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md)         | 傳回說明模式是否為開啟。                                               |
| [**SetHelpCoNtextID**](iagentcharacterex--sethelpcontextid.md)   | 設定字元的提供。                                      |
| [**GetHelpCoNtextID**](iagentcharacterex--gethelpcontextid.md)   | 傳回字元的提供。                                   |
| [**GetActive**](iagentcharacterex--getactive.md)                 | 傳回字元的現用狀態。                                    |
| [**接聽**](iagentcharacterex--listen.md)                       | 設定字元的接聽狀態。                                    |
| [**SetLanguageID**](iagentcharacterex--setlanguageid.md)         | 設定字元的語言識別項。                                        |
| [**getLanguageID**](iagentcharacterex--getlanguageid.md)         | 傳回字元的語言識別項。                                     |
| [**getTTSModeID**](iagentcharacterex--getttsmodeid.md)           | 傳回為字元設定的 TTS 模式識別碼。                                 |
| [**SetTTSModeID**](iagentcharacterex--setttsmodeid.md)           | 設定字元的 TTS 模式識別碼。                                        |
| [**getSRModeID**](iagentcharacterex--getsrmodeid.md)             | 傳回目前的語音辨識引擎的模式識別碼。                       |
| [**setSRModeID**](iagentcharacterex--setsrmodeid.md)             | 設定語音辨識引擎。                                            |
| [**GetGUID**](iagentcharacterex--getguid.md)                     | 傳回字元的識別碼。                                            |
| [**GetOriginalSize**](iagentcharacterex--getoriginalsize.md)     | 傳回字元框架的原始大小。                              |
| [**認為**](iagentcharacterex--think.md)                         | 在字元的「想法」氣球中顯示指定的文字。              |
| [**GetVersion**](iagentcharacterex--getversion.md)               | 傳回字元的版本。                                          |
| [**GetAnimationNames**](iagentcharacterex--getanimationnames.md) | 傳回字元的動畫名稱。                         |
| [**getSRStatus**](iagentcharacterex--getsrstatus.md)             | 傳回支援語音輸入所需的條件。                      |



 

 

 





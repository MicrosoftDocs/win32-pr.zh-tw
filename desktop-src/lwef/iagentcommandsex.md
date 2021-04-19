---
title: IAgentCommandsEx
description: IAgentCommandsEx
ms.assetid: 6c354677-4cdb-4a74-9c41-2d0bf6f8dd55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16616ccb86bf109dad85a8ee2ac5d2bd009827
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106980274"
---
# <a name="iagentcommandsex"></a>IAgentCommandsEx

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

[**IAgentCommandsEx**](iagentcommandex.md) 會定義擴充 [**IAgentCommands**](iagentcommands.md) 介面的介面。

**依照 Vtable 順序的方法**



| IAgentCommandsEx 方法                                                             | Description                                                                                                   |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SetDefaultID](iagentcommandsex--setdefaultid.md)                                   | 設定字元快顯功能表的預設命令。                                                     |
| [GetDefaultID](iagentcommandsex--getdefaultid.md)                                   | 傳回字元快顯功能表的預設命令。                                                  |
| [**SetHelpCoNtextID**](iagentcommandex--sethelpcontextid.md)                        | 設定 [**命令**](/windows/desktop/lwef/the-command-object) 物件的上下文相關說明主題識別碼。                     |
| [**GetHelpCoNtextID**](iagentcommandex--gethelpcontextid.md)                        | 傳回 [**命令**](/windows/desktop/lwef/the-command-object) 物件的上下文相關說明主題識別碼。                  |
| [SetFontName](iagentcommandsex--setfontname.md)                                     | 設定要在字元的快顯功能表中使用的字型。                                                          |
| [GetFontName](iagentcommandsex--getfontname.md)                                     | 傳回字元快顯功能表中所使用的字型。                                                         |
| [SetFontSize](iagentcommandsex--setfontsize.md)                                     | 設定要在字元的快顯功能表中使用的字型大小。                                                     |
| [GetFontSize](iagentcommandsex--getfontsize.md)                                     | 傳回字元快顯功能表中所使用的字型大小。                                                    |
| [**SetVoiceCaption**](iagentcommandex--setvoicecaption.md)                          | 設定字元 [**命令**](/windows/desktop/lwef/the-command-object) 物件的語音標題。                         |
| [**GetVoiceCaption**](iagentcommandex--getvoicecaption.md)                          | 傳回字元 [**命令**](/windows/desktop/lwef/the-command-object) 物件的聲音標題。                      |
| [AddEx](iagentcommandsex--addex.md)                                                 | 將 [**命令**](/windows/desktop/lwef/the-command-object) 物件加入至 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合。    |
| [InsertEx](iagentcommandsex--insertex.md)                                           | 在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中插入 [**Command**](/windows/desktop/lwef/the-command-object)物件。 |
| [SetGlobalVoiceCommandsEnabled](iagentcommandsex--setglobalvoicecommandsenabled.md) | 啟用代理程式全域命令的語音文法。                                                        |
| [GetGlobalVoiceCommandsEnabled](iagentcommandsex--getglobalvoicecommandsenabled.md) | 傳回是否啟用代理程式全域命令的語音文法。                                     |



 

 

 
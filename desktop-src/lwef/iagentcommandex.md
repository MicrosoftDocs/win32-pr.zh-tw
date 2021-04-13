---
title: IAgentCommandEx
description: IAgentCommandEx
ms.assetid: 7849ddbe-e81f-4088-ba66-67676279789b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d54218d28372e9d22bebedbb0b07d8cbacfc03
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375125"
---
# <a name="iagentcommandex"></a>IAgentCommandEx

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

**IAgentCommandEx** 衍生自 [**IAgentCommand**](iagentcommand.md) 介面。 它包含所有的 **IAgentCommand** 方法，並提供其他函式的存取權。

**依照 Vtable 順序的方法**



| IAgentCommandEx 方法                                       | Description                                                                                  |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**SetHelpCoNtextID**](iagentcommandex--sethelpcontextid.md) | 設定 [**命令**](/windows/desktop/lwef/the-command-object) 物件的上下文相關說明主題識別碼。    |
| [**GetHelpCoNtextID**](iagentcommandex--gethelpcontextid.md) | 傳回 [**命令**](/windows/desktop/lwef/the-command-object) 物件的上下文相關說明主題識別碼。 |
| [**SetVoiceCaption**](iagentcommandex--setvoicecaption.md)   | 設定 [**命令**](/windows/desktop/lwef/the-command-object) 物件的語音標題。                      |
| [**GetVoiceCaption**](iagentcommandex--getvoicecaption.md)   | 傳回 [**命令**](/windows/desktop/lwef/the-command-object) 物件的聲音標題。                   |



 

 

 
---
title: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092692"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a>IAgentCommandsEx::SetGlobalVoiceCommandsEnabled

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

為 Microsoft 代理程式的全域命令的語音文法設定 [**Enabled**](enabled-property.md) 屬性。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*
</dt> <dd>

布林值，設定是否啟用代理程式全域命令的語音文法。 **True** 可啟用語音文法; **False** 會停用它。

</dd> </dl>

Microsoft 代理程式會自動新增語音參數 (文法) 來開啟和關閉 [語音命令] 視窗，以及顯示和隱藏字元。 當設定為 **False** 時，Agent 會停用這些命令的任何語音參數，以及其他用戶端 [**命令**](/windows/desktop/lwef/the-command-object)物件之 [**標題**](caption-property.md)的語音參數。 這可讓您從用戶端目前的活動文法中排除這些。 不過，因為這可能會封鎖其他用戶端的語音存取，所以在處理使用者的語音輸入之後，請將此屬性重設為 **True** 。

停用此屬性並不會影響該字元的快顯功能表。 伺服器所加入的全域命令仍會出現。 您無法從快顯功能表中移除它們。

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 
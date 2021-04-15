---
title: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375157"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a>IAgentCommandsEx::GetGlobalVoiceCommandsEnabled

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

抓取是否已啟用代理程式全域命令的語音文法。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

如果已啟用代理程式 global 命令的語音文法，則為收到 **True** 的位址，如果停用，則為 **False** 。

</dd> </dl>

Microsoft 代理程式會自動新增語音參數 (文法) 來開啟和關閉 [語音命令] 視窗，以及顯示和隱藏字元。 當此方法傳回 **False** 時，文法中不會包含這些命令的任何語音參數，以及其他用戶端 [**命令**](/windows/desktop/lwef/the-command-object)物件之 [**標題**](caption-property.md)的語音參數。 這可讓您從用戶端目前的活動文法中排除這些。 不過，此設定不會反映在字元的快顯功能表中包含這些命令。

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 
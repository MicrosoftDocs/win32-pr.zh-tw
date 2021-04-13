---
title: IAgentCommands 插入
description: IAgentCommands 插入
ms.assetid: f450aae4-db6f-4326-ae14-ddb68ab0953a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f15df0c24e16a7554881cf3d0e6c41c4ee42b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375121"
---
# <a name="iagentcommandsinsert"></a>IAgentCommands：： Insert

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT Insert(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long dwRefID,     // reference Command for insertion
   long dBefore,     // insertion position flag
   long * pdwID      // address for variable for Command ID
);
```

在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中插入 [**Command**](/windows/desktop/lwef/the-command-object)物件。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

指定針對 [**命令**](/windows/desktop/lwef/the-command-object)顯示之 [**標題**](caption-property.md)文字值的 BSTR。

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**語音**](voice-property.md)文字設定值的 BSTR。

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

指定 [**命令**](/windows/desktop/lwef/the-command-object)[**已啟用**](enabled-property.md)設定的布林運算式。 如果參數為 **True**，則會啟用並選取 **命令** ;如果 **為 False**，則表示 **命令** 已停用。

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**可見**](visible-property.md)設定的布林運算式。 如果參數為 **True**，則在字元的快顯功能表中會顯示 **命令** (如果 [**Caption**](caption-property.md) 屬性也設定為) 。

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*
</dt> <dd>

用來作為新 **命令** 之相對插入參考的 [**命令**](/windows/desktop/lwef/the-command-object)識別碼。

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*
</dt> <dd>

指定要放置 [**命令**](/windows/desktop/lwef/the-command-object)之位置的布林運算式。 如果此參數為 **True**，則會在參考的 **命令** 之前插入新的 **命令**;如果 **為 False**，則新的 **命令** 會放在參考的 **命令** 之後。

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

接收所插入 [**命令**](/windows/desktop/lwef/the-command-object)之識別碼的變數位址。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Remove**](iagentcommands--remove.md)、 [**IAgentCommands：： RemoveAll**](iagentcommands--removeall.md)


 

 
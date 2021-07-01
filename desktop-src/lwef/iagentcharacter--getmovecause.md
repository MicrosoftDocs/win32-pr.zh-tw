---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119681"
---
# <a name="iagentcharactergetmovecause"></a>IAgentCharacter::GetMoveCause

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

抓取字元上一次移動的原因。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

接收字元最後一個移動原因的變數位址，將會是下列其中一項：



| 值                                                               | 描述                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const 不帶正負號短** **NeverMoved = 0;**<br/>        | 尚未移動字元。                                                        |
| **const 不帶正負號短** **UserMoved = 1;**<br/>         | 使用者拖曳字元。                                                          |
| **const 不帶正負號短** **ProgramMoved = 2;**<br/>      | 您的應用程式移動了該字元。                                                |
| **const 不帶正負號短** **OtherProgramMoved = 3;**<br/> | 另一個應用程式移動字元。                                             |
| **const 不帶正負號短** **SystemMoved = 4**<br/>        | 伺服器移動字元，以在螢幕解析度變更之後讓它保持在畫面上。 |



 

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentNotifySink：： Move**](iagentnotifysink--move.md)


 

 






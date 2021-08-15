---
title: IAgentCharacter GetIdleOn
description: IAgentCharacter GetIdleOn
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a5ce64b39b615325a3de55c1643004cffaeecf89e2e0a024d317bb56e32d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478361"
---
# <a name="iagentcharactergetidleon"></a>IAgentCharacter::GetIdleOn

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

指出字元的自動閒置處理狀態。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

如果 Microsoft 代理程式伺服器自動針對字元播放 **閒置** 狀態動畫，則為收到 **True** 之變數的位址，否則為 **False** 。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)


 

 





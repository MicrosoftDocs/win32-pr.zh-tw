---
title: IAgentCharacterEx GetVersion
description: IAgentCharacterEx GetVersion
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864bd0cf53e9dd94a547a459bb17cd477189401d544aebca047ead2f049c1c6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750471"
---
# <a name="iagentcharacterexgetversion"></a>IAgentCharacterEx：： GetVersion

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

抓取字元標準動畫集的版本號碼。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*
</dt> <dd>

接收主要版本之變數的位址。

</dd> <dt>

<span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*
</dt> <dd>

接收次要版本之變數的位址。

</dd> </dl>

當您使用 Microsoft 代理程式字元編輯器來建立時，系統會自動設定標準動畫組版本號碼。

 

 





---
title: IAgentCharacterEx GetVersion
description: IAgentCharacterEx GetVersion
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c72d9304aa689cda83117d57f26c2da776c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021261"
---
# <a name="iagentcharacterexgetversion"></a>IAgentCharacterEx：： GetVersion

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

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

 

 





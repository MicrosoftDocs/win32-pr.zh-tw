---
title: IAgentEx GetVersion
description: IAgentEx GetVersion
ms.assetid: e5d55fcd-c1b4-4c9e-b3c7-4471af2f86af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359abb1d22e2cd34fb6b31d85012ac0110f14037
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301307"
---
# <a name="iagentexgetversion"></a>IAgentEx：： GetVersion

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

抓取 Microsoft 代理程式伺服器的版本號碼。

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

 

 





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
# <a name="iagentcharacterexgetversion"></a><span data-ttu-id="c8745-103">IAgentCharacterEx：： GetVersion</span><span class="sxs-lookup"><span data-stu-id="c8745-103">IAgentCharacterEx::GetVersion</span></span>

<span data-ttu-id="c8745-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c8745-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="c8745-105">抓取字元標準動畫集的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="c8745-105">Retrieves the version number of the character standard animation set.</span></span>

-   <span data-ttu-id="c8745-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="c8745-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c8745-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span><span class="sxs-lookup"><span data-stu-id="c8745-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="c8745-108">接收主要版本之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="c8745-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="c8745-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span><span class="sxs-lookup"><span data-stu-id="c8745-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="c8745-110">接收次要版本之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="c8745-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

<span data-ttu-id="c8745-111">當您使用 Microsoft 代理程式字元編輯器來建立時，系統會自動設定標準動畫組版本號碼。</span><span class="sxs-lookup"><span data-stu-id="c8745-111">The standard animation set version number is automatically set when you build it with the Microsoft Agent Character Editor.</span></span>

 

 





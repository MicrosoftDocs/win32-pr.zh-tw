---
title: IAgentCharacter GetIdleOn
description: IAgentCharacter GetIdleOn
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675928"
---
# <a name="iagentcharactergetidleon"></a><span data-ttu-id="3b720-103">IAgentCharacter::GetIdleOn</span><span class="sxs-lookup"><span data-stu-id="3b720-103">IAgentCharacter::GetIdleOn</span></span>

<span data-ttu-id="3b720-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3b720-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

<span data-ttu-id="3b720-105">指出字元的自動閒置處理狀態。</span><span class="sxs-lookup"><span data-stu-id="3b720-105">Indicates the automatic idle processing state for a character.</span></span>

-   <span data-ttu-id="3b720-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="3b720-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3b720-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span><span class="sxs-lookup"><span data-stu-id="3b720-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="3b720-108">如果 Microsoft 代理程式伺服器自動針對字元播放 **閒置** 狀態動畫，則為收到 **True** 之變數的位址，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="3b720-108">Address of a variable that receives **True** if the Microsoft Agent server automatically plays **Idling** state animations for a character and **False** if not.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="3b720-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b720-109">See Also</span></span>

[<span data-ttu-id="3b720-110">**IAgentCharacter::SetIdleOn**</span><span class="sxs-lookup"><span data-stu-id="3b720-110">**IAgentCharacter::SetIdleOn**</span></span>](iagentcharacter--setidleon.md)


 

 





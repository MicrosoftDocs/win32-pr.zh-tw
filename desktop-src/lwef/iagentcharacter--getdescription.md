---
title: IAgentCharacter GetDescription
description: IAgentCharacter GetDescription
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372695"
---
# <a name="iagentcharactergetdescription"></a><span data-ttu-id="4146b-103">IAgentCharacter：： GetDescription</span><span class="sxs-lookup"><span data-stu-id="4146b-103">IAgentCharacter::GetDescription</span></span>

<span data-ttu-id="4146b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="4146b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

<span data-ttu-id="4146b-105">抓取字元的描述。</span><span class="sxs-lookup"><span data-stu-id="4146b-105">Retrieves the description of the character.</span></span>

-   <span data-ttu-id="4146b-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="4146b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4146b-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span><span class="sxs-lookup"><span data-stu-id="4146b-107"><span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="4146b-108">接收字元的描述值之 BSTR 的位址。</span><span class="sxs-lookup"><span data-stu-id="4146b-108">The address of a BSTR that receives the value of the description for the character.</span></span> <span data-ttu-id="4146b-109">使用 Microsoft 代理程式字元編輯器來編譯時，會定義字元的描述。</span><span class="sxs-lookup"><span data-stu-id="4146b-109">A character's description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4146b-110">描述設定是選擇性的，可能不會提供所有字元。</span><span class="sxs-lookup"><span data-stu-id="4146b-110">The description setting is optional and may not be supplied for all characters.</span></span>

</dd> </dl>

 

 





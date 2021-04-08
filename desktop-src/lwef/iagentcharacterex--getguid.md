---
title: IAgentCharacterEx GetGUID
description: IAgentCharacterEx GetGUID
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932417"
---
# <a name="iagentcharacterexgetguid"></a><span data-ttu-id="a6d42-103">IAgentCharacterEx：： GetGUID</span><span class="sxs-lookup"><span data-stu-id="a6d42-103">IAgentCharacterEx::GetGUID</span></span>

<span data-ttu-id="a6d42-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a6d42-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

<span data-ttu-id="a6d42-105">捕獲字元的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6d42-105">Retrieves the unique ID for the character.</span></span>

-   <span data-ttu-id="a6d42-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="a6d42-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a6d42-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span><span class="sxs-lookup"><span data-stu-id="a6d42-107"><span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="a6d42-108">接收字元識別碼之 BSTR 的位址。</span><span class="sxs-lookup"><span data-stu-id="a6d42-108">Address of a BSTR that receives the ID for the character.</span></span>

</dd> </dl>

<span data-ttu-id="a6d42-109">屬性會傳回 GUID 的字串表示， (以大括弧和連字號) 格式化，以供伺服器用來唯一識別該字元。</span><span class="sxs-lookup"><span data-stu-id="a6d42-109">The property returns a string representation of the GUID (formatted with braces and dashes) that the server uses to uniquely identify the character.</span></span> <span data-ttu-id="a6d42-110">使用 Microsoft 代理程式字元編輯器來編譯時，會設定字元識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6d42-110">A character identifier is set when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="a6d42-111">此為唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="a6d42-111">The property is read-only.</span></span>

 

 





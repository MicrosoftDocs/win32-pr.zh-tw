---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311601"
---
# <a name="iagentcharactergetname"></a><span data-ttu-id="ee2ce-103">IAgentCharacter：： GetName</span><span class="sxs-lookup"><span data-stu-id="ee2ce-103">IAgentCharacter::GetName</span></span>

<span data-ttu-id="ee2ce-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="ee2ce-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

<span data-ttu-id="ee2ce-105">抓取字元的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee2ce-105">Retrieves the name of the character.</span></span>

-   <span data-ttu-id="ee2ce-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="ee2ce-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ee2ce-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span><span class="sxs-lookup"><span data-stu-id="ee2ce-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="ee2ce-108">接收字元名稱值之 BSTR 的位址。</span><span class="sxs-lookup"><span data-stu-id="ee2ce-108">The address of a BSTR that receives the value of the name for the character.</span></span>

</dd> </dl>

<span data-ttu-id="ee2ce-109">使用 Microsoft 代理程式字元編輯器來編譯時，會定義字元的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="ee2ce-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="ee2ce-110">字元的名稱可能會根據字元的語言識別項而有所不同。</span><span class="sxs-lookup"><span data-stu-id="ee2ce-110">A character's name may vary based on the character's language ID.</span></span> <span data-ttu-id="ee2ce-111">您可以使用不同的名稱來編譯不同語言的字元。</span><span class="sxs-lookup"><span data-stu-id="ee2ce-111">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="ee2ce-112">您也可以使用 **IAgentCharacter： SetName**; 設定字元的名稱。不過，這會變更所有目前字元用戶端的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee2ce-112">You can also set the character's name using **IAgentCharacter:SetName**; however, this changes the name for all current clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee2ce-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee2ce-113">See Also</span></span>

[<span data-ttu-id="ee2ce-114">**IAgentCharacter：： SetName**</span><span class="sxs-lookup"><span data-stu-id="ee2ce-114">**IAgentCharacter::SetName**</span></span>](iagentcharacter--setname.md)


 

 





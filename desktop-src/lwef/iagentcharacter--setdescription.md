---
title: IAgentCharacter SetDescription
description: IAgentCharacter SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372687"
---
# <a name="iagentcharactersetdescription"></a><span data-ttu-id="71656-103">IAgentCharacter：： SetDescription</span><span class="sxs-lookup"><span data-stu-id="71656-103">IAgentCharacter::SetDescription</span></span>

<span data-ttu-id="71656-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="71656-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

<span data-ttu-id="71656-105">設定字元的描述。</span><span class="sxs-lookup"><span data-stu-id="71656-105">Sets the description of the character.</span></span>

-   <span data-ttu-id="71656-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="71656-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="71656-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span><span class="sxs-lookup"><span data-stu-id="71656-107"><span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*</span></span>
</dt> <dd>

<span data-ttu-id="71656-108">設定字元描述的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="71656-108">A BSTR that sets the description for the character.</span></span> <span data-ttu-id="71656-109">使用 Microsoft 代理程式字元編輯器來編譯時，會定義字元的預設描述。</span><span class="sxs-lookup"><span data-stu-id="71656-109">A character's default description is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="71656-110">描述設定是選擇性的，可能不會提供所有字元。</span><span class="sxs-lookup"><span data-stu-id="71656-110">The description setting is optional and may not be supplied for all characters.</span></span> <span data-ttu-id="71656-111">您可以使用 **IAgentCharacter：： setDescription**; 來變更字元的描述。不過，這個值不是持續性 (永久儲存) 。</span><span class="sxs-lookup"><span data-stu-id="71656-111">You can change the character's description using **IAgentCharacter::setDescription**; however, this value is not persistent (stored permanently).</span></span> <span data-ttu-id="71656-112">當用戶端第一次載入字元時，字元的描述會還原為其預設設定。</span><span class="sxs-lookup"><span data-stu-id="71656-112">The character's description reverts to its default setting whenever the character is first loaded by a client.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="71656-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71656-113">See Also</span></span>

[<span data-ttu-id="71656-114">**IAgentCharacter：： GetDescription**</span><span class="sxs-lookup"><span data-stu-id="71656-114">**IAgentCharacter::GetDescription**</span></span>](iagentcharacter--getdescription.md)


 

 





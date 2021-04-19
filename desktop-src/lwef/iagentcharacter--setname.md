---
title: IAgentCharacter SetName
description: IAgentCharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969074"
---
# <a name="iagentcharactersetname"></a><span data-ttu-id="53b31-103">IAgentCharacter：： SetName</span><span class="sxs-lookup"><span data-stu-id="53b31-103">IAgentCharacter::SetName</span></span>

<span data-ttu-id="53b31-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="53b31-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

<span data-ttu-id="53b31-105">設定字元的名稱。</span><span class="sxs-lookup"><span data-stu-id="53b31-105">Sets the name of the character.</span></span>

-   <span data-ttu-id="53b31-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="53b31-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="53b31-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="53b31-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="53b31-108">設定字元名稱的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="53b31-108">A BSTR that sets the character's name.</span></span> <span data-ttu-id="53b31-109">使用 Microsoft 代理程式字元編輯器來編譯時，會定義字元的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="53b31-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="53b31-110">您可以使用 **IAgentCharacter：： SetName**; 來變更它。不過，這會變更所有目前字元用戶端的字元名稱。</span><span class="sxs-lookup"><span data-stu-id="53b31-110">You can change it using **IAgentCharacter::SetName**; however, this changes the character name for all current clients of the character.</span></span> <span data-ttu-id="53b31-111">這個屬性不是持續性 (永久儲存) 。</span><span class="sxs-lookup"><span data-stu-id="53b31-111">This property is not persistent (stored permanently).</span></span> <span data-ttu-id="53b31-112">只要用戶端第一次載入字元，字元的名稱就會還原為預設名稱。</span><span class="sxs-lookup"><span data-stu-id="53b31-112">The character's name reverts to its default name whenever the character is first loaded by a client.</span></span>

<span data-ttu-id="53b31-113">字元的名稱也可能相依于其語言識別項。</span><span class="sxs-lookup"><span data-stu-id="53b31-113">The character's name may also depend on its language ID.</span></span> <span data-ttu-id="53b31-114">您可以使用不同的名稱來編譯不同語言的字元。</span><span class="sxs-lookup"><span data-stu-id="53b31-114">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="53b31-115">伺服器使用 Microsoft 代理程式介面的部分中的字元名稱設定，例如當字元為輸入-使用中時，以及在 Microsoft Agent 工作列快顯功能表中的 [語音命令] 視窗標題。</span><span class="sxs-lookup"><span data-stu-id="53b31-115">The server uses the character's name setting in parts of the Microsoft Agent's interface, such as the Voice Commands Window title when the character is input-active and in the Microsoft Agent taskbar pop-up menu.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="53b31-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53b31-116">See Also</span></span>

[<span data-ttu-id="53b31-117">**IAgentCharacter：： GetName**</span><span class="sxs-lookup"><span data-stu-id="53b31-117">**IAgentCharacter::GetName**</span></span>](iagentcharacter--getname.md)


 

 





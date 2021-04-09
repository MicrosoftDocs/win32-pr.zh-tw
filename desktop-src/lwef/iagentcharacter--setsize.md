---
title: IAgentCharacter SetSize
description: IAgentCharacter SetSize
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39d5b33afa7ff59516b793f194a0ba186c2e002
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674991"
---
# <a name="iagentcharactersetsize"></a><span data-ttu-id="18267-103">IAgentCharacter：： SetSize</span><span class="sxs-lookup"><span data-stu-id="18267-103">IAgentCharacter::SetSize</span></span>

<span data-ttu-id="18267-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="18267-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

<span data-ttu-id="18267-105">設定字元的動畫框架大小。</span><span class="sxs-lookup"><span data-stu-id="18267-105">Sets the size of the character's animation frame.</span></span>

-   <span data-ttu-id="18267-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="18267-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="18267-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span><span class="sxs-lookup"><span data-stu-id="18267-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="18267-108">字元動畫框架的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="18267-108">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="18267-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span><span class="sxs-lookup"><span data-stu-id="18267-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="18267-110">字元動畫框架的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="18267-110">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="18267-111">變更字元的框架大小會將字元調整為使用這個方法所設定的大小。</span><span class="sxs-lookup"><span data-stu-id="18267-111">Changing the character's frame size scales the character to the size set with this method.</span></span> <span data-ttu-id="18267-112">這個屬性的設定會套用到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="18267-112">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="18267-113">雖然字元會出現在不規則形狀的區域視窗中，但字元的位置是以其矩形動畫框架為基礎。</span><span class="sxs-lookup"><span data-stu-id="18267-113">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="18267-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18267-114">See Also</span></span>

[<span data-ttu-id="18267-115">**IAgentCharacter：： GetSize**</span><span class="sxs-lookup"><span data-stu-id="18267-115">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 





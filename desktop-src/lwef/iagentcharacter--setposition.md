---
title: IAgentCharacter SetPosition
description: IAgentCharacter SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021228"
---
# <a name="iagentcharactersetposition"></a><span data-ttu-id="5b10b-103">IAgentCharacter：： SetPosition</span><span class="sxs-lookup"><span data-stu-id="5b10b-103">IAgentCharacter::SetPosition</span></span>

<span data-ttu-id="5b10b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5b10b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

<span data-ttu-id="5b10b-105">設定字元動畫框架的位置。</span><span class="sxs-lookup"><span data-stu-id="5b10b-105">Sets the position of the character's animation frame.</span></span>

-   <span data-ttu-id="5b10b-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="5b10b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5b10b-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span><span class="sxs-lookup"><span data-stu-id="5b10b-107"><span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*</span></span>
</dt> <dd>

<span data-ttu-id="5b10b-108">字元動畫框架左邊緣的螢幕座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="5b10b-108">Screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="5b10b-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span><span class="sxs-lookup"><span data-stu-id="5b10b-109"><span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*</span></span>
</dt> <dd>

<span data-ttu-id="5b10b-110">字元動畫框架的上邊緣（以圖元為單位）的螢幕座標，相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="5b10b-110">Screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="5b10b-111">這個屬性的設定會套用到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="5b10b-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="5b10b-112">雖然字元會出現在不規則形狀的區域視窗中，但字元的位置是以其矩形動畫框架為基礎。</span><span class="sxs-lookup"><span data-stu-id="5b10b-112">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

> [!Note]  
> <span data-ttu-id="5b10b-113">與 [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) 方法不同的是，此函式未排入佇列。</span><span class="sxs-lookup"><span data-stu-id="5b10b-113">Unlike the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) method, this function is not queued.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5b10b-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b10b-114">See Also</span></span>

[<span data-ttu-id="5b10b-115">**IAgentCharacter：： GetPosition**</span><span class="sxs-lookup"><span data-stu-id="5b10b-115">**IAgentCharacter::GetPosition**</span></span>](iagentcharacter--getposition.md)


 

 





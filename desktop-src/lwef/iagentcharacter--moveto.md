---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023351"
---
# <a name="iagentcharactermoveto"></a><span data-ttu-id="8c8b8-103">IAgentCharacter：： MoveTo</span><span class="sxs-lookup"><span data-stu-id="8c8b8-103">IAgentCharacter::MoveTo</span></span>

<span data-ttu-id="8c8b8-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="8c8b8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="8c8b8-105">播放相關聯的 **移動** 狀態動畫，並將字元框架移至指定的位置。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-105">Plays the associated **Moving** state animation and moves the character frame to the specified location.</span></span>

-   <span data-ttu-id="8c8b8-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="8c8b8-107">當函式傳回時，這個變數會包含要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-107">When the function returns, this variable contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="8c8b8-108"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="8c8b8-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="8c8b8-109">相對於螢幕原點的新位置 x 座標（以圖元為單位）， (左上) 。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-109">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="8c8b8-110">字元的位置是根據其動畫框架的左上角。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-110">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="8c8b8-111"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="8c8b8-111"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="8c8b8-112">新位置的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-112">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="8c8b8-113">字元的位置是根據其動畫框架的左上角。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-113">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="8c8b8-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span><span class="sxs-lookup"><span data-stu-id="8c8b8-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="8c8b8-115">參數，以毫秒為單位，指定字元的畫面格移動速度。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-115">A parameter specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="8c8b8-116">建議值為1000。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-116">The recommended value is 1000.</span></span> <span data-ttu-id="8c8b8-117">指定零 (0) 移動框架，而不播放動畫。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-117">Specifying zero (0) moves the frame without playing an animation.</span></span>

</dd> <dt>

<span data-ttu-id="8c8b8-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="8c8b8-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="8c8b8-119">接收 [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) 要求識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-119">Address of a variable that receives the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="8c8b8-120">使用 HTTP 通訊協定來存取字元和動畫資料時，請使用 [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) 方法，以確保在呼叫這個方法之前， **移動** 狀態動畫的可用性。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-120">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Moving** state animations before calling this method.</span></span> <span data-ttu-id="8c8b8-121">即使未載入動畫，伺服器還是會移動框架。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-121">Even if the animation is not loaded, the server still moves the frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c8b8-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c8b8-122">See Also</span></span>

[<span data-ttu-id="8c8b8-123">**IAgentCharacter：： SetPosition**</span><span class="sxs-lookup"><span data-stu-id="8c8b8-123">**IAgentCharacter::SetPosition**</span></span>](iagentcharacter--setposition.md)


 

 
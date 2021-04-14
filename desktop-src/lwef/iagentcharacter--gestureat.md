---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 266dc2d5e797ec0c7b30f7f827a094cd01c04195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372696"
---
# <a name="iagentcharactergestureat"></a><span data-ttu-id="535a4-103">IAgentCharacter::GestureAt</span><span class="sxs-lookup"><span data-stu-id="535a4-103">IAgentCharacter::GestureAt</span></span>

<span data-ttu-id="535a4-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="535a4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="535a4-105">根據指定的位置，播放相關聯的 **Gesturing** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="535a4-105">Plays the associated **Gesturing** state animation based on the specified location.</span></span>

-   <span data-ttu-id="535a4-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="535a4-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="535a4-107">當函式傳回時， *pdwReqID* 會包含要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="535a4-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="535a4-108"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="535a4-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="535a4-109">指定位置的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="535a4-109">The x-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="535a4-110"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="535a4-110"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="535a4-111">指定位置的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="535a4-111">The y-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="535a4-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="535a4-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="535a4-113">接收 **GestureAt** 要求識別碼之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="535a4-113">Address of a variable that receives the **GestureAt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="535a4-114">伺服器會根據字元目前的位置和指定的位置，自動決定並播放適當的 gesturing 動畫。</span><span class="sxs-lookup"><span data-stu-id="535a4-114">The server automatically determines and plays the appropriate gesturing animation based on the character's current position and the specified location.</span></span> <span data-ttu-id="535a4-115">使用 HTTP 通訊協定來存取字元和動畫資料時，請使用 [**Prepare**](iagentcharacter--prepare.md) 方法，以確保在呼叫這個方法之前可以使用動畫。</span><span class="sxs-lookup"><span data-stu-id="535a4-115">When using the HTTP protocol to access character and animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure that the animations are available before calling this method.</span></span>

 

 





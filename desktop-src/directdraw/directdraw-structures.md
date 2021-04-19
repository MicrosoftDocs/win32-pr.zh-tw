---
title: DirectDraw 結構
description: 此區段包含下列與 DirectDraw 搭配使用之結構的相關資訊
ms.assetid: 36424B41-B179-414A-ACFF-E63DA7B27043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52cf24c71da3f022833c6ecf9843e996df2c514b
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "106967699"
---
# <a name="directdraw-structures"></a><span data-ttu-id="2f590-103">DirectDraw 結構</span><span class="sxs-lookup"><span data-stu-id="2f590-103">DirectDraw Structures</span></span>

<span data-ttu-id="2f590-104">本章節包含下列與 DirectDraw 搭配使用之結構的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="2f590-104">This section contains information about the following structures used with DirectDraw:</span></span>

-   [<span data-ttu-id="2f590-105">**DDBLTBATCH**</span><span class="sxs-lookup"><span data-stu-id="2f590-105">**DDBLTBATCH**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddbltbatch)
-   [<span data-ttu-id="2f590-106">**DDBLTFX**</span><span class="sxs-lookup"><span data-stu-id="2f590-106">**DDBLTFX**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddbltfx)
-   [<span data-ttu-id="2f590-107">**DDCAPS**</span><span class="sxs-lookup"><span data-stu-id="2f590-107">**DDCAPS**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)
-   [<span data-ttu-id="2f590-108">**DDCOLORCONTROL**</span><span class="sxs-lookup"><span data-stu-id="2f590-108">**DDCOLORCONTROL**</span></span>](/windows/win32/api/ddraw/nn-ddraw-idirectdrawcolorcontrol)
-   [<span data-ttu-id="2f590-109">**DDCOLORKEY**</span><span class="sxs-lookup"><span data-stu-id="2f590-109">**DDCOLORKEY**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddcolorkey)
-   [<span data-ttu-id="2f590-110">**DDDEVICEIDENTIFIER2**</span><span class="sxs-lookup"><span data-stu-id="2f590-110">**DDDEVICEIDENTIFIER2**</span></span>](/windows/win32/api/ddraw/ns-ddraw-dddeviceidentifier2)
-   [<span data-ttu-id="2f590-111">**DDGAMMARAMP**</span><span class="sxs-lookup"><span data-stu-id="2f590-111">**DDGAMMARAMP**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddgammaramp)
-   [<span data-ttu-id="2f590-112">**DDOVERLAYFX**</span><span class="sxs-lookup"><span data-stu-id="2f590-112">**DDOVERLAYFX**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddoverlayfx)
-   [<span data-ttu-id="2f590-113">**DDPIXELFORMAT**</span><span class="sxs-lookup"><span data-stu-id="2f590-113">**DDPIXELFORMAT**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddpixelformat)
-   <span data-ttu-id="2f590-114">[**DDSCAPS**](/previous-versions/ms783271(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f590-114">[**DDSCAPS**](/previous-versions/ms783271(v=vs.85))</span></span>
-   <span data-ttu-id="2f590-115">[**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f590-115">[**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))</span></span>
-   <span data-ttu-id="2f590-116">[**DDSURFACEDESC**](/previous-versions/ms783272(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f590-116">[**DDSURFACEDESC**](/previous-versions/ms783272(v=vs.85))</span></span>
-   <span data-ttu-id="2f590-117">[**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f590-117">[**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))</span></span>

> [!Note]  
> <span data-ttu-id="2f590-118">使用結構之前，您應該將每個 DirectX 結構的記憶體初始化為0。</span><span class="sxs-lookup"><span data-stu-id="2f590-118">You should initialize the memory for each DirectX structure to 0 before you use the structure.</span></span> <span data-ttu-id="2f590-119">此外，對於包含 **dwSize** 成員的所有結構，您應該將成員設定為使用結構之前的結構大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f590-119">In addition, for all structures that contain a **dwSize** member, you should set the member to the size of the structure, in bytes, before the structure is used.</span></span> <span data-ttu-id="2f590-120">下列範例會在通用結構 [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)上執行這些工作：</span><span class="sxs-lookup"><span data-stu-id="2f590-120">The following example performs these tasks on a common structure, [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3):</span></span>

 


```
DDCAPS ddcaps; // You cannot use this yet.
 
ZeroMemory(&ddcaps, sizeof(DDCAPS));
ddcaps.dwSize = sizeof(DDCAPS);
 
// Now you can use the structure.
.
.
```



 

 





---
title: 壓縮機、Decompressors 和轉譯器的系統專案
description: 壓縮機、Decompressors 和轉譯器的系統專案
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Windows (VFW) 的影片、壓縮程式系統專案
- 適用于 Windows) 的 VFW (影片、壓縮程式系統專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675067"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a><span data-ttu-id="08db3-105">壓縮機、Decompressors 和轉譯器的系統專案</span><span class="sxs-lookup"><span data-stu-id="08db3-105">System Entries for Compressors, Decompressors, and Renderers</span></span>

<span data-ttu-id="08db3-106">系統會使用登錄中的專案來尋找 BC-VCM-LVM-HYPERV 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="08db3-106">The system uses entries in the registry to find VCM drivers.</span></span> <span data-ttu-id="08db3-107">這些專案的格式為 2 4 個字元的代碼，並以句號分隔。</span><span class="sxs-lookup"><span data-stu-id="08db3-107">These entries are in the form of two four-character codes separated by a period.</span></span> <span data-ttu-id="08db3-108">前四個字元的程式碼是由系統所定義，而且可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="08db3-108">The first four-character code is defined by the system and can be one of the following:</span></span>



| <span data-ttu-id="08db3-109">四個字元的程式碼</span><span class="sxs-lookup"><span data-stu-id="08db3-109">Four-character code</span></span> | <span data-ttu-id="08db3-110">Description</span><span class="sxs-lookup"><span data-stu-id="08db3-110">Description</span></span>                               |
|---------------------|-------------------------------------------|
| <span data-ttu-id="08db3-111">程式</span><span class="sxs-lookup"><span data-stu-id="08db3-111">"VIDC"</span></span>              | <span data-ttu-id="08db3-112">識別壓縮機和 decompressors。</span><span class="sxs-lookup"><span data-stu-id="08db3-112">Identifies compressors and decompressors.</span></span> |
| <span data-ttu-id="08db3-113">VIDS</span><span class="sxs-lookup"><span data-stu-id="08db3-113">"VIDS"</span></span>              | <span data-ttu-id="08db3-114">識別影片資料流程轉譯器。</span><span class="sxs-lookup"><span data-stu-id="08db3-114">Identifies video-stream renderers.</span></span>        |
| <span data-ttu-id="08db3-115">"TXTS"</span><span class="sxs-lookup"><span data-stu-id="08db3-115">"TXTS"</span></span>              | <span data-ttu-id="08db3-116">識別文字資料流程轉譯器。</span><span class="sxs-lookup"><span data-stu-id="08db3-116">Identifies text-stream renderers.</span></span>         |
| <span data-ttu-id="08db3-117">"AUDS"</span><span class="sxs-lookup"><span data-stu-id="08db3-117">"AUDS"</span></span>              | <span data-ttu-id="08db3-118">識別音訊資料流程處理常式。</span><span class="sxs-lookup"><span data-stu-id="08db3-118">Identifies audio-stream handlers.</span></span>         |



 

<span data-ttu-id="08db3-119">自訂轉譯器可以定義自己的四個字元的代碼。</span><span class="sxs-lookup"><span data-stu-id="08db3-119">Custom renderers can define their own four-character codes.</span></span>

<span data-ttu-id="08db3-120">第二個四個字元的程式碼是由驅動程式所定義。</span><span class="sxs-lookup"><span data-stu-id="08db3-120">The second four-character code is defined by the driver.</span></span> <span data-ttu-id="08db3-121">一般來說，第二個四個字元的程式碼會對應至驅動程式可處理的資料類型。</span><span class="sxs-lookup"><span data-stu-id="08db3-121">Typically, the second four-character code corresponds to the type of data the driver can handle.</span></span>

<span data-ttu-id="08db3-122">開啟 BC-VCM-LVM-HYPERV 驅動程式時，應用程式會指定驅動程式的類型，以及它所需的資料處理程式類型。</span><span class="sxs-lookup"><span data-stu-id="08db3-122">When opening a VCM driver, an application specifies the type of driver and the type of data handler it needs.</span></span> <span data-ttu-id="08db3-123">一般而言，這是來自資料流程標頭的資訊。</span><span class="sxs-lookup"><span data-stu-id="08db3-123">Typically, this information comes from the stream header.</span></span> <span data-ttu-id="08db3-124">系統會嘗試開啟指定的資料處理程式，但如果失敗，系統就會在登錄中搜尋具有必要處理常式的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="08db3-124">The system tries to open the specified data handler, but if it fails, the system searches the registry for a driver that has the required handler.</span></span>

<span data-ttu-id="08db3-125">搜尋驅動程式時，系統會嘗試比對驅動程式類型和資料處理程式所指定的四個字元碼與驅動程式專案中所指定的代碼。</span><span class="sxs-lookup"><span data-stu-id="08db3-125">When searching for the driver, the system tries to match the four-character codes specified for the driver type and data handler with those specified in the driver entry.</span></span> <span data-ttu-id="08db3-126">例如，如果應用程式指定了壓縮程式 MSSQ，系統就會在登錄中搜尋驅動程式專案程式. MSSQ。</span><span class="sxs-lookup"><span data-stu-id="08db3-126">For example, if an application specifies the compressor MSSQ, the system searches the registry for the driver entry VIDC.MSSQ.</span></span> <span data-ttu-id="08db3-127">如果找不到相符項，則會開啟對應至驅動程式類型的每個驅動程式，並找出可處理您應用程式所指定之資料類型的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="08db3-127">If it cannot find a match, it opens each driver corresponding to the driver type and locates one that can handle the type of data your application specifies.</span></span> <span data-ttu-id="08db3-128">在上述範例中，如果系統找不到程式 MSSQ，則會以 "程式" 四個字元的程式碼開啟所有驅動程式，並找出可處理資料的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="08db3-128">In the previous example, if the system could not find VIDC.MSSQ, it would open all drivers with the "VIDC" four-character code and locate one that can handle the data.</span></span>

 

 





---
description: 下列函式搭配輸出保護管理員使用 (OPM) 。
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: OPM 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980735"
---
# <a name="opm-functions"></a><span data-ttu-id="8cca4-103">OPM 函式</span><span class="sxs-lookup"><span data-stu-id="8cca4-103">OPM Functions</span></span>

<span data-ttu-id="8cca4-104">下列函式搭配 [輸出保護管理員](output-protection-manager.md) 使用 (OPM) 。</span><span class="sxs-lookup"><span data-stu-id="8cca4-104">The following functions are used with [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>



| <span data-ttu-id="8cca4-105">函式</span><span class="sxs-lookup"><span data-stu-id="8cca4-105">Function</span></span>                                                                                             | <span data-ttu-id="8cca4-106">描述</span><span class="sxs-lookup"><span data-stu-id="8cca4-106">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cca4-107">**OPMGetVideoOutputForTarget**</span><span class="sxs-lookup"><span data-stu-id="8cca4-107">**OPMGetVideoOutputForTarget**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | <span data-ttu-id="8cca4-108">傳回指定介面卡上之 VidPN 目標的影片輸出物件。</span><span class="sxs-lookup"><span data-stu-id="8cca4-108">Returns a video output object for the VidPN target on the specified adapter.</span></span>                                                          |
| [<span data-ttu-id="8cca4-109">**OPMGetVideoOutputsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="8cca4-109">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | <span data-ttu-id="8cca4-110">針對每個與特定 **HMONITOR** 控制碼相關聯的實體監視器，建立輸出保護管理員 (OPM) 物件。</span><span class="sxs-lookup"><span data-stu-id="8cca4-110">Creates an Output Protection Manager (OPM) object for each physical monitor that is associated with a particular **HMONITOR** handle.</span></span> |
| [<span data-ttu-id="8cca4-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="8cca4-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | <span data-ttu-id="8cca4-112">為每個與特定 Direct3D 裝置相關聯的實體監視器建立 OPM 物件。</span><span class="sxs-lookup"><span data-stu-id="8cca4-112">Creates an OPM object for each physical monitor that is associated with a particular Direct3D device.</span></span>                                 |



 

<span data-ttu-id="8cca4-113">OPM 會使用下列功能來存取顯示驅動程式中的功能。</span><span class="sxs-lookup"><span data-stu-id="8cca4-113">The following functions are used by OPM to access functionality in the display driver.</span></span> <span data-ttu-id="8cca4-114">應用程式不應呼叫這些函式。</span><span class="sxs-lookup"><span data-stu-id="8cca4-114">Applications should not call these functions.</span></span>

-   [<span data-ttu-id="8cca4-115">**ConfigureOPMProtectedOutput**</span><span class="sxs-lookup"><span data-stu-id="8cca4-115">**ConfigureOPMProtectedOutput**</span></span>](configureopmprotectedoutput.md)
-   [<span data-ttu-id="8cca4-116">**CreateOPMProtectedOutputs**</span><span class="sxs-lookup"><span data-stu-id="8cca4-116">**CreateOPMProtectedOutputs**</span></span>](createopmprotectedoutputs.md)
-   [<span data-ttu-id="8cca4-117">**DestroyOPMProtectedOutput**</span><span class="sxs-lookup"><span data-stu-id="8cca4-117">**DestroyOPMProtectedOutput**</span></span>](destroyopmprotectedoutput.md)
-   [<span data-ttu-id="8cca4-118">**GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="8cca4-118">**GetCertificate**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [<span data-ttu-id="8cca4-119">**GetCertificateSize**</span><span class="sxs-lookup"><span data-stu-id="8cca4-119">**GetCertificateSize**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [<span data-ttu-id="8cca4-120">**GetCOPPCompatibleOPMInformation**</span><span class="sxs-lookup"><span data-stu-id="8cca4-120">**GetCOPPCompatibleOPMInformation**</span></span>](getcoppcompatibleopminformation.md)
-   [<span data-ttu-id="8cca4-121">**GetOPMInformation**</span><span class="sxs-lookup"><span data-stu-id="8cca4-121">**GetOPMInformation**</span></span>](getopminformation.md)
-   [<span data-ttu-id="8cca4-122">**GetOPMRandomNumber**</span><span class="sxs-lookup"><span data-stu-id="8cca4-122">**GetOPMRandomNumber**</span></span>](getopmrandomnumber.md)
-   [<span data-ttu-id="8cca4-123">**GetSuggestedOPMProtectedOutputArraySize**</span><span class="sxs-lookup"><span data-stu-id="8cca4-123">**GetSuggestedOPMProtectedOutputArraySize**</span></span>](getsuggestedopmprotectedoutputarraysize.md)
-   [<span data-ttu-id="8cca4-124">**SetOPMSigningKeyAndSequenceNumbers**</span><span class="sxs-lookup"><span data-stu-id="8cca4-124">**SetOPMSigningKeyAndSequenceNumbers**</span></span>](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a><span data-ttu-id="8cca4-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="8cca4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cca4-126">OPM 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="8cca4-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="8cca4-127">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="8cca4-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 




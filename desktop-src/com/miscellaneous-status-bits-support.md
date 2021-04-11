---
title: 其他狀態位支援
description: 其他狀態位支援
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c281b52283796d67c476e8ee00383436bc2235a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020768"
---
# <a name="miscellaneous-status-bits-support"></a><span data-ttu-id="34c73-103">其他狀態位支援</span><span class="sxs-lookup"><span data-stu-id="34c73-103">Miscellaneous Status Bits Support</span></span>

<span data-ttu-id="34c73-104">ActiveX 控制項容器必須辨識並支援下列 OLEMISC \_ 狀態位。</span><span class="sxs-lookup"><span data-stu-id="34c73-104">ActiveX Control Containers must recognize and support the following OLEMISC\_ status bits.</span></span>



| <span data-ttu-id="34c73-105">狀態位</span><span class="sxs-lookup"><span data-stu-id="34c73-105">Status Bit</span></span>                           | <span data-ttu-id="34c73-106">必要？</span><span class="sxs-lookup"><span data-stu-id="34c73-106">Required?</span></span>      | <span data-ttu-id="34c73-107">註解</span><span class="sxs-lookup"><span data-stu-id="34c73-107">Comments</span></span>                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c73-108">ACTI加值稅EWHENVISIBLE</span><span class="sxs-lookup"><span data-stu-id="34c73-108">ACTIVATEWHENVISIBLE</span></span><br/>       | <span data-ttu-id="34c73-109">Yes</span><span class="sxs-lookup"><span data-stu-id="34c73-109">Yes</span></span><br/> |                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="34c73-110">IGNOREACTI加值稅EWHENVISIBLE</span><span class="sxs-lookup"><span data-stu-id="34c73-110">IGNOREACTIVATEWHENVISIBLE</span></span><br/> | <span data-ttu-id="34c73-111">No</span><span class="sxs-lookup"><span data-stu-id="34c73-111">No</span></span><br/>  | <span data-ttu-id="34c73-112">非作用中和無視窗控制項支援所需。</span><span class="sxs-lookup"><span data-stu-id="34c73-112">Needed for inactive and windowless control support.</span></span> <span data-ttu-id="34c73-113">IGNOREACTI加值稅EWHENVISIBLE 位適用于裝載非使用中和無視窗控制項的容器。</span><span class="sxs-lookup"><span data-stu-id="34c73-113">The IGNOREACTIVATEWHENVISIBLE bit is for containers hosting inactive and windowless controls.</span></span> <span data-ttu-id="34c73-114">IGNOREACTI加值稅EWHENVISIBLE 位引進為 ActiveX 控制項96規格的一部分，請參閱此檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="34c73-114">The IGNOREACTIVATEWHENVISIBLE bit is introduced as part of the ActiveX Controls 96 specification, see this documentation for more details.</span></span><br/> |
| <span data-ttu-id="34c73-115">INSIDEOUT</span><span class="sxs-lookup"><span data-stu-id="34c73-115">INSIDEOUT</span></span><br/>                 | <span data-ttu-id="34c73-116">No</span><span class="sxs-lookup"><span data-stu-id="34c73-116">No</span></span><br/>  | <span data-ttu-id="34c73-117">通常不會與 ActiveX 控制項搭配使用，而是使用複合檔案內嵌。</span><span class="sxs-lookup"><span data-stu-id="34c73-117">Not generally used with ActiveX Controls but rather with compound document embeddings.</span></span> <span data-ttu-id="34c73-118">請注意，這與某些 SDK 檔相反，此位必須設定為要設定 ACTI加值稅EWHENVISIBLE 位。</span><span class="sxs-lookup"><span data-stu-id="34c73-118">Note this is contrary to some SDK documentation that says this bit must be set for the ACTIVATEWHENVISIBLE bit to be set.</span></span><br/>                                                                             |
| <span data-ttu-id="34c73-119">INVISIBLEATRUNTIME</span><span class="sxs-lookup"><span data-stu-id="34c73-119">INVISIBLEATRUNTIME</span></span><br/>        | <span data-ttu-id="34c73-120">Yes</span><span class="sxs-lookup"><span data-stu-id="34c73-120">Yes</span></span><br/> | <span data-ttu-id="34c73-121">指定應在設計階段顯示的控制項，但在執行時間不可見。</span><span class="sxs-lookup"><span data-stu-id="34c73-121">Designates a control that should be visible at design time, but invisible at run time.</span></span><br/>                                                                                                                                                                                                       |
| <span data-ttu-id="34c73-122">ALWAYSRUN</span><span class="sxs-lookup"><span data-stu-id="34c73-122">ALWAYSRUN</span></span><br/>                 | <span data-ttu-id="34c73-123">Yes</span><span class="sxs-lookup"><span data-stu-id="34c73-123">Yes</span></span><br/> |                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="34c73-124">ACTSLIKEBUTTON</span><span class="sxs-lookup"><span data-stu-id="34c73-124">ACTSLIKEBUTTON</span></span><br/>            | <span data-ttu-id="34c73-125">No</span><span class="sxs-lookup"><span data-stu-id="34c73-125">No</span></span><br/>  | <span data-ttu-id="34c73-126">雖然檔樣式的容器不需要支援，但通常是強制性的支援。</span><span class="sxs-lookup"><span data-stu-id="34c73-126">Support is normally mandatory although it is not necessary for document style containers.</span></span><br/>                                                                                                                                                                                                    |
| <span data-ttu-id="34c73-127">ACTSLIKELABEL</span><span class="sxs-lookup"><span data-stu-id="34c73-127">ACTSLIKELABEL</span></span><br/>             | <span data-ttu-id="34c73-128">No</span><span class="sxs-lookup"><span data-stu-id="34c73-128">No</span></span><br/>  | <span data-ttu-id="34c73-129">雖然檔樣式的容器不需要支援，但通常是強制性的支援。</span><span class="sxs-lookup"><span data-stu-id="34c73-129">Support is normally mandatory although it is not necessary for document style containers.</span></span><br/>                                                                                                                                                                                                    |
| <span data-ttu-id="34c73-130">NOUIACTI加值稅E</span><span class="sxs-lookup"><span data-stu-id="34c73-130">NOUIACTIVATE</span></span><br/>              | <span data-ttu-id="34c73-131">Yes</span><span class="sxs-lookup"><span data-stu-id="34c73-131">Yes</span></span><br/> |                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="34c73-132">ALIGNABLE</span><span class="sxs-lookup"><span data-stu-id="34c73-132">ALIGNABLE</span></span><br/>                 | <span data-ttu-id="34c73-133">No</span><span class="sxs-lookup"><span data-stu-id="34c73-133">No</span></span><br/>  |                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="34c73-134">SIMPLEFRAME</span><span class="sxs-lookup"><span data-stu-id="34c73-134">SIMPLEFRAME</span></span><br/>               | <span data-ttu-id="34c73-135">No</span><span class="sxs-lookup"><span data-stu-id="34c73-135">No</span></span><br/>  | <span data-ttu-id="34c73-136">查看[簡單的框架網站](simple-frame-site-containment.md)內含專案</span><span class="sxs-lookup"><span data-stu-id="34c73-136">See [Simple Frame Site Containment](simple-frame-site-containment.md)</span></span><br/>                                                                                                                                                                                                                       |
| <span data-ttu-id="34c73-137">SETCLIENTSITEFIRST</span><span class="sxs-lookup"><span data-stu-id="34c73-137">SETCLIENTSITEFIRST</span></span><br/>        | <span data-ttu-id="34c73-138">No</span><span class="sxs-lookup"><span data-stu-id="34c73-138">No</span></span><br/>  | <span data-ttu-id="34c73-139">建議使用此位的支援，但不是強制性。</span><span class="sxs-lookup"><span data-stu-id="34c73-139">Support for this bit is recommended but not mandatory.</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="34c73-140">IMEMODE</span><span class="sxs-lookup"><span data-stu-id="34c73-140">IMEMODE</span></span><br/>                   | <span data-ttu-id="34c73-141">No</span><span class="sxs-lookup"><span data-stu-id="34c73-141">No</span></span><br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="34c73-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="34c73-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34c73-143">容器</span><span class="sxs-lookup"><span data-stu-id="34c73-143">Containers</span></span>](containers.md)
</dt> </dl>

 

 






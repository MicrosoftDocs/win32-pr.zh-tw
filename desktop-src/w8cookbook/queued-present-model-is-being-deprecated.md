---
title: 已取代佇列的目前模型
description: 已取代佇列的目前模型
ms.assetid: 271CD4F7-0992-47DB-AF5A-B77570EF681A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5713009cd5cd3a575d0d634f81fce7a289d1c1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "106965046"
---
# <a name="queued-present-model-is-being-deprecated"></a><span data-ttu-id="8cf70-103">已取代佇列的目前模型</span><span class="sxs-lookup"><span data-stu-id="8cf70-103">Queued present model is being deprecated</span></span>

## <a name="platforms"></a><span data-ttu-id="8cf70-104">平台</span><span class="sxs-lookup"><span data-stu-id="8cf70-104">Platforms</span></span>

<span data-ttu-id="8cf70-105">**用戶端** – Windows 8 後</span><span class="sxs-lookup"><span data-stu-id="8cf70-105">**Clients** – After Windows 8</span></span>  
<span data-ttu-id="8cf70-106">**伺服器** – Windows Server 2012 之後</span><span class="sxs-lookup"><span data-stu-id="8cf70-106">**Servers** – After Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="8cf70-107">Description</span><span class="sxs-lookup"><span data-stu-id="8cf70-107">Description</span></span>

<span data-ttu-id="8cf70-108">在 Windows 8 後的 Windows 版本中，這些 Api 會傳回 E \_ >notimpl：</span><span class="sxs-lookup"><span data-stu-id="8cf70-108">In the Windows release after Windows 8, these APIs will return E\_NOTIMPL:</span></span>

-   <span data-ttu-id="8cf70-109">DwmSetPresentParameters</span><span class="sxs-lookup"><span data-stu-id="8cf70-109">DwmSetPresentParameters</span></span>
-   <span data-ttu-id="8cf70-110">DwmSetDxFrameDuration</span><span class="sxs-lookup"><span data-stu-id="8cf70-110">DwmSetDxFrameDuration</span></span>
-   <span data-ttu-id="8cf70-111">DwmModifyPreviousDxFrameDuration</span><span class="sxs-lookup"><span data-stu-id="8cf70-111">DwmModifyPreviousDxFrameDuration</span></span>

<span data-ttu-id="8cf70-112">此外，此 API 只會接受 hwnd 參數的 Null 值：</span><span class="sxs-lookup"><span data-stu-id="8cf70-112">In addition, this API will only accept the NULL value for the hwnd parameter:</span></span>

-   <span data-ttu-id="8cf70-113">DwmGetCompositionTimingInfo</span><span class="sxs-lookup"><span data-stu-id="8cf70-113">DwmGetCompositionTimingInfo</span></span>

<span data-ttu-id="8cf70-114">我們將停止支援具有 hwnd！ = Null 的 DwmGetCompositionTimingInfo，並移除相關聯的功能。</span><span class="sxs-lookup"><span data-stu-id="8cf70-114">We will stop supporting DwmGetCompositionTimingInfo with hwnd != NULL and remove associated functionality.</span></span> <span data-ttu-id="8cf70-115">如果指定 hwnd 的非 Null 值，此 API 將會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="8cf70-115">If non-NULL value for hwnd is specified, this API will return E\_INVALIDARG.</span></span>

<span data-ttu-id="8cf70-116">我們也鼓勵使用 DwmGetCompositionTimingInfo API，並建議開發人員切換至 DXGI 翻轉模型和相關聯的 DX 目前統計資料 API。</span><span class="sxs-lookup"><span data-stu-id="8cf70-116">We also discourage the use of DwmGetCompositionTimingInfo API and suggest that developers switch to the DXGI flip model and associated DX present statistics API.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8cf70-117">表現</span><span class="sxs-lookup"><span data-stu-id="8cf70-117">Manifestation</span></span>

<span data-ttu-id="8cf70-118">使用佇列的目前模型的應用程式將無法正確運作。</span><span class="sxs-lookup"><span data-stu-id="8cf70-118">Applications that use the queued present model will not function correctly.</span></span> <span data-ttu-id="8cf70-119">確切的外觀取決於特定的應用程式，但其範圍可能從不正確的呈現時機，到應用程式意外結束) 。</span><span class="sxs-lookup"><span data-stu-id="8cf70-119">The exact manifestation depends on the particular application, but can range from incorrect presentation timing to the application exiting unexpectedly).</span></span> <span data-ttu-id="8cf70-120">在實務上，如果有任何) 這類應用程式，我們就不會看到許多 (。</span><span class="sxs-lookup"><span data-stu-id="8cf70-120">In practice, we do not expect to see many (if any) such applications.</span></span> <span data-ttu-id="8cf70-121">這是 Vista media player 使用的模型，這種模型不會用在 Windows 8 (上，也可能) 舊的 Zune 播放程式。</span><span class="sxs-lookup"><span data-stu-id="8cf70-121">This model was used by Vista media player, which will not be used on Windows 8 (and possibly the old Zune player).</span></span> <span data-ttu-id="8cf70-122">目前，我們沒有任何其他應用程式實際使用此模型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8cf70-122">At this time we don’t have info about any other applications actually using this model.</span></span>

## <a name="solution"></a><span data-ttu-id="8cf70-123">解決方法</span><span class="sxs-lookup"><span data-stu-id="8cf70-123">Solution</span></span>

<span data-ttu-id="8cf70-124">開發人員必須使用 [DXGI 翻轉] 呈現模式，而不是從 Windows 7 開始，DX9 執行時間中提供的佇列存在 (，以及 DX10 和 DX11 相互作用執行時間的 Windows 8) 。</span><span class="sxs-lookup"><span data-stu-id="8cf70-124">Developers need to use the DXGI flip presentation mode instead of queued present (available in DX9 runtime since Windows 7, and on DX10 and DX11 runtimes in Windows 8).</span></span>

## <a name="tests"></a><span data-ttu-id="8cf70-125">測試</span><span class="sxs-lookup"><span data-stu-id="8cf70-125">Tests</span></span>

<span data-ttu-id="8cf70-126">執行一般測試，以確保收件匣 Windows 元件和主要產品可在下一版 Windows 上繼續運作。</span><span class="sxs-lookup"><span data-stu-id="8cf70-126">Run general tests to ensure that inbox Windows components and major products continue to work on the next version of Windows.</span></span>

 

 





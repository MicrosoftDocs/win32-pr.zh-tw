---
description: 這些選項會識別查詢資源類型。
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f5dda7f84dfa36e4f3b7ece1b359a4841bbbf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110761"
---
# <a name="d3dusage_query"></a><span data-ttu-id="28c43-103">D3DUSAGE \_ 查詢</span><span class="sxs-lookup"><span data-stu-id="28c43-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="28c43-104">這些選項會識別查詢資源類型。</span><span class="sxs-lookup"><span data-stu-id="28c43-104">These options identify query resource types.</span></span>



|                                            |                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c43-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="28c43-105">\#define</span></span>                                   | <span data-ttu-id="28c43-106">Description</span><span class="sxs-lookup"><span data-stu-id="28c43-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="28c43-107">D3DUSAGE \_ 查詢 \_ 篩選</span><span class="sxs-lookup"><span data-stu-id="28c43-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="28c43-108">查詢資源格式，以查看它是否支援 D3DTEXF 點以外的材質篩選器類型， \_ (一律支援) 。</span><span class="sxs-lookup"><span data-stu-id="28c43-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="28c43-109">D3DUSAGE \_ 查詢 \_ LEGACYBUMPMAP</span><span class="sxs-lookup"><span data-stu-id="28c43-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="28c43-110">查詢有關舊版凹凸地圖的資源。</span><span class="sxs-lookup"><span data-stu-id="28c43-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="28c43-111">D3DUSAGE \_ QUERY \_ POSTPIXELSHADER \_ 混色</span><span class="sxs-lookup"><span data-stu-id="28c43-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="28c43-112">查詢資源以驗證支援的 post 圖元著色器混色支援。</span><span class="sxs-lookup"><span data-stu-id="28c43-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="28c43-113">如果 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 因為 D3DUSAGE \_ QUERY \_ POSTPIXELSHADER 混色而失敗 \_ ，則不支援 post 圖元混合作業。</span><span class="sxs-lookup"><span data-stu-id="28c43-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="28c43-114">這些包括 Alpha 測試、圖元霧化、轉譯目標混色、色彩寫入啟用和遞色。</span><span class="sxs-lookup"><span data-stu-id="28c43-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="28c43-115">D3DUSAGE \_ 查詢 \_ SRGBREAD</span><span class="sxs-lookup"><span data-stu-id="28c43-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="28c43-116">查詢資源，以確認材質在讀取作業期間是否支援 gamma 修正。</span><span class="sxs-lookup"><span data-stu-id="28c43-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="28c43-117">D3DUSAGE \_ 查詢 \_ SRGBWRITE</span><span class="sxs-lookup"><span data-stu-id="28c43-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="28c43-118">查詢資源，以確認材質在寫入作業期間是否支援 gamma 修正。</span><span class="sxs-lookup"><span data-stu-id="28c43-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="28c43-119">D3DUSAGE \_ 查詢 \_ VERTEXTEXTURE</span><span class="sxs-lookup"><span data-stu-id="28c43-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="28c43-120">查詢資源以驗證端點著色器紋理取樣的支援。</span><span class="sxs-lookup"><span data-stu-id="28c43-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="28c43-121">D3DUSAGE \_ 查詢 \_ WRAPANDMIP</span><span class="sxs-lookup"><span data-stu-id="28c43-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="28c43-122">查詢資源以確認紋理包裝和 mip 對應的支援。</span><span class="sxs-lookup"><span data-stu-id="28c43-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="28c43-123">使用 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) 來查詢這些使用方式的硬體支援，以及 [D3DUSAGE](d3dusage.md)中列出的其他使用方式。</span><span class="sxs-lookup"><span data-stu-id="28c43-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="28c43-124">常數資訊</span><span class="sxs-lookup"><span data-stu-id="28c43-124">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="28c43-125">標頭</span><span class="sxs-lookup"><span data-stu-id="28c43-125">Header</span></span>                   | <span data-ttu-id="28c43-126">d3d9types。h</span><span class="sxs-lookup"><span data-stu-id="28c43-126">d3d9types.h</span></span> |
| <span data-ttu-id="28c43-127">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="28c43-127">Minimum operating system</span></span> | <span data-ttu-id="28c43-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="28c43-128">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="28c43-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="28c43-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28c43-130">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="28c43-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

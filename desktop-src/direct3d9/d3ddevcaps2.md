---
description: D3DDEVCAPS2 驅動程式功能旗標。
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ef30540f19add130aaca6eb48655a5ac47b2b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999465"
---
# <a name="d3ddevcaps2"></a><span data-ttu-id="54566-103">D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="54566-103">D3DDEVCAPS2</span></span>

<span data-ttu-id="54566-104">D3DDEVCAPS2 驅動程式功能旗標。</span><span class="sxs-lookup"><span data-stu-id="54566-104">D3DDEVCAPS2 driver capability flags.</span></span>



| <span data-ttu-id="54566-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="54566-105">\#define</span></span>                                        | <span data-ttu-id="54566-106">Description</span><span class="sxs-lookup"><span data-stu-id="54566-106">Description</span></span>                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54566-107">D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH</span><span class="sxs-lookup"><span data-stu-id="54566-107">D3DDEVCAPS2\_ADAPTIVETESSRTPATCH</span></span>                | <span data-ttu-id="54566-108">裝置支援 RT-修補程式的自我調整鑲嵌</span><span class="sxs-lookup"><span data-stu-id="54566-108">Device supports adaptive tessellation of RT-patches</span></span>                                                                                                                                                                       |
| <span data-ttu-id="54566-109">D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH</span><span class="sxs-lookup"><span data-stu-id="54566-109">D3DDEVCAPS2\_ADAPTIVETESSNPATCH</span></span>                 | <span data-ttu-id="54566-110">裝置支援自我調整的 N 個修補程式鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="54566-110">Device supports adaptive tessellation of N-patches.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="54566-111">D3DDEVCAPS2 \_ 可以 \_ \_ 從 \_ 紋理 STRETCHRECT</span><span class="sxs-lookup"><span data-stu-id="54566-111">D3DDEVCAPS2\_CAN\_STRETCHRECT\_FROM\_TEXTURES</span></span>   | <span data-ttu-id="54566-112">裝置支援使用材質作為來源的 [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) 。</span><span class="sxs-lookup"><span data-stu-id="54566-112">Device supports [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) using a texture as the source.</span></span>                                                                                                                       |
| <span data-ttu-id="54566-113">D3DDEVCAPS2 \_ DMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="54566-113">D3DDEVCAPS2\_DMAPNPATCH</span></span>                         | <span data-ttu-id="54566-114">裝置支援 N 個修補程式的置換對應。</span><span class="sxs-lookup"><span data-stu-id="54566-114">Device supports displacement maps for N-patches.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="54566-115">D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="54566-115">D3DDEVCAPS2\_PRESAMPLEDDMAPNPATCH</span></span>               | <span data-ttu-id="54566-116">裝置支援 N 個修補程式的 presampled 置換對應。</span><span class="sxs-lookup"><span data-stu-id="54566-116">Device supports presampled displacement maps for N-patches.</span></span> <span data-ttu-id="54566-117">如需置換對應的詳細資訊，請參閱 [ (Direct3D 9) 的置換對應 ](displacement-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="54566-117">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span>                                           |
| <span data-ttu-id="54566-118">D3DDEVCAPS2 \_ STREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="54566-118">D3DDEVCAPS2\_STREAMOFFSET</span></span>                       | <span data-ttu-id="54566-119">裝置支援資料流程位移。</span><span class="sxs-lookup"><span data-stu-id="54566-119">Device supports stream offsets.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="54566-120">D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="54566-120">D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET</span></span> | <span data-ttu-id="54566-121">如果 \_ 裝置已設定 D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET，且頂點宣告沒有具有 D3DDECLUSAGE POSITIONT0 的元素，則多個頂點元素可以在資料流程中共用相同的位移 \_ 。</span><span class="sxs-lookup"><span data-stu-id="54566-121">Multiple vertex elements can share the same offset in a stream if D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET is set by the device and the vertex declaration does not have an element with D3DDECLUSAGE\_POSITIONT0.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="54566-122">常數資訊</span><span class="sxs-lookup"><span data-stu-id="54566-122">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="54566-123">標頭</span><span class="sxs-lookup"><span data-stu-id="54566-123">Header</span></span>                   | <span data-ttu-id="54566-124">d3d9caps。h</span><span class="sxs-lookup"><span data-stu-id="54566-124">d3d9caps.h</span></span> |
| <span data-ttu-id="54566-125">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="54566-125">Minimum operating system</span></span> | <span data-ttu-id="54566-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="54566-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="54566-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="54566-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54566-128">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="54566-128">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

---
description: 協助您瞭解應用程式效能的輸送量計量。
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: 'D3DDEVINFO_D3D9BANDWIDTHTIMINGS 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196217"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a><span data-ttu-id="03cf7-103">D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS 結構</span><span class="sxs-lookup"><span data-stu-id="03cf7-103">D3DDEVINFO\_D3D9BANDWIDTHTIMINGS structure</span></span>

<span data-ttu-id="03cf7-104">協助您瞭解應用程式效能的輸送量計量。</span><span class="sxs-lookup"><span data-stu-id="03cf7-104">Throughput metrics for help in understanding the performance of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="03cf7-105">語法</span><span class="sxs-lookup"><span data-stu-id="03cf7-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a><span data-ttu-id="03cf7-106">成員</span><span class="sxs-lookup"><span data-stu-id="03cf7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="03cf7-107">**MaxBandwidthUtilized**</span><span class="sxs-lookup"><span data-stu-id="03cf7-107">**MaxBandwidthUtilized**</span></span>
</dt> <dd>

<span data-ttu-id="03cf7-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03cf7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03cf7-109">從主機 CPU 到 GPU 的頻寬或最大資料傳輸速率。</span><span class="sxs-lookup"><span data-stu-id="03cf7-109">The bandwidth or maximum data transfer rate from the host CPU to the GPU.</span></span> <span data-ttu-id="03cf7-110">這通常是連接 CPU 和 GPU 的 PCI 或 AGP 匯流排的頻寬。</span><span class="sxs-lookup"><span data-stu-id="03cf7-110">This is typically the bandwidth of the PCI or AGP bus which connects the CPU and the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="03cf7-111">**FrontEndUploadMemoryUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="03cf7-111">**FrontEndUploadMemoryUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="03cf7-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03cf7-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03cf7-113">將資料從主機 CPU 上傳至 GPU 時的記憶體使用量百分比。</span><span class="sxs-lookup"><span data-stu-id="03cf7-113">Memory utilized percentage when uploading data from the host CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="03cf7-114">**VertexRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="03cf7-114">**VertexRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="03cf7-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03cf7-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03cf7-116">頂點輸送量百分比。</span><span class="sxs-lookup"><span data-stu-id="03cf7-116">Vertex throughput percentage.</span></span> <span data-ttu-id="03cf7-117">這是與理論最大頂點處理速率相較之下，所處理的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="03cf7-117">This is the number of vertices processed compared to the theoretical maximum vertex processing rate.</span></span>

</dd> <dt>

<span data-ttu-id="03cf7-118">**TriangleSetupRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="03cf7-118">**TriangleSetupRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="03cf7-119">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03cf7-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03cf7-120">三角形的設定輸送量百分比。</span><span class="sxs-lookup"><span data-stu-id="03cf7-120">Triangle set-up throughput percentage.</span></span> <span data-ttu-id="03cf7-121">這是與理論最大三角形設定速率相較之下，針對點陣設定的三角形數目。</span><span class="sxs-lookup"><span data-stu-id="03cf7-121">This is the number of triangles that are set up for rasterization compared to the theoretical maximum triangle set-up rate.</span></span>

</dd> <dt>

<span data-ttu-id="03cf7-122">**FillRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="03cf7-122">**FillRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="03cf7-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="03cf7-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="03cf7-124">圖元填滿輸送量百分比。</span><span class="sxs-lookup"><span data-stu-id="03cf7-124">Pixel fill throughput percentage.</span></span> <span data-ttu-id="03cf7-125">這是相較于理論圖元填滿而填滿的圖元數目。</span><span class="sxs-lookup"><span data-stu-id="03cf7-125">This is the number of pixels that are filled compared to the theoretical pixel fill.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03cf7-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="03cf7-126">Requirements</span></span>



| <span data-ttu-id="03cf7-127">需求</span><span class="sxs-lookup"><span data-stu-id="03cf7-127">Requirement</span></span> | <span data-ttu-id="03cf7-128">值</span><span class="sxs-lookup"><span data-stu-id="03cf7-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03cf7-129">標頭</span><span class="sxs-lookup"><span data-stu-id="03cf7-129">Header</span></span><br/> | <dl> <span data-ttu-id="03cf7-130"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="03cf7-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03cf7-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03cf7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03cf7-132">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="03cf7-132">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="03cf7-133">**GetData**</span><span class="sxs-lookup"><span data-stu-id="03cf7-133">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 

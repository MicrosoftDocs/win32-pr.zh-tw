---
description: 驅動程式材質座標功能旗標。
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da9ca23ebc4dd121527721a9d10a2db55a4d555
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995255"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="c621b-103">D3DTSS \_ TCI</span><span class="sxs-lookup"><span data-stu-id="c621b-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="c621b-104">驅動程式材質座標功能旗標。</span><span class="sxs-lookup"><span data-stu-id="c621b-104">Driver texture coordinate capability flags.</span></span>



| <span data-ttu-id="c621b-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="c621b-105">\#define</span></span>                                 | <span data-ttu-id="c621b-106">值</span><span class="sxs-lookup"><span data-stu-id="c621b-106">Value</span></span>       | <span data-ttu-id="c621b-107">描述</span><span class="sxs-lookup"><span data-stu-id="c621b-107">Description</span></span>                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c621b-108">D3DTSS \_ TCI \_ PASSTHRU</span><span class="sxs-lookup"><span data-stu-id="c621b-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="c621b-109">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="c621b-109">0x00000000L</span></span> | <span data-ttu-id="c621b-110">使用包含在頂點格式內的指定材質座標。</span><span class="sxs-lookup"><span data-stu-id="c621b-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="c621b-111">此值會解析為零。</span><span class="sxs-lookup"><span data-stu-id="c621b-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="c621b-112">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="c621b-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="c621b-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="c621b-113">0x00010000L</span></span> | <span data-ttu-id="c621b-114">使用轉換成相機空間的頂點，作為此階段之材質轉換的輸入材質座標。</span><span class="sxs-lookup"><span data-stu-id="c621b-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="c621b-115">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="c621b-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="c621b-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="c621b-116">0x00020000L</span></span> | <span data-ttu-id="c621b-117">使用轉換成相機空間的頂點位置，作為此階段之材質轉換的輸入材質座標。</span><span class="sxs-lookup"><span data-stu-id="c621b-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="c621b-118">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="c621b-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="c621b-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="c621b-119">0x00030000L</span></span> | <span data-ttu-id="c621b-120">使用轉換成相機空間的反映向量，作為此階段之材質轉換的輸入材質座標。</span><span class="sxs-lookup"><span data-stu-id="c621b-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="c621b-121">反映向量是從輸入頂點位置和一般向量計算而來。</span><span class="sxs-lookup"><span data-stu-id="c621b-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="c621b-122">D3DTSS \_ TCI \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="c621b-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="c621b-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="c621b-123">0x00040000L</span></span> | <span data-ttu-id="c621b-124">使用指定的材質座標做為球體對應。</span><span class="sxs-lookup"><span data-stu-id="c621b-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="c621b-125">這些常數會由 D3DTSS \_ TEXCOORDINDEX 使用。</span><span class="sxs-lookup"><span data-stu-id="c621b-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="c621b-126">常數資訊</span><span class="sxs-lookup"><span data-stu-id="c621b-126">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="c621b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c621b-127">Header</span></span>                   | <span data-ttu-id="c621b-128">d3d9caps。h</span><span class="sxs-lookup"><span data-stu-id="c621b-128">d3d9caps.h</span></span> |
| <span data-ttu-id="c621b-129">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="c621b-129">Minimum operating system</span></span> | <span data-ttu-id="c621b-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c621b-130">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c621b-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="c621b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c621b-132">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="c621b-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




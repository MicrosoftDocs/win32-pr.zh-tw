---
title: '自動產生的材質座標 (Direct3D 9) '
description: 系統可以使用已轉換的相機空間位置或頂點中的法線作為材質座標，也可以計算用來定址三個元素向量的三個元素向量。
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8a6328df66296c0948c53be68109a9f5afbbb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997070"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a><span data-ttu-id="97044-103">自動產生的材質座標 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="97044-103">Auto-generated texture coordinates (Direct3D 9)</span></span>

<span data-ttu-id="97044-104">系統可以使用已轉換的相機空間位置或頂點中的法線作為材質座標，也可以計算用來定址三個元素向量的三個元素向量。</span><span class="sxs-lookup"><span data-stu-id="97044-104">The system can use the transformed camera-space position or the normal from a vertex as texture coordinates, or it can compute the three element vectors used to address a cubic environment map.</span></span> <span data-ttu-id="97044-105">如同您在頂點中明確指定的材質座標，您可以使用自動產生的材質座標作為材質座標轉換的輸入。</span><span class="sxs-lookup"><span data-stu-id="97044-105">Like texture coordinates that you explicitly specify in a vertex, you can use automatically generated texture coordinates as input for texture coordinate transformations.</span></span>

<span data-ttu-id="97044-106">自動產生的材質座標可以大幅減少幾何資料所需的頻寬，方法是消除頂點格式的明確材質座標需求。</span><span class="sxs-lookup"><span data-stu-id="97044-106">Automatically generated texture coordinates can significantly reduce the bandwidth required for geometry data by eliminating the need for explicit texture coordinates in the vertex format.</span></span> <span data-ttu-id="97044-107">在許多情況下，系統產生的材質座標可以搭配轉換使用，以產生特殊效果。</span><span class="sxs-lookup"><span data-stu-id="97044-107">In many cases, the texture coordinates that the system generates can be used with transformations to produce special effects.</span></span> <span data-ttu-id="97044-108">當然，這是一個特殊用途的功能，而且您會在許多情況下使用明確的材質座標。</span><span class="sxs-lookup"><span data-stu-id="97044-108">Of course, this is a special-purpose feature, and you will use explicit texture coordinates for many occasions.</span></span>

## <a name="configuring-automatically-generated-texture-coordinates"></a><span data-ttu-id="97044-109">設定自動產生的材質座標</span><span class="sxs-lookup"><span data-stu-id="97044-109">Configuring Automatically Generated Texture Coordinates</span></span>

<span data-ttu-id="97044-110">在 c + + 中， \_ [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) 列舉型別中的 D3DTSS TEXCOORDINDEX 材質階段狀態 (，) 控制系統產生材質座標的方式。</span><span class="sxs-lookup"><span data-stu-id="97044-110">In C++, the D3DTSS\_TEXCOORDINDEX texture-stage state (from the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type) controls how the system generates texture coordinates.</span></span>

<span data-ttu-id="97044-111">一般來說，此狀態會指示系統使用以頂點格式編碼的一組特定紋理座標。</span><span class="sxs-lookup"><span data-stu-id="97044-111">Normally, this state instructs the system to use a particular set of texture coordinates encoded in the vertex format.</span></span> <span data-ttu-id="97044-112">當您 \_ 將 D3DTSS TCI \_ CAMERASPACENORMAL、D3DTSS \_ TCI \_ CAMERASPACEPOSITION 或 D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR 旗標包含在指派給此狀態的值中時，系統行為會相當不同。</span><span class="sxs-lookup"><span data-stu-id="97044-112">When you include the D3DTSS\_TCI\_CAMERASPACENORMAL, D3DTSS\_TCI\_CAMERASPACEPOSITION, or D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR flags in the value that you assign to this state, the system behavior is quite different.</span></span> <span data-ttu-id="97044-113">如果有任何這些旗標存在，紋理階段會忽略頂點格式內的材質座標，以配合系統所產生的座標。</span><span class="sxs-lookup"><span data-stu-id="97044-113">If any of these flags are present, the texture stage ignores the texture coordinates within the vertex format in favor of coordinates that the system generates.</span></span> <span data-ttu-id="97044-114">下列清單會顯示每個旗標的意義。</span><span class="sxs-lookup"><span data-stu-id="97044-114">The meanings for each flag are shown in the following list.</span></span>

-   <span data-ttu-id="97044-115">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="97044-115">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>

    <span data-ttu-id="97044-116">使用轉換成相機空間的頂點，作為輸入材質座標。</span><span class="sxs-lookup"><span data-stu-id="97044-116">Use the vertex normal, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="97044-117">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="97044-117">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>

    <span data-ttu-id="97044-118">使用頂點位置（轉換成相機空間）做為輸入材質座標。</span><span class="sxs-lookup"><span data-stu-id="97044-118">Use the vertex position, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="97044-119">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="97044-119">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span>

    <span data-ttu-id="97044-120">使用轉換成相機空間的反映向量做為輸入材質座標。</span><span class="sxs-lookup"><span data-stu-id="97044-120">Use the reflection vector, transformed to camera space, as input texture coordinates.</span></span> <span data-ttu-id="97044-121">反映向量是從輸入頂點位置和一般向量計算而來。</span><span class="sxs-lookup"><span data-stu-id="97044-121">The reflection vector is computed from the input vertex position and normal vector.</span></span>

<span data-ttu-id="97044-122">材質座標索引旗標是互斥的。</span><span class="sxs-lookup"><span data-stu-id="97044-122">The texture coordinate index flags are mutually exclusive.</span></span> <span data-ttu-id="97044-123">這個範例會使用：</span><span class="sxs-lookup"><span data-stu-id="97044-123">This example uses:</span></span>

-   <span data-ttu-id="97044-124">[相機空間] (的頂點位置) 為此材質階段的輸入材質座標</span><span class="sxs-lookup"><span data-stu-id="97044-124">The vertex position (in camera-space) as the input texture coordinates for this texture stage</span></span>
-   <span data-ttu-id="97044-125">D3DRENDERSTATE WRAP1 轉譯狀態中設定的 wrap 模式 \_</span><span class="sxs-lookup"><span data-stu-id="97044-125">The wrap mode set in the D3DRENDERSTATE\_WRAP1 render state</span></span>


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



<span data-ttu-id="97044-126">自動產生的材質座標最適合作為紋理座標轉換的輸入值，或讓應用程式不需要計算三個元素的三個元素向量來進行三個元素的對應。</span><span class="sxs-lookup"><span data-stu-id="97044-126">Automatically generated texture coordinates are most useful as input values for a texture coordinate transformation, or to eliminate the need for your application to compute three-element vectors for cubic-environment maps.</span></span>

<span data-ttu-id="97044-127">球體對應會在模型時間使用預先計算 () 材質圖，其中包含由 chrome 球體反映的整個環境。</span><span class="sxs-lookup"><span data-stu-id="97044-127">Sphere-mapping uses a precomputed (at model time) texture map that contains the entire environment as reflected by a chrome sphere.</span></span> <span data-ttu-id="97044-128">Direct3D 具有使用轉譯狀態 D3DTSS TCI CAMERASPACENORMAL 的材質座標產生功能，此功能 \_ \_ 會採用相機空間中頂點的標準，並透過材質轉換來產生材質座標。</span><span class="sxs-lookup"><span data-stu-id="97044-128">Direct3D has a texture-coordinate generation feature using render state D3DTSS\_TCI\_CAMERASPACENORMAL, which takes the normal of the vertex in camera space and puts it through a texture transform to generate texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97044-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="97044-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97044-130">材質座標處理</span><span class="sxs-lookup"><span data-stu-id="97044-130">Texture Coordinate Processing</span></span>](texture-coordinate-processing.md)
</dt> <dt>

[<span data-ttu-id="97044-131"> (Direct3D 9) 的材質座標轉換 </span><span class="sxs-lookup"><span data-stu-id="97044-131">Texture Coordinate Transformations (Direct3D 9)</span></span>](texture-coordinate-transformations.md)
</dt> <dt>

[<span data-ttu-id="97044-132"> (Direct3D 9) 的三次環境對應 </span><span class="sxs-lookup"><span data-stu-id="97044-132">Cubic Environment Mapping (Direct3D 9)</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 

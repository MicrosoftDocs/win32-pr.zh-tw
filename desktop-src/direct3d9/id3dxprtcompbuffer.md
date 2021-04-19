---
description: ID3DXPRTCompBuffer 介面會儲存 ID3DXPRTBuffer 緩衝區的壓縮版本，以搭配 (PCA) 的主體元件分析使用。
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: 'ID3DXPRTCompBuffer 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 323ed6f2bbe9ce4caf495a00330c1b1e0e83e158
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985726"
---
# <a name="id3dxprtcompbuffer-interface"></a><span data-ttu-id="89192-103">ID3DXPRTCompBuffer 介面</span><span class="sxs-lookup"><span data-stu-id="89192-103">ID3DXPRTCompBuffer interface</span></span>

<span data-ttu-id="89192-104">**ID3DXPRTCompBuffer** 介面會儲存 [**ID3DXPRTBuffer**](id3dxprtbuffer.md)緩衝區的壓縮版本，以搭配 (PCA) 的主體元件分析使用。</span><span class="sxs-lookup"><span data-stu-id="89192-104">The **ID3DXPRTCompBuffer** interface stores a compressed version of a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer, for use with principal component analysis (PCA).</span></span>

## <a name="members"></a><span data-ttu-id="89192-105">成員</span><span class="sxs-lookup"><span data-stu-id="89192-105">Members</span></span>

<span data-ttu-id="89192-106">**ID3DXPRTCompBuffer** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="89192-106">The **ID3DXPRTCompBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="89192-107">**ID3DXPRTCompBuffer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="89192-107">**ID3DXPRTCompBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="89192-108">方法</span><span class="sxs-lookup"><span data-stu-id="89192-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="89192-109">方法</span><span class="sxs-lookup"><span data-stu-id="89192-109">Methods</span></span>

<span data-ttu-id="89192-110">**ID3DXPRTCompBuffer** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="89192-110">The **ID3DXPRTCompBuffer** interface has these methods.</span></span>



| <span data-ttu-id="89192-111">方法</span><span class="sxs-lookup"><span data-stu-id="89192-111">Method</span></span>                                                             | <span data-ttu-id="89192-112">描述</span><span class="sxs-lookup"><span data-stu-id="89192-112">Description</span></span>                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89192-113">**ExtractBasis**</span><span class="sxs-lookup"><span data-stu-id="89192-113">**ExtractBasis**</span></span>](id3dxprtcompbuffer--extractbasis.md)           | <span data-ttu-id="89192-114">從 **ID3DXPRTCompBuffer** 壓縮的資料緩衝區中，針對指定的叢集，將 mean 和主體元件分析 (PCA) 基礎向量。</span><span class="sxs-lookup"><span data-stu-id="89192-114">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                       |
| [<span data-ttu-id="89192-115">**ExtractClusterIDs**</span><span class="sxs-lookup"><span data-stu-id="89192-115">**ExtractClusterIDs**</span></span>](id3dxprtcompbuffer--extractclusterids.md) | <span data-ttu-id="89192-116">從 **ID3DXPRTCompBuffer** 壓縮的資料緩衝區解壓縮每個範例的叢集識別碼。</span><span class="sxs-lookup"><span data-stu-id="89192-116">Extracts the per-sample cluster IDs from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="89192-117">**ExtractPCA**</span><span class="sxs-lookup"><span data-stu-id="89192-117">**ExtractPCA**</span></span>](id3dxprtcompbuffer--extractpca.md)               | <span data-ttu-id="89192-118">從 **ID3DXPRTCompBuffer** 壓縮的資料緩衝區，將每個樣本的主體元件分析 (PCA) 投影係數。</span><span class="sxs-lookup"><span data-stu-id="89192-118">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                               |
| [<span data-ttu-id="89192-119">**ExtractTexture**</span><span class="sxs-lookup"><span data-stu-id="89192-119">**ExtractTexture**</span></span>](id3dxprtcompbuffer--extracttexture.md)       | <span data-ttu-id="89192-120">從 **ID3DXPRTCompBuffer** 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 物件。</span><span class="sxs-lookup"><span data-stu-id="89192-120">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="89192-121">**ExtractToMesh**</span><span class="sxs-lookup"><span data-stu-id="89192-121">**ExtractToMesh**</span></span>](id3dxprtcompbuffer--extracttomesh.md)         | <span data-ttu-id="89192-122">從 **ID3DXPRTCompBuffer** 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 [**ID3DXMesh**](id3dxmesh.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="89192-122">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                 |
| [<span data-ttu-id="89192-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="89192-123">**GetHeight**</span></span>](id3dxprtcompbuffer--getheight.md)                 | <span data-ttu-id="89192-124">抓取紋理的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="89192-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="89192-125">**GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="89192-125">**GetNumChannels**</span></span>](id3dxprtcompbuffer--getnumchannels.md)       | <span data-ttu-id="89192-126">抓取記憶體中用來儲存範例的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="89192-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="89192-127">**GetNumClusters**</span><span class="sxs-lookup"><span data-stu-id="89192-127">**GetNumClusters**</span></span>](id3dxprtcompbuffer--getnumclusters.md)       | <span data-ttu-id="89192-128">抓取要用於壓縮的群集數目。</span><span class="sxs-lookup"><span data-stu-id="89192-128">Retrieves the number of clusters to use for compression.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="89192-129">**GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="89192-129">**GetNumCoeffs**</span></span>](id3dxprtcompbuffer--getnumcoeffs.md)           | <span data-ttu-id="89192-130">抓取記憶體中用來儲存範例的每個顏色通道的純量數目。</span><span class="sxs-lookup"><span data-stu-id="89192-130">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="89192-131">**GetNumPCA**</span><span class="sxs-lookup"><span data-stu-id="89192-131">**GetNumPCA**</span></span>](id3dxprtcompbuffer--getnumpca.md)                 | <span data-ttu-id="89192-132">抓取每個叢集中要使用的主體元件分析 (PCA) 基礎向量的數目。</span><span class="sxs-lookup"><span data-stu-id="89192-132">Retrieves the number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="89192-133">**GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="89192-133">**GetNumSamples**</span></span>](id3dxprtcompbuffer--getnumsamples.md)         | <span data-ttu-id="89192-134">抓取取樣 (或材質) 的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="89192-134">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="89192-135">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="89192-135">**GetWidth**</span></span>](id3dxprtcompbuffer--getwidth.md)                   | <span data-ttu-id="89192-136">抓取紋理的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="89192-136">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="89192-137">**IsTexture**</span><span class="sxs-lookup"><span data-stu-id="89192-137">**IsTexture**</span></span>](id3dxprtcompbuffer--istexture.md)                 | <span data-ttu-id="89192-138">指出緩衝區是否包含材質。</span><span class="sxs-lookup"><span data-stu-id="89192-138">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="89192-139">**NormalizeData**</span><span class="sxs-lookup"><span data-stu-id="89192-139">**NormalizeData**</span></span>](id3dxprtcompbuffer--normalizedata.md)         | <span data-ttu-id="89192-140">將所有主體元件分析正規化 (PCA) 權數，使其介於-1 到1之間。</span><span class="sxs-lookup"><span data-stu-id="89192-140">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="89192-141">基礎向量會經過修改，以反映此正規化。</span><span class="sxs-lookup"><span data-stu-id="89192-141">Basis vectors are modified to reflect this normalization.</span></span><br/>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="89192-142">備註</span><span class="sxs-lookup"><span data-stu-id="89192-142">Remarks</span></span>

<span data-ttu-id="89192-143">**ID3DXPRTCompBuffer** 介面是藉由呼叫 [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md)函數來取得。</span><span class="sxs-lookup"><span data-stu-id="89192-143">The **ID3DXPRTCompBuffer** interface is obtained by calling the [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) function.</span></span>

<span data-ttu-id="89192-144">LPD3DXPRTCOMPBUFFER 型別定義為 **ID3DXPRTCompBuffer** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="89192-144">The LPD3DXPRTCOMPBUFFER type is defined as a pointer to the **ID3DXPRTCompBuffer** interface.</span></span>


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="89192-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="89192-145">Requirements</span></span>



| <span data-ttu-id="89192-146">需求</span><span class="sxs-lookup"><span data-stu-id="89192-146">Requirement</span></span> | <span data-ttu-id="89192-147">值</span><span class="sxs-lookup"><span data-stu-id="89192-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89192-148">標頭</span><span class="sxs-lookup"><span data-stu-id="89192-148">Header</span></span><br/>  | <dl> <span data-ttu-id="89192-149"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="89192-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="89192-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="89192-150">Library</span></span><br/> | <dl> <span data-ttu-id="89192-151"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="89192-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="89192-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89192-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89192-153">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="89192-153">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="89192-154">**D3DXCreatePRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="89192-154">**D3DXCreatePRTCompBuffer**</span></span>](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="89192-155">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="89192-155">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 

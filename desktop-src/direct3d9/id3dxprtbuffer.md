---
description: ID3DXPRTBuffer 介面是用來儲存頂點和圖元資料的資料緩衝區，以搭配預先計算 radiance 傳輸 (PRT) 方法和函式使用。
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: 'ID3DXPRTBuffer 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: daadb5b0ad8155062e75ea4eca566a0afbf3631b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992753"
---
# <a name="id3dxprtbuffer-interface"></a><span data-ttu-id="11ff2-103">ID3DXPRTBuffer 介面</span><span class="sxs-lookup"><span data-stu-id="11ff2-103">ID3DXPRTBuffer interface</span></span>

<span data-ttu-id="11ff2-104">ID3DXPRTBuffer 介面是用來儲存頂點和圖元資料的資料緩衝區，以搭配預先計算 radiance 傳輸 (PRT) 方法和函式使用。</span><span class="sxs-lookup"><span data-stu-id="11ff2-104">The ID3DXPRTBuffer interface is used as a data buffer to store vertex and pixel data for use with precomputed radiance transfer (PRT) methods and functions.</span></span>

## <a name="members"></a><span data-ttu-id="11ff2-105">成員</span><span class="sxs-lookup"><span data-stu-id="11ff2-105">Members</span></span>

<span data-ttu-id="11ff2-106">**ID3DXPRTBuffer** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="11ff2-106">The **ID3DXPRTBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="11ff2-107">**ID3DXPRTBuffer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="11ff2-107">**ID3DXPRTBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="11ff2-108">方法</span><span class="sxs-lookup"><span data-stu-id="11ff2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="11ff2-109">方法</span><span class="sxs-lookup"><span data-stu-id="11ff2-109">Methods</span></span>

<span data-ttu-id="11ff2-110">**ID3DXPRTBuffer** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="11ff2-110">The **ID3DXPRTBuffer** interface has these methods.</span></span>



| <span data-ttu-id="11ff2-111">方法</span><span class="sxs-lookup"><span data-stu-id="11ff2-111">Method</span></span>                                                   | <span data-ttu-id="11ff2-112">描述</span><span class="sxs-lookup"><span data-stu-id="11ff2-112">Description</span></span>                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11ff2-113">**AddBuffer**</span><span class="sxs-lookup"><span data-stu-id="11ff2-113">**AddBuffer**</span></span>](id3dxprtbuffer--addbuffer.md)           | <span data-ttu-id="11ff2-114">將另一個緩衝區新增至 **ID3DXPRTBuffer** ，並將結果儲存在 **ID3DXPRTBuffer** 中。</span><span class="sxs-lookup"><span data-stu-id="11ff2-114">Adds another buffer to the **ID3DXPRTBuffer** and stores the results in **ID3DXPRTBuffer**.</span></span><br/>                                                                                        |
| [<span data-ttu-id="11ff2-115">**AttachGH**</span><span class="sxs-lookup"><span data-stu-id="11ff2-115">**AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)             | <span data-ttu-id="11ff2-116">將 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 物件與 **ID3DXPRTBuffer** 物件建立關聯。</span><span class="sxs-lookup"><span data-stu-id="11ff2-116">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="11ff2-117">**EvalGH**</span><span class="sxs-lookup"><span data-stu-id="11ff2-117">**EvalGH**</span></span>](id3dxprtbuffer--evalgh.md)                 | <span data-ttu-id="11ff2-118">將儲存的材質裝訂邊資料套用至 **ID3DXPRTBuffer** 材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11ff2-118">Applies stored texture gutter data to an **ID3DXPRTBuffer** texture buffer.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="11ff2-119">**ExtractTexture**</span><span class="sxs-lookup"><span data-stu-id="11ff2-119">**ExtractTexture**</span></span>](id3dxprtbuffer--extracttexture.md) | <span data-ttu-id="11ff2-120">從緩衝區的色頻中，將係數資料從指定的係數範圍中解壓縮，並將資料加入至 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 物件。</span><span class="sxs-lookup"><span data-stu-id="11ff2-120">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="11ff2-121">**ExtractToMesh**</span><span class="sxs-lookup"><span data-stu-id="11ff2-121">**ExtractToMesh**</span></span>](id3dxprtbuffer--extracttomesh.md)   | <span data-ttu-id="11ff2-122">從單一通道緩衝區解壓縮係數資料，並將資料加入至 [**ID3DXMesh**](id3dxmesh.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="11ff2-122">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                                                              |
| [<span data-ttu-id="11ff2-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="11ff2-123">**GetHeight**</span></span>](id3dxprtbuffer--getheight.md)           | <span data-ttu-id="11ff2-124">抓取紋理的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="11ff2-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="11ff2-125">**GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="11ff2-125">**GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md) | <span data-ttu-id="11ff2-126">抓取記憶體中用來儲存範例的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="11ff2-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="11ff2-127">**GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="11ff2-127">**GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)     | <span data-ttu-id="11ff2-128">抓取記憶體中用來儲存範例的每個顏色通道的純量數目。</span><span class="sxs-lookup"><span data-stu-id="11ff2-128">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="11ff2-129">**GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="11ff2-129">**GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)   | <span data-ttu-id="11ff2-130">抓取取樣 (或材質) 的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="11ff2-130">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="11ff2-131">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="11ff2-131">**GetWidth**</span></span>](id3dxprtbuffer--getwidth.md)             | <span data-ttu-id="11ff2-132">抓取紋理的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="11ff2-132">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="11ff2-133">**IsTexture**</span><span class="sxs-lookup"><span data-stu-id="11ff2-133">**IsTexture**</span></span>](id3dxprtbuffer--istexture.md)           | <span data-ttu-id="11ff2-134">指出緩衝區是否包含材質。</span><span class="sxs-lookup"><span data-stu-id="11ff2-134">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="11ff2-135">**LockBuffer**</span><span class="sxs-lookup"><span data-stu-id="11ff2-135">**LockBuffer**</span></span>](id3dxprtbuffer--lockbuffer.md)         | <span data-ttu-id="11ff2-136">鎖定某個範圍的頂點或材質範例資料，並取得緩衝區記憶體中位置的指標。</span><span class="sxs-lookup"><span data-stu-id="11ff2-136">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span><br/>                                                                               |
| [<span data-ttu-id="11ff2-137">**ReleaseGH**</span><span class="sxs-lookup"><span data-stu-id="11ff2-137">**ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)           | <span data-ttu-id="11ff2-138">Unassociates 具有 **ID3DXPRTBuffer** 物件的附加 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)物件。</span><span class="sxs-lookup"><span data-stu-id="11ff2-138">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                   |
| [<span data-ttu-id="11ff2-139">**調整大小**</span><span class="sxs-lookup"><span data-stu-id="11ff2-139">**Resize**</span></span>](id3dxprtbuffer--resize.md)                 | <span data-ttu-id="11ff2-140">變更緩衝區中包含的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="11ff2-140">Changes the number of samples contained in the buffer.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="11ff2-141">**ScaleBuffer**</span><span class="sxs-lookup"><span data-stu-id="11ff2-141">**ScaleBuffer**</span></span>](id3dxprtbuffer--scalebuffer.md)       | <span data-ttu-id="11ff2-142">將緩衝區中的每個值乘以常數值。</span><span class="sxs-lookup"><span data-stu-id="11ff2-142">Multiplies every value in the buffer by a constant value.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="11ff2-143">**UnlockBuffer**</span><span class="sxs-lookup"><span data-stu-id="11ff2-143">**UnlockBuffer**</span></span>](id3dxprtbuffer--unlockbuffer.md)     | <span data-ttu-id="11ff2-144">結束 [**ID3DXPRTBuffer：： LockBuffer**](id3dxprtbuffer--lockbuffer.md)所傳回之 ppData 指標的存留期。</span><span class="sxs-lookup"><span data-stu-id="11ff2-144">Ends the lifespan of the ppData pointer returned by [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="11ff2-145">備註</span><span class="sxs-lookup"><span data-stu-id="11ff2-145">Remarks</span></span>

<span data-ttu-id="11ff2-146">**ID3DXPRTBuffer** 介面是藉由呼叫 [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)或 [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)函數來取得。</span><span class="sxs-lookup"><span data-stu-id="11ff2-146">The **ID3DXPRTBuffer** interface is obtained by calling the [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) functions.</span></span>

<span data-ttu-id="11ff2-147">LPD3DXPRTBUFFER 型別定義為 **ID3DXPRTBuffer** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="11ff2-147">The LPD3DXPRTBUFFER type is defined as a pointer to the **ID3DXPRTBuffer** interface.</span></span>


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="11ff2-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="11ff2-148">Requirements</span></span>



| <span data-ttu-id="11ff2-149">需求</span><span class="sxs-lookup"><span data-stu-id="11ff2-149">Requirement</span></span> | <span data-ttu-id="11ff2-150">值</span><span class="sxs-lookup"><span data-stu-id="11ff2-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11ff2-151">標頭</span><span class="sxs-lookup"><span data-stu-id="11ff2-151">Header</span></span><br/>  | <dl> <span data-ttu-id="11ff2-152"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="11ff2-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="11ff2-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="11ff2-153">Library</span></span><br/> | <dl> <span data-ttu-id="11ff2-154"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="11ff2-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="11ff2-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11ff2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ff2-156">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="11ff2-156">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="11ff2-157">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="11ff2-157">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="11ff2-158">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="11ff2-158">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> <dt>

[<span data-ttu-id="11ff2-159">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="11ff2-159">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 

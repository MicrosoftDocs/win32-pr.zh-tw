---
description: ID3DX10SkinInfo 可讓您優化、處理及手動設定網格中的骨骼與頂點之間的關聯性 (請參閱維琪百科) 上的框架動畫。
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: 'ID3DX10SkinInfo 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322948"
---
# <a name="id3dx10skininfo-interface"></a><span data-ttu-id="ad00f-103">ID3DX10SkinInfo 介面</span><span class="sxs-lookup"><span data-stu-id="ad00f-103">ID3DX10SkinInfo interface</span></span>

<span data-ttu-id="ad00f-104">ID3DX10SkinInfo 可讓您優化、處理及手動設定網格中的骨骼與頂點之間的關聯性 (請參閱 [維琪百科) 上的框架動畫](https://en.wikipedia.org/wiki/Skeletal_animation) 。</span><span class="sxs-lookup"><span data-stu-id="ad00f-104">ID3DX10SkinInfo allows you to optimize, process, and manually set the relationship between bones and vertices in your meshes (see [Skeletal Animation on Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span></span> <span data-ttu-id="ad00f-105">它最適合用來製作 DCC Apps 所匯出的. x 檔案 (例如 3DS Max 和 Maya) 更容易使用硬體，以及改善 skinned 網格在軟體轉譯模式中的呈現速度。</span><span class="sxs-lookup"><span data-stu-id="ad00f-105">It is most useful for making .x files exported by DCC Apps (such as 3DS Max and Maya) more hardware-friendly, and for improving the render speed of your skinned meshes in software render mode.</span></span>

## <a name="members"></a><span data-ttu-id="ad00f-106">成員</span><span class="sxs-lookup"><span data-stu-id="ad00f-106">Members</span></span>

<span data-ttu-id="ad00f-107">**ID3DX10SkinInfo** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="ad00f-107">The **ID3DX10SkinInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ad00f-108">**ID3DX10SkinInfo** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ad00f-108">**ID3DX10SkinInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="ad00f-109">方法</span><span class="sxs-lookup"><span data-stu-id="ad00f-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ad00f-110">方法</span><span class="sxs-lookup"><span data-stu-id="ad00f-110">Methods</span></span>

<span data-ttu-id="ad00f-111">**ID3DX10SkinInfo** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ad00f-111">The **ID3DX10SkinInfo** interface has these methods.</span></span>



| <span data-ttu-id="ad00f-112">方法</span><span class="sxs-lookup"><span data-stu-id="ad00f-112">Method</span></span>                                                                   | <span data-ttu-id="ad00f-113">描述</span><span class="sxs-lookup"><span data-stu-id="ad00f-113">Description</span></span>                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad00f-114">**AddBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="ad00f-114">**AddBoneInfluences**</span></span>](id3dx10skininfo-addboneinfluences.md)           | <span data-ttu-id="ad00f-115">啟用現有的骨骼來影響一組頂點，並定義骨骼對每個頂點的影響程度。</span><span class="sxs-lookup"><span data-stu-id="ad00f-115">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span><br/>     |
| [<span data-ttu-id="ad00f-116">**AddBones**</span><span class="sxs-lookup"><span data-stu-id="ad00f-116">**AddBones**</span></span>](id3dx10skininfo-addbones.md)                             | <span data-ttu-id="ad00f-117">配置更多骨骼的空間。</span><span class="sxs-lookup"><span data-stu-id="ad00f-117">Allocate space for more bones.</span></span><br/>                                                                                          |
| [<span data-ttu-id="ad00f-118">**AddVertices**</span><span class="sxs-lookup"><span data-stu-id="ad00f-118">**AddVertices**</span></span>](id3dx10skininfo-addvertices.md)                       | <span data-ttu-id="ad00f-119">配置其他頂點的空間。</span><span class="sxs-lookup"><span data-stu-id="ad00f-119">Allocate space for additional vertices.</span></span><br/>                                                                                 |
| [<span data-ttu-id="ad00f-120">**ClearBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="ad00f-120">**ClearBoneInfluences**</span></span>](id3dx10skininfo-clearboneinfluences.md)       | <span data-ttu-id="ad00f-121">清除其所影響之骨骼的頂點清單。</span><span class="sxs-lookup"><span data-stu-id="ad00f-121">Clear a bone's list of vertices that it influences.</span></span><br/>                                                                     |
| [<span data-ttu-id="ad00f-122">**精簡**</span><span class="sxs-lookup"><span data-stu-id="ad00f-122">**Compact**</span></span>](id3dx10skininfo-compact.md)                               | <span data-ttu-id="ad00f-123">限制可能影響頂點的骨骼數目，以及/或限制骨骼在頂點上可以有的影響數量。</span><span class="sxs-lookup"><span data-stu-id="ad00f-123">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span><br/> |
| [<span data-ttu-id="ad00f-124">**DoSoftwareSkinning**</span><span class="sxs-lookup"><span data-stu-id="ad00f-124">**DoSoftwareSkinning**</span></span>](id3dx10skininfo-dosoftwareskinning.md)         | <span data-ttu-id="ad00f-125">在頂點的陣列上進行軟體外觀。</span><span class="sxs-lookup"><span data-stu-id="ad00f-125">Do software skinning on an array of vertices.</span></span><br/>                                                                           |
| [<span data-ttu-id="ad00f-126">**FindBoneInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="ad00f-126">**FindBoneInfluenceIndex**</span></span>](id3dx10skininfo-findboneinfluenceindex.md) | <span data-ttu-id="ad00f-127">找出表示指定頂點在受影響頂點的指定清單中之位置的索引。</span><span class="sxs-lookup"><span data-stu-id="ad00f-127">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span><br/>                    |
| [<span data-ttu-id="ad00f-128">**GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="ad00f-128">**GetBoneInfluence**</span></span>](id3dx10skininfo-getboneinfluence.md)             | <span data-ttu-id="ad00f-129">取得指定之骨骼對指定頂點的影響量。</span><span class="sxs-lookup"><span data-stu-id="ad00f-129">Get the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |
| [<span data-ttu-id="ad00f-130">**GetBoneInfluenceCount**</span><span class="sxs-lookup"><span data-stu-id="ad00f-130">**GetBoneInfluenceCount**</span></span>](id3dx10skininfo-getboneinfluencecount.md)   | <span data-ttu-id="ad00f-131">取得指定之骨骼影響的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="ad00f-131">Get the number of vertices that a given bone influences.</span></span><br/>                                                                |
| [<span data-ttu-id="ad00f-132">**GetBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="ad00f-132">**GetBoneInfluences**</span></span>](id3dx10skininfo-getboneinfluences.md)           | <span data-ttu-id="ad00f-133">取得指定之骨骼影響的頂點清單，以及骨骼對每個頂點的影響數量清單。</span><span class="sxs-lookup"><span data-stu-id="ad00f-133">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span><br/> |
| [<span data-ttu-id="ad00f-134">**GetMaxBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="ad00f-134">**GetMaxBoneInfluences**</span></span>](id3dx10skininfo-getmaxboneinfluences.md)     | <span data-ttu-id="ad00f-135">取得骨骼可充分影響的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="ad00f-135">Get the number of vertices a bone can maximally influence.</span></span><br/>                                                              |
| [<span data-ttu-id="ad00f-136">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="ad00f-136">**GetNumBones**</span></span>](id3dx10skininfo-getnumbones.md)                       | <span data-ttu-id="ad00f-137">取得 ID3DX10SkinInfo 中的骨骼數目。</span><span class="sxs-lookup"><span data-stu-id="ad00f-137">Get the number of bones in ID3DX10SkinInfo.</span></span><br/>                                                                             |
| [<span data-ttu-id="ad00f-138">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="ad00f-138">**GetNumVertices**</span></span>](id3dx10skininfo-getnumvertices.md)                 | <span data-ttu-id="ad00f-139">取得 ID3DX10SkinInfo 中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="ad00f-139">Get the number of vertices in ID3DX10SkinInfo.</span></span><br/>                                                                          |
| [<span data-ttu-id="ad00f-140">**RemapBones**</span><span class="sxs-lookup"><span data-stu-id="ad00f-140">**RemapBones**</span></span>](id3dx10skininfo-remapbones.md)                         | <span data-ttu-id="ad00f-141">變更哪些骨骼會影響哪些頂點。</span><span class="sxs-lookup"><span data-stu-id="ad00f-141">Change which bones influence which vertices.</span></span><br/>                                                                            |
| [<span data-ttu-id="ad00f-142">**RemapVertices**</span><span class="sxs-lookup"><span data-stu-id="ad00f-142">**RemapVertices**</span></span>](id3dx10skininfo-remapvertices.md)                   | <span data-ttu-id="ad00f-143">變更哪些頂點受哪些骨骼影響。</span><span class="sxs-lookup"><span data-stu-id="ad00f-143">Change which vertices are influenced by which bones.</span></span><br/>                                                                    |
| [<span data-ttu-id="ad00f-144">**RemoveBone**</span><span class="sxs-lookup"><span data-stu-id="ad00f-144">**RemoveBone**</span></span>](id3dx10skininfo-removebone.md)                         | <span data-ttu-id="ad00f-145">移除骨骼。</span><span class="sxs-lookup"><span data-stu-id="ad00f-145">Remove a bone.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="ad00f-146">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="ad00f-146">**SetBoneInfluence**</span></span>](id3dx10skininfo-setboneinfluence.md)             | <span data-ttu-id="ad00f-147">設定指定之骨骼對指定頂點的影響量。</span><span class="sxs-lookup"><span data-stu-id="ad00f-147">Set the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="ad00f-148">備註</span><span class="sxs-lookup"><span data-stu-id="ad00f-148">Remarks</span></span>

<span data-ttu-id="ad00f-149">使用 [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md)、 **D3DX10CreateSkinInfoFromBlendedMesh** 或 **D3DX10CreateSkinInfoFVF** 建立 ID3DX10SkinInfo 介面。</span><span class="sxs-lookup"><span data-stu-id="ad00f-149">Create a ID3DX10SkinInfo interface with [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh**, or **D3DX10CreateSkinInfoFVF**.</span></span>

<span data-ttu-id="ad00f-150">LPD3DX10SKININFO 型別定義為 **ID3DX10SkinInfo** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ad00f-150">The LPD3DX10SKININFO type is defined as a pointer to the **ID3DX10SkinInfo** interface.</span></span>


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a><span data-ttu-id="ad00f-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad00f-151">Requirements</span></span>



| <span data-ttu-id="ad00f-152">需求</span><span class="sxs-lookup"><span data-stu-id="ad00f-152">Requirement</span></span> | <span data-ttu-id="ad00f-153">值</span><span class="sxs-lookup"><span data-stu-id="ad00f-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad00f-154">標頭</span><span class="sxs-lookup"><span data-stu-id="ad00f-154">Header</span></span><br/>  | <dl> <span data-ttu-id="ad00f-155"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad00f-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad00f-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="ad00f-156">Library</span></span><br/> | <dl> <span data-ttu-id="ad00f-157"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad00f-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad00f-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad00f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad00f-159">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="ad00f-159">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

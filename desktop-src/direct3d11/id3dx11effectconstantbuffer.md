---
title: 'ID3DX11EffectConstantBuffer 介面 (D3dx11effect .h) '
description: 常數緩衝區介面會存取常數緩衝區或紋理緩衝區。
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- ID3DX11EffectConstantBuffer 介面 Direct3D 11
- ID3DX11EffectConstantBuffer 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323079"
---
# <a name="id3dx11effectconstantbuffer-interface"></a><span data-ttu-id="518dd-105">ID3DX11EffectConstantBuffer 介面</span><span class="sxs-lookup"><span data-stu-id="518dd-105">ID3DX11EffectConstantBuffer interface</span></span>

<span data-ttu-id="518dd-106">常數緩衝區介面會存取常數緩衝區或紋理緩衝區。</span><span class="sxs-lookup"><span data-stu-id="518dd-106">A constant-buffer interface accesses constant buffers or texture buffers.</span></span>

## <a name="members"></a><span data-ttu-id="518dd-107">成員</span><span class="sxs-lookup"><span data-stu-id="518dd-107">Members</span></span>

<span data-ttu-id="518dd-108">**ID3DX11EffectConstantBuffer** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="518dd-108">The **ID3DX11EffectConstantBuffer** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="518dd-109">**ID3DX11EffectConstantBuffer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="518dd-109">**ID3DX11EffectConstantBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="518dd-110">方法</span><span class="sxs-lookup"><span data-stu-id="518dd-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="518dd-111">方法</span><span class="sxs-lookup"><span data-stu-id="518dd-111">Methods</span></span>

<span data-ttu-id="518dd-112">**ID3DX11EffectConstantBuffer** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="518dd-112">The **ID3DX11EffectConstantBuffer** interface has these methods.</span></span>



| <span data-ttu-id="518dd-113">方法</span><span class="sxs-lookup"><span data-stu-id="518dd-113">Method</span></span>                                                                             | <span data-ttu-id="518dd-114">描述</span><span class="sxs-lookup"><span data-stu-id="518dd-114">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="518dd-115">**GetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="518dd-115">**GetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-getconstantbuffer.md)         | <span data-ttu-id="518dd-116">取得常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="518dd-116">Get a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="518dd-117">**GetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="518dd-117">**GetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-gettexturebuffer.md)           | <span data-ttu-id="518dd-118">取得材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="518dd-118">Get a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="518dd-119">**SetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="518dd-119">**SetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-setconstantbuffer.md)         | <span data-ttu-id="518dd-120">設定常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="518dd-120">Set a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="518dd-121">**SetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="518dd-121">**SetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-settexturebuffer.md)           | <span data-ttu-id="518dd-122">設定材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="518dd-122">Set a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="518dd-123">**UndoSetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="518dd-123">**UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | <span data-ttu-id="518dd-124">還原先前設定的常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="518dd-124">Reverts a previously set constant buffer.</span></span><br/> |
| [<span data-ttu-id="518dd-125">**UndoSetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="518dd-125">**UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | <span data-ttu-id="518dd-126">還原先前設定的材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="518dd-126">Reverts a previously set texture buffer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="518dd-127">備註</span><span class="sxs-lookup"><span data-stu-id="518dd-127">Remarks</span></span>

<span data-ttu-id="518dd-128">使用常數緩衝區來儲存許多效果常數;根據更新頻率將常數分組到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="518dd-128">Use constant buffers to store many effect constants; grouping constants into buffers based on their frequency of update.</span></span> <span data-ttu-id="518dd-129">這可讓您將狀態變更的數目降至最低，以及進行最少的 API 呼叫以變更狀態。</span><span class="sxs-lookup"><span data-stu-id="518dd-129">This allows you to minimize the number of state changes as well as make the fewest API calls to change state.</span></span> <span data-ttu-id="518dd-130">這兩個因素都可提升效能。</span><span class="sxs-lookup"><span data-stu-id="518dd-130">Both of these factors lead to better performance.</span></span>

> [!Note]  
> <span data-ttu-id="518dd-131">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="518dd-131">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="518dd-132">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="518dd-132">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="518dd-133">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="518dd-133">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="518dd-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="518dd-134">Requirements</span></span>



| <span data-ttu-id="518dd-135">需求</span><span class="sxs-lookup"><span data-stu-id="518dd-135">Requirement</span></span> | <span data-ttu-id="518dd-136">值</span><span class="sxs-lookup"><span data-stu-id="518dd-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="518dd-137">標頭</span><span class="sxs-lookup"><span data-stu-id="518dd-137">Header</span></span><br/>  | <dl> <span data-ttu-id="518dd-138"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="518dd-138"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="518dd-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="518dd-139">Library</span></span><br/> | <dl> <span data-ttu-id="518dd-140"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="518dd-140"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="518dd-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="518dd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="518dd-142">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="518dd-142">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="518dd-143">效果11介面</span><span class="sxs-lookup"><span data-stu-id="518dd-143">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="518dd-144">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="518dd-144">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 






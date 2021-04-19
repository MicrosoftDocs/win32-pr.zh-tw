---
title: D3D12 的 Helper 函式
description: 這些 helper 函式特別有助於處理子資源，而且會在 d3dx12 中宣告。
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Helper 函式
- d3dx12。h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cacaaf5ad2a8204cc35b8a89f7c3c00e756116
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969467"
---
# <a name="helper-functions-for-d3d12"></a><span data-ttu-id="17b51-105">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="17b51-105">Helper Functions for D3D12</span></span>

<span data-ttu-id="17b51-106">這些 helper 函式特別有助於處理子資源，而且會在 **d3dx12** 中宣告。</span><span class="sxs-lookup"><span data-stu-id="17b51-106">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="17b51-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="17b51-107">In this section</span></span>



| <span data-ttu-id="17b51-108">主題</span><span class="sxs-lookup"><span data-stu-id="17b51-108">Topic</span></span>                                                                                             | <span data-ttu-id="17b51-109">描述</span><span class="sxs-lookup"><span data-stu-id="17b51-109">Description</span></span>                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17b51-110">**CommandListCast**</span><span class="sxs-lookup"><span data-stu-id="17b51-110">**CommandListCast**</span></span>](cd3dx12-shader-bytecode.md)<br/>                                     | <span data-ttu-id="17b51-111">這個函式範本會將任何命令清單的常數指標轉換成 ID3D12CommandList 的 const 指標。</span><span class="sxs-lookup"><span data-stu-id="17b51-111">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="17b51-112">**D3D12CalcSubresource**</span><span class="sxs-lookup"><span data-stu-id="17b51-112">**D3D12CalcSubresource**</span></span>](d3d12calcsubresource.md)<br/>                                   | <span data-ttu-id="17b51-113">計算材質的 subresource 索引。</span><span class="sxs-lookup"><span data-stu-id="17b51-113">Calculates a subresource index for a texture.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="17b51-114">**D3D12DecomposeSubresource**</span><span class="sxs-lookup"><span data-stu-id="17b51-114">**D3D12DecomposeSubresource**</span></span>](d3d12decomposesubresource.md)<br/>                         | <span data-ttu-id="17b51-115">輸出對應至指定之 subresource 索引的 mip 配量、陣列配量和平面配量。</span><span class="sxs-lookup"><span data-stu-id="17b51-115">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span> <br/>                                                                                                                                        |
| [<span data-ttu-id="17b51-116">**D3D12GetFormatPlaneCount**</span><span class="sxs-lookup"><span data-stu-id="17b51-116">**D3D12GetFormatPlaneCount**</span></span>](d3d12getformatplanecount.md)<br/>                           | <span data-ttu-id="17b51-117">針對指定的虛擬配接器 (**ID3D12Device**) ，取得指定之 DXGI 格式的平面數目。</span><span class="sxs-lookup"><span data-stu-id="17b51-117">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="17b51-118">**D3D12IsLayoutOpaque**</span><span class="sxs-lookup"><span data-stu-id="17b51-118">**D3D12IsLayoutOpaque**</span></span>](d3d12islayoutopaque.md)<br/>                                     | <span data-ttu-id="17b51-119">指出版面配置是否為不透明。</span><span class="sxs-lookup"><span data-stu-id="17b51-119">Indicates whether the layout is opaque.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="17b51-120">**D3DX12GetBaseSubobjectType**</span><span class="sxs-lookup"><span data-stu-id="17b51-120">**D3DX12GetBaseSubobjectType**</span></span>](d3dx12getbasesubobjecttype.md)<br/>                       | <span data-ttu-id="17b51-121">傳回子物件類型，這個物件對應至傳入之子物件類型的基類。</span><span class="sxs-lookup"><span data-stu-id="17b51-121">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="17b51-122">**D3DX12ParsePipelineStateStream**</span><span class="sxs-lookup"><span data-stu-id="17b51-122">**D3DX12ParsePipelineStateStream**</span></span>](d3dx12parsepipelinestream.md)<br/>                    | <span data-ttu-id="17b51-123">剖析管線狀態資料流程描述，針對每個已剖析的子物件實例呼叫使用者定義的回呼。</span><span class="sxs-lookup"><span data-stu-id="17b51-123">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="17b51-124">**D3DX12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="17b51-124">**D3DX12SerializeVersionedRootSignature**</span></span>](d3dx12serializeversionedrootsignature.md)<br/> | <span data-ttu-id="17b51-125">有助於啟用根簽章1.1 功能（如果有的話），而且不需要維護兩個程式碼路徑來建立根簽章。</span><span class="sxs-lookup"><span data-stu-id="17b51-125">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="17b51-126">此 helper 方法會在版本1.1 不受支援時，重建版本1.0 的根簽章。</span><span class="sxs-lookup"><span data-stu-id="17b51-126">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span><br/> |
| [<span data-ttu-id="17b51-127">**GetRequiredIntermediateSize**</span><span class="sxs-lookup"><span data-stu-id="17b51-127">**GetRequiredIntermediateSize**</span></span>](getrequiredintermediatesize.md)<br/>                     | <span data-ttu-id="17b51-128">傳回要用於資料上傳的緩衝區所需大小。</span><span class="sxs-lookup"><span data-stu-id="17b51-128">Returns the required size of a buffer to be used for data upload.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="17b51-129">**Memcpysubresource**</span><span class="sxs-lookup"><span data-stu-id="17b51-129">**Memcpysubresource**</span></span>](memcpysubresource.md)<br/>                                         | <span data-ttu-id="17b51-130">逐列複製 subresource 資料列。</span><span class="sxs-lookup"><span data-stu-id="17b51-130">Copies a subresource row by row.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="17b51-131">**Updatesubresources**</span><span class="sxs-lookup"><span data-stu-id="17b51-131">**Updatesubresources**</span></span>](updatesubresources1.md)<br/>                                      | <span data-ttu-id="17b51-132">更新子資源，所有 subresource 陣列都應該填入，通常是藉由呼叫 [**ID3D12Device：： GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)。</span><span class="sxs-lookup"><span data-stu-id="17b51-132">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span> <br/>                                                                  |
| [<span data-ttu-id="17b51-133">**Updatesubresources (堆積配置)**</span><span class="sxs-lookup"><span data-stu-id="17b51-133">**Updatesubresources (heap-allocating)**</span></span>](updatesubresources2.md)<br/>                    | <span data-ttu-id="17b51-134">以堆積配置的執行更新子資源。</span><span class="sxs-lookup"><span data-stu-id="17b51-134">Updates subresources with a heap-allocating implementation.</span></span> <br/>                                                                                                                                                                                    |
| [<span data-ttu-id="17b51-135">**Updatesubresources (堆疊配置)**</span><span class="sxs-lookup"><span data-stu-id="17b51-135">**Updatesubresources (stack-allocating)**</span></span>](updatesubresources3.md)<br/>                   | <span data-ttu-id="17b51-136">使用堆疊配置執行更新子資源。</span><span class="sxs-lookup"><span data-stu-id="17b51-136">Updates subresources with a stack-allocating implementation.</span></span> <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="17b51-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="17b51-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17b51-138">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="17b51-138">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="17b51-139">D3D12 的 Helper 結構和函式</span><span class="sxs-lookup"><span data-stu-id="17b51-139">Helper Structures and Functions for D3D12</span></span>](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 






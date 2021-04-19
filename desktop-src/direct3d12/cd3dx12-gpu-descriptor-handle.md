---
title: 'CD3DX12_GPU_DESCRIPTOR_HANDLE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ GPU \_ 描述項 \_ 控制碼結構。
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- CD3DX12_GPU_DESCRIPTOR_HANDLE 結構
topic_type:
- apiref
api_name:
- CD3DX12_GPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429d41d401b7d3e928bc4ab76850b36ae41b1e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982865"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a><span data-ttu-id="7e3ac-104">CD3DX12 \_ GPU \_ 描述項 \_ 控制碼結構</span><span class="sxs-lookup"><span data-stu-id="7e3ac-104">CD3DX12\_GPU\_DESCRIPTOR\_HANDLE structure</span></span>

<span data-ttu-id="7e3ac-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ GPU 描述項 \_ \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) 結構。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-105">A helper structure to enable easy initialization of a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e3ac-106">語法</span><span class="sxs-lookup"><span data-stu-id="7e3ac-106">Syntax</span></span>


```C++
struct CD3DX12_GPU_DESCRIPTOR_HANDLE  : public D3D12_GPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            inline operator==( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  bool                            inline operator!=( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_GPU_DESCRIPTOR_HANDLE & operator=(const D3D12_GPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a><span data-ttu-id="7e3ac-107">成員</span><span class="sxs-lookup"><span data-stu-id="7e3ac-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e3ac-108">**CD3DX12 \_ GPU \_ 描述項 \_ 控制碼 ()**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-108">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE()**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-109">建立 CD3DX12 \_ GPU \_ 描述項控制碼的新、未初始化的實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-109">Creates a new, uninitialized, instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-110">**明確 CD3DX12 的 \_ gpu \_ 描述項 \_ 控制碼 (const D3D12 \_ gpu 描述項 \_ \_ 控制碼 &o)**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-110">**explicit CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-111">建立 CD3DX12 \_ GPU 描述元控制碼的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ gpu 描述元 \_ \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-111">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initialized with the contents of another [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-112">**CD3DX12 \_ GPU \_ 描述項 \_ 控制碼 (CD3DX12 \_ 預設)**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-112">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-113">建立 CD3DX12 \_ GPU 描述元控制碼的新實例 \_ ，以 \_ 預設參數初始化， (將指標設定為零) 。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-113">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initialized with default parameters (sets the pointer to zero).</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-114">**CD3DX12 \_ gpu \_ 描述項 \_ 控制碼 (const D3D12 \_ gpu 描述項 \_ \_ 控制碼，&其他，INT offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-114">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-115">建立 CD3DX12 \_ GPU 描述元控制碼的新實例 \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="7e3ac-115">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="7e3ac-116">D3D12 \_ GPU \_ 描述項 \_ 控制碼 &其他</span><span class="sxs-lookup"><span data-stu-id="7e3ac-116">D3D12\_GPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="7e3ac-117">INT offsetScaledByIncrementSize：位移的遞增數目。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-117">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-118">**CD3DX12 \_ gpu \_ 描述項 \_ 控制碼 (const D3D12 \_ gpu \_ 描述項 \_ 控制碼，&其他，INT offsetInDescriptors，UINT descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-118">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-119">建立 CD3DX12 \_ GPU 描述元控制碼的新實例 \_ ，並 \_ 初始化下列參數：</span><span class="sxs-lookup"><span data-stu-id="7e3ac-119">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="7e3ac-120">D3D12 \_ GPU \_ 描述項 \_ 控制碼 &其他</span><span class="sxs-lookup"><span data-stu-id="7e3ac-120">D3D12\_GPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="7e3ac-121">INT offsetInDescriptors：要遞增的描述項數目。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-121">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="7e3ac-122">UINT descriptorIncrementSize：每個描述項的遞增量（包括填補）。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-122">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-123">**Offset (INT offsetInDescriptors，UINT descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-123">**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-124">根據指定的描述項數目和每個描述項的遞增量，設定位移。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-124">Sets the offset based on the specified number of descriptors and how much to increment for each descriptor.</span></span> <span data-ttu-id="7e3ac-125">使用下列參數：</span><span class="sxs-lookup"><span data-stu-id="7e3ac-125">Uses the following parameters:</span></span>

<span data-ttu-id="7e3ac-126">INT offsetInDescriptors：要遞增的描述項數目。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-126">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="7e3ac-127">UINT descriptorIncrementSize：每個描述項的遞增量（包括填補）。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-127">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-128">**Offset (INT offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-128">**Offset(INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-129">根據指定的增量數目來設定位移。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-129">Sets the offset based on the specified number of increments.</span></span> <span data-ttu-id="7e3ac-130">使用下列參數：</span><span class="sxs-lookup"><span data-stu-id="7e3ac-130">Uses the following parameters:</span></span>

<span data-ttu-id="7e3ac-131">INT offsetScaledByIncrementSize：位移的遞增數目。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-131">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-132">**內嵌運算子 = = ( \_ 在 \_ const D3D12 \_ GPU \_ 描述項 \_ 控制碼中& 其他) const**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-132">**inline operator==( \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-133">測試目前的 CD3DX12 \_ gpu \_ 描述項 \_ 控制碼和指定的 D3D12 gpu 描述項控制碼， \_ \_ \_ 或 CD3DX12 \_ gpu \_ 描述 \_ 項控制碼是否相等。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-133">Tests for equality between the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-134">**內嵌運算子！ = ( \_ \_ 常數 D3D12 \_ GPU 描述 \_ 項 \_ 控制碼& 其他) const**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-134">**inline operator!=( \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-135">測試目前 CD3DX12 \_ gpu \_ 描述項 \_ 控制碼和指定的 D3D12 gpu 描述項控制碼之間是否不相等， \_ \_ \_ 或 CD3DX12 \_ gpu \_ 描述項 \_ 控制碼。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-135">Tests for inequality between the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-136">**operator = (const D3D12 \_ GPU \_ 描述項 \_ 控制碼 &其他)**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-136">**operator=(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other)**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-137">將目前的 CD3DX12 \_ gpu \_ 描述元 \_ 控制碼設定為與指定的 D3D12 \_ gpu \_ 描述項 \_ 控制碼或 CD3DX12 \_ GPU 描述項 \_ \_ 控制碼相同的值。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-137">Sets the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE to the same values as the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-138">**內嵌 InitOffsetted (\_ In \_ const D3D12 \_ GPU \_ 描述項 \_ 控制碼 &base，INT offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-138">**inline InitOffsetted(\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-139">使用指定的專案數，初始化 [**D3D12 \_ GPU \_ 描述元 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) 結構。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-139">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with the specified number of items.</span></span> <span data-ttu-id="7e3ac-140">使用下列參數：</span><span class="sxs-lookup"><span data-stu-id="7e3ac-140">Uses the following parameters:</span></span>

<span data-ttu-id="7e3ac-141">\_在 \_ CONST D3D12 \_ GPU \_ 描述項 \_ 控制碼中 &基底：要從中位移的基底位址。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-141">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="7e3ac-142">INT offsetScaledByIncrementSize：位移的遞增數目。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-142">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-143">**內嵌 InitOffsetted (\_ In \_ const D3D12 \_ GPU \_ 描述項 \_ 控制碼 &BASE，INT offsetInDescriptors，UINT descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-143">**inline InitOffsetted(\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-144">使用指定大小的指定數量描述元，初始化具有位移的 [**D3D12 \_ GPU \_ 描述元 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) 結構。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-144">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="7e3ac-145">使用下列參數：</span><span class="sxs-lookup"><span data-stu-id="7e3ac-145">Uses the following parameters:</span></span>

<span data-ttu-id="7e3ac-146">\_在 \_ CONST D3D12 \_ GPU \_ 描述項 \_ 控制碼中 &基底：要從中位移的基底位址。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-146">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="7e3ac-147">INT offsetInDescriptors：要位移的描述項數目。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-147">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="7e3ac-148">UINT descriptorIncrementSize：每個描述項的遞增量（包括填補）。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-148">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-149">**靜態內嵌 InitOffsetted (\_ Out \_ D3D12 \_ gpu \_ 描述 \_ 項 &控制碼， \_ 在 \_ const D3D12 \_ GPU 描述項 \_ \_ 控制碼 &base，INT offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-149">**static inline InitOffsetted(\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-150">使用指定大小的指定數量描述元，初始化具有位移的 [**D3D12 \_ GPU \_ 描述元 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) 結構。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-150">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="7e3ac-151">使用下列參數：</span><span class="sxs-lookup"><span data-stu-id="7e3ac-151">Uses the following parameters:</span></span>

<span data-ttu-id="7e3ac-152">\_Out \_ D3D12 \_ gpu \_ 描述項 \_ 控制碼 &控制碼：輸出產生的 D3D12 \_ GPU \_ 描述項 \_ 控制碼。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-152">\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="7e3ac-153">\_在 \_ CONST D3D12 \_ GPU \_ 描述項 \_ 控制碼中 &基底：要從中位移的基底位址。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-153">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="7e3ac-154">INT offsetScaledByIncrementSize：位移的遞增數目。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-154">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="7e3ac-155">**靜態內嵌 InitOffsetted (\_ Out \_ D3D12 \_ gpu \_ 描述 \_ 項 &控制碼， \_ 在 \_ const D3D12 \_ GPU 描述項 \_ \_ 控制碼 &base，INT offsetInDescriptors，UINT descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-155">**static inline InitOffsetted(\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="7e3ac-156">使用指定大小的指定數量描述元，初始化具有位移的 [**D3D12 \_ GPU \_ 描述元 \_ 控制碼**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) 結構。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-156">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="7e3ac-157">使用下列參數：</span><span class="sxs-lookup"><span data-stu-id="7e3ac-157">Uses the following parameters:</span></span>

<span data-ttu-id="7e3ac-158">\_Out \_ D3D12 \_ gpu \_ 描述項 \_ 控制碼 &控制碼：輸出產生的 D3D12 \_ GPU \_ 描述項 \_ 控制碼。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-158">\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="7e3ac-159">\_在 \_ CONST D3D12 \_ GPU \_ 描述項 \_ 控制碼中 &基底：要從中位移的基底位址。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-159">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="7e3ac-160">INT offsetInDescriptors：要位移的描述項數目。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-160">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="7e3ac-161">UINT descriptorIncrementSize：每個描述項的遞增量（包括填補）。</span><span class="sxs-lookup"><span data-stu-id="7e3ac-161">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e3ac-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e3ac-162">Requirements</span></span>



| <span data-ttu-id="7e3ac-163">需求</span><span class="sxs-lookup"><span data-stu-id="7e3ac-163">Requirement</span></span> | <span data-ttu-id="7e3ac-164">值</span><span class="sxs-lookup"><span data-stu-id="7e3ac-164">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7e3ac-165">標頭</span><span class="sxs-lookup"><span data-stu-id="7e3ac-165">Header</span></span><br/> | <dl> <span data-ttu-id="7e3ac-166"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e3ac-166"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e3ac-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e3ac-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e3ac-168">**D3D12 \_ GPU \_ 描述項 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="7e3ac-168">**D3D12\_GPU\_DESCRIPTOR\_HANDLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[<span data-ttu-id="7e3ac-169">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="7e3ac-169">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 






---
description: 介面和資源建立選項的旗標。
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: 'DXGI_USAGE (DXGI. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976700"
---
# <a name="dxgi_usage"></a><span data-ttu-id="859ce-103">DXGI \_ 使用量</span><span class="sxs-lookup"><span data-stu-id="859ce-103">DXGI\_USAGE</span></span>

<span data-ttu-id="859ce-104">介面和資源建立選項的旗標。</span><span class="sxs-lookup"><span data-stu-id="859ce-104">Flags for surface and resource creation options.</span></span>



| <span data-ttu-id="859ce-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="859ce-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="859ce-106">Description</span><span class="sxs-lookup"><span data-stu-id="859ce-106">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <span data-ttu-id="859ce-107"><dt>**DXGI \_使用量 \_ 回 \_ 緩衝區**</dt> <dt>1L <<  (2 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="859ce-107"><dt>**DXGI\_USAGE\_BACK\_BUFFER**</dt> <dt>1L << (2 + 4)</dt></span></span> </dl>                             | <span data-ttu-id="859ce-108">介面或資源會用來做為背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="859ce-108">The surface or resource is used as a back buffer.</span></span> <span data-ttu-id="859ce-109">當您建立交換鏈時，不需要將 **DXGI 的 \_ 使用方式傳遞 \_ 回 \_ 緩衝區** 。</span><span class="sxs-lookup"><span data-stu-id="859ce-109">You don’t need to pass **DXGI\_USAGE\_BACK\_BUFFER** when you create a swap chain.</span></span> <span data-ttu-id="859ce-110">但是，您可以在呼叫 [**IDXGIResource：： GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) 並取得 **DXGI \_ 使用方式 \_ \_ 緩衝區** 時，判斷資源是否屬於交換鏈。</span><span class="sxs-lookup"><span data-stu-id="859ce-110">But you can determine whether a resource belongs to a swap chain when you call [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) and get **DXGI\_USAGE\_BACK\_BUFFER**.</span></span><br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <span data-ttu-id="859ce-111"><dt>**DXGI \_\_ \_ 在 \_ 目前的1L 上使用捨棄**</dt> <dt> <<  (5 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="859ce-111"><dt>**DXGI\_USAGE\_DISCARD\_ON\_PRESENT**</dt> <dt>1L << (5 + 4)</dt></span></span> </dl>       | <span data-ttu-id="859ce-112">此旗標僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="859ce-112">This flag is for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <span data-ttu-id="859ce-113"><dt>**DXGI \_使用 \_ 唯讀 \_**</dt> <dt>1L <<  (4 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="859ce-113"><dt>**DXGI\_USAGE\_READ\_ONLY**</dt> <dt>1L << (4 + 4)</dt></span></span> </dl>                                   | <span data-ttu-id="859ce-114">使用介面或資源僅供讀取。</span><span class="sxs-lookup"><span data-stu-id="859ce-114">Use the surface or resource for reading only.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <span data-ttu-id="859ce-115"><dt>**DXGI \_使用方式 \_ 呈現 \_ 目標 \_ 輸出**</dt> <dt>1L <<  (1 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="859ce-115"><dt>**DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT**</dt> <dt>1L << (1 + 4)</dt></span></span> </dl> | <span data-ttu-id="859ce-116">使用介面或資源作為輸出呈現目標。</span><span class="sxs-lookup"><span data-stu-id="859ce-116">Use the surface or resource as an output render target.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <span data-ttu-id="859ce-117"><dt>**DXGI \_使用 \_ 著色器 \_ 輸入**</dt> <dt>1L <<  (0 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="859ce-117"><dt>**DXGI\_USAGE\_SHADER\_INPUT**</dt> <dt>1L << (0 + 4)</dt></span></span> </dl>                          | <span data-ttu-id="859ce-118">使用介面或資源做為著色器的輸入。</span><span class="sxs-lookup"><span data-stu-id="859ce-118">Use the surface or resource as an input to a shader.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <span data-ttu-id="859ce-119"><dt>**DXGI \_使用量 \_ 共用**</dt> <dt>1L <<  (3 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="859ce-119"><dt>**DXGI\_USAGE\_SHARED**</dt> <dt>1L << (3 + 4)</dt></span></span> </dl>                                             | <span data-ttu-id="859ce-120">共用 surface 或資源。</span><span class="sxs-lookup"><span data-stu-id="859ce-120">Share the surface or resource.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <span data-ttu-id="859ce-121"><dt>**DXGI \_使用未 \_ 排序 \_ 存取**</dt> <dt>1L <<  (6 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="859ce-121"><dt>**DXGI\_USAGE\_UNORDERED\_ACCESS**</dt> <dt>1L << (6 + 4)</dt></span></span> </dl>              | <span data-ttu-id="859ce-122">使用介面或資源進行未排序的存取。</span><span class="sxs-lookup"><span data-stu-id="859ce-122">Use the surface or resource for unordered access.</span></span><br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="859ce-123">備註</span><span class="sxs-lookup"><span data-stu-id="859ce-123">Remarks</span></span>

<span data-ttu-id="859ce-124">每個旗標都會定義為不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="859ce-124">Each flag is defined as an unsigned integer.</span></span>

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

<span data-ttu-id="859ce-125">在呼叫 [**IDXGIFactory：： CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain)、 [**IDXGIFactory2：： CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)、 [**IDXGIFactory2：： CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)或 [**IDXGIFactory2：： CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) 方法時，會使用這些旗標選項來描述交換鏈背面緩衝區的介面使用狀況和 CPU 存取選項。</span><span class="sxs-lookup"><span data-stu-id="859ce-125">These flag options are used in a call to the [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow), or [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method to describe the surface usage and CPU access options for the back buffer of a swap chain.</span></span> <span data-ttu-id="859ce-126">您無法使用 [ **dxgi \_ \_ 共用**]、[ **dxgi 使用方式 \_ \_ \_ \_ 捨棄**] 和 [ **dxgi \_ 使用 \_ 唯讀 \_** ] 值做為輸入來建立交換鏈。</span><span class="sxs-lookup"><span data-stu-id="859ce-126">You can't use the **DXGI\_USAGE\_SHARED**, **DXGI\_USAGE\_DISCARD\_ON\_PRESENT**, and **DXGI\_USAGE\_READ\_ONLY** values as input to create a swap chain.</span></span> <span data-ttu-id="859ce-127">不過，DXGI 可以 **\_ \_ \_ 在 \_ 目前的情況下設定 dxgi 使用方式捨棄** ，而在應用程式上，對某些交換鏈的背景緩衝區進行 **\_ \_ 唯讀 \_ 使用** 。</span><span class="sxs-lookup"><span data-stu-id="859ce-127">However, DXGI can set **DXGI\_USAGE\_DISCARD\_ON\_PRESENT** and **DXGI\_USAGE\_READ\_ONLY** for some of the swap chain's back buffers on the application's behalf.</span></span> <span data-ttu-id="859ce-128">您可以呼叫 [**IDXGIResource：： GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) 方法來取得這些背景緩衝區的使用方式。</span><span class="sxs-lookup"><span data-stu-id="859ce-128">You can call the [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) method to retrieve the usage of these back buffers.</span></span> <span data-ttu-id="859ce-129">交換鏈在 **dxgi \_ 使用量** 的 [ **dxgi \_ cpu \_ 存取] \_ 欄位** 部分中，僅支援 [ **dxgi \_ cpu \_ 存取 \_ 無**] 值。</span><span class="sxs-lookup"><span data-stu-id="859ce-129">Swap chain's only support the **DXGI\_CPU\_ACCESS\_NONE** value in the **DXGI\_CPU\_ACCESS\_FIELD** part of **DXGI\_USAGE**.</span></span>

<span data-ttu-id="859ce-130">[**IDXGIDevice：： CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface)方法也會使用這些旗標選項。</span><span class="sxs-lookup"><span data-stu-id="859ce-130">These flag options are also used by the [**IDXGIDevice::CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="859ce-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="859ce-131">Requirements</span></span>



| <span data-ttu-id="859ce-132">需求</span><span class="sxs-lookup"><span data-stu-id="859ce-132">Requirement</span></span> | <span data-ttu-id="859ce-133">值</span><span class="sxs-lookup"><span data-stu-id="859ce-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="859ce-134">標頭</span><span class="sxs-lookup"><span data-stu-id="859ce-134">Header</span></span><br/> | <dl> <span data-ttu-id="859ce-135"><dt>DXGI。h</dt></span><span class="sxs-lookup"><span data-stu-id="859ce-135"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="859ce-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="859ce-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="859ce-137">DXGI 常數</span><span class="sxs-lookup"><span data-stu-id="859ce-137">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 





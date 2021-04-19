---
title: IDXCoreAdapter::QueryState
description: 抓取介面卡上所指定專案的目前狀態。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966469"
---
# <a name="idxcoreadapterquerystate-method"></a><span data-ttu-id="93ffc-103">IDXCoreAdapter：： QueryState 方法</span><span class="sxs-lookup"><span data-stu-id="93ffc-103">IDXCoreAdapter::QueryState method</span></span>

<span data-ttu-id="93ffc-104">抓取介面卡上所指定專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="93ffc-104">Retrieves the current state of the specified item on the adapter.</span></span> <span data-ttu-id="93ffc-105">在呼叫屬性類型的 **QueryState** 之前，請先呼叫 [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) ，確認此介面卡與作業系統 (OS) 可以使用此狀態種類。</span><span class="sxs-lookup"><span data-stu-id="93ffc-105">Before calling **QueryState** for a property type, call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="93ffc-106">語法</span><span class="sxs-lookup"><span data-stu-id="93ffc-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a><span data-ttu-id="93ffc-107">參數</span><span class="sxs-lookup"><span data-stu-id="93ffc-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="93ffc-108">狀態</span><span class="sxs-lookup"><span data-stu-id="93ffc-108">state</span></span>

<span data-ttu-id="93ffc-109">類型： **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="93ffc-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="93ffc-110">介面卡上您想要取得其狀態的狀態專案類型。</span><span class="sxs-lookup"><span data-stu-id="93ffc-110">The kind of state item on the adapter whose state you wish to retrieve.</span></span> <span data-ttu-id="93ffc-111">如需每個介面卡狀態種類的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。</span><span class="sxs-lookup"><span data-stu-id="93ffc-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="93ffc-112">inputStateDetailsSize</span><span class="sxs-lookup"><span data-stu-id="93ffc-112">inputStateDetailsSize</span></span>

<span data-ttu-id="93ffc-113">類型： **size_t**</span><span class="sxs-lookup"><span data-stu-id="93ffc-113">Type: **size_t**</span></span>

<span data-ttu-id="93ffc-114">您 (選擇性地) 配置並在 *inputStateDetails* 中提供的輸入狀態詳細資料緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="93ffc-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="93ffc-115">inputStateDetails [in]</span><span class="sxs-lookup"><span data-stu-id="93ffc-115">inputStateDetails [in]</span></span>

<span data-ttu-id="93ffc-116">類型： **void const \***</span><span class="sxs-lookup"><span data-stu-id="93ffc-116">Type: **void const\***</span></span>

<span data-ttu-id="93ffc-117">您在應用程式中配置的常數輸入狀態詳細資料緩衝區的選擇性指標，其中包含您在 [ *狀態*] 中指定之狀態類型所需的任何要求資訊。</span><span class="sxs-lookup"><span data-stu-id="93ffc-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="93ffc-118">如需特定狀態種類的任何輸入緩衝區需求的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。</span><span class="sxs-lookup"><span data-stu-id="93ffc-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="outputbuffersize"></a><span data-ttu-id="93ffc-119">outputBufferSize</span><span class="sxs-lookup"><span data-stu-id="93ffc-119">outputBufferSize</span></span>

<span data-ttu-id="93ffc-120">類型： **size_t**</span><span class="sxs-lookup"><span data-stu-id="93ffc-120">Type: **size_t**</span></span>

<span data-ttu-id="93ffc-121">您在 *outputBuffer* 中配置並提供之輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="93ffc-121">The size, in bytes, of the output buffer that you allocate and provide in *outputBuffer*.</span></span>

### <a name="outputbuffer-out"></a><span data-ttu-id="93ffc-122">outputBuffer [out]</span><span class="sxs-lookup"><span data-stu-id="93ffc-122">outputBuffer [out]</span></span>

<span data-ttu-id="93ffc-123">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="93ffc-123">Type: **void\***</span></span>

<span data-ttu-id="93ffc-124">您在應用程式中配置的輸出緩衝區指標，且該函式會填入。</span><span class="sxs-lookup"><span data-stu-id="93ffc-124">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="93ffc-125">如需特定狀態種類之輸出緩衝區需求的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。</span><span class="sxs-lookup"><span data-stu-id="93ffc-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the output buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="93ffc-126">傳回</span><span class="sxs-lookup"><span data-stu-id="93ffc-126">Returns</span></span>

<span data-ttu-id="93ffc-127">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="93ffc-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="93ffc-128">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="93ffc-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="93ffc-129">否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。</span><span class="sxs-lookup"><span data-stu-id="93ffc-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="93ffc-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="93ffc-130">Return value</span></span>|<span data-ttu-id="93ffc-131">描述</span><span class="sxs-lookup"><span data-stu-id="93ffc-131">Description</span></span>|
|-|-|
|<span data-ttu-id="93ffc-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="93ffc-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="93ffc-133">介面卡不再處於有效狀態。</span><span class="sxs-lookup"><span data-stu-id="93ffc-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="93ffc-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="93ffc-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="93ffc-135">此作業系統 (OS) 無法辨識 *狀態* 中指定的狀態種類。</span><span class="sxs-lookup"><span data-stu-id="93ffc-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="93ffc-136">呼叫 [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) 確認此介面卡與作業系統 (OS) 可以使用查詢狀態種類。</span><span class="sxs-lookup"><span data-stu-id="93ffc-136">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="93ffc-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="93ffc-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="93ffc-138">介面卡不支援 *狀態* 中指定的狀態種類。</span><span class="sxs-lookup"><span data-stu-id="93ffc-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="93ffc-139">呼叫 [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) 確認此介面卡與作業系統 (OS) 可以使用查詢狀態種類。</span><span class="sxs-lookup"><span data-stu-id="93ffc-139">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="93ffc-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="93ffc-140">E_INVALIDARG</span></span>|<span data-ttu-id="93ffc-141">提供的緩衝區大小不足以供 *outputBuffer* (或 *inputStateDetails* ，其中需要輸入狀態詳細資料緩衝區) 。</span><span class="sxs-lookup"><span data-stu-id="93ffc-141">An insufficient buffer size is provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="93ffc-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="93ffc-142">E_POINTER</span></span>|<span data-ttu-id="93ffc-143">`nullptr` 提供給 *outputBuffer* (或 *inputStateDetails* ，其中需要輸入狀態詳細資料緩衝區) 。</span><span class="sxs-lookup"><span data-stu-id="93ffc-143">`nullptr` was provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="remarks"></a><span data-ttu-id="93ffc-144">備註</span><span class="sxs-lookup"><span data-stu-id="93ffc-144">Remarks</span></span>

<span data-ttu-id="93ffc-145">如需每個介面卡狀態種類的詳細資訊，以及使用的輸入和輸出，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 。</span><span class="sxs-lookup"><span data-stu-id="93ffc-145">See [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind, and what inputs and outputs are used.</span></span> <span data-ttu-id="93ffc-146">在填入之前，此函式會將 *outputBuffer* 緩衝區設為零。</span><span class="sxs-lookup"><span data-stu-id="93ffc-146">This function zeros out the *outputBuffer* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="93ffc-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93ffc-147">See also</span></span>

<span data-ttu-id="93ffc-148">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="93ffc-148">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
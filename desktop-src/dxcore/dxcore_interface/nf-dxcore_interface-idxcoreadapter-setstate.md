---
title: IDXCoreAdapter::SetState
description: 在介面卡上設定指定專案的狀態。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8cbeacdb8c6020441b5dd74a9f9233a6c112b4f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968108"
---
# <a name="idxcoreadaptersetstate-method"></a><span data-ttu-id="0f0d2-103">IDXCoreAdapter：： SetState 方法</span><span class="sxs-lookup"><span data-stu-id="0f0d2-103">IDXCoreAdapter::SetState method</span></span>

<span data-ttu-id="0f0d2-104">在介面卡上設定指定專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-104">Sets the state of the specified item on the adapter.</span></span> <span data-ttu-id="0f0d2-105">在呼叫屬性類型的 **SetState** 之前，請先呼叫 [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) ，確認此介面卡和作業系統 (OS) 的設定狀態種類是否可用。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-105">Before calling **SetState** for a property type, call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0d2-106">語法</span><span class="sxs-lookup"><span data-stu-id="0f0d2-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a><span data-ttu-id="0f0d2-107">參數</span><span class="sxs-lookup"><span data-stu-id="0f0d2-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="0f0d2-108">狀態</span><span class="sxs-lookup"><span data-stu-id="0f0d2-108">state</span></span>

<span data-ttu-id="0f0d2-109">類型： **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="0f0d2-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="0f0d2-110">您要設定其狀態的介面卡上狀態專案類型。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-110">The kind of state item on the adapter whose state you wish to set.</span></span> <span data-ttu-id="0f0d2-111">如需每個介面卡狀態種類的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="0f0d2-112">inputStateDetailsSize</span><span class="sxs-lookup"><span data-stu-id="0f0d2-112">inputStateDetailsSize</span></span>

<span data-ttu-id="0f0d2-113">類型： **size_t**</span><span class="sxs-lookup"><span data-stu-id="0f0d2-113">Type: **size_t**</span></span>

<span data-ttu-id="0f0d2-114">您 (選擇性地) 配置並在 *inputStateDetails* 中提供的輸入狀態詳細資料緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="0f0d2-115">inputStateDetails [in]</span><span class="sxs-lookup"><span data-stu-id="0f0d2-115">inputStateDetails [in]</span></span>

<span data-ttu-id="0f0d2-116">類型： **void const \***</span><span class="sxs-lookup"><span data-stu-id="0f0d2-116">Type: **void const\***</span></span>

<span data-ttu-id="0f0d2-117">您在應用程式中配置的常數輸入狀態詳細資料緩衝區的選擇性指標，其中包含您在 [ *狀態*] 中指定之狀態類型所需的任何要求資訊。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="0f0d2-118">如需特定狀態種類的任何輸入緩衝區需求的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="inputdatasize"></a><span data-ttu-id="0f0d2-119">inputDataSize</span><span class="sxs-lookup"><span data-stu-id="0f0d2-119">inputDataSize</span></span>

<span data-ttu-id="0f0d2-120">類型： **size_t**</span><span class="sxs-lookup"><span data-stu-id="0f0d2-120">Type: **size_t**</span></span>

<span data-ttu-id="0f0d2-121">您在 *inputData* 中配置並提供之輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-121">The size, in bytes, of the input buffer that you allocate and provide in *inputData*.</span></span>

### <a name="inputdata-in"></a><span data-ttu-id="0f0d2-122">inputData [in]</span><span class="sxs-lookup"><span data-stu-id="0f0d2-122">inputData [in]</span></span>

<span data-ttu-id="0f0d2-123">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="0f0d2-123">Type: **void\***</span></span>

<span data-ttu-id="0f0d2-124">您在應用程式中配置之輸入緩衝區的指標，其中包含要針對您在 [ *狀態*] 中指定之狀態專案設定的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-124">A pointer to an input buffer that you allocate in your application, containing the state information to set for the state item whose kind you specify in *state*.</span></span> <span data-ttu-id="0f0d2-125">如需特定狀態種類之輸入緩衝區需求的詳細資訊，請參閱 [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) 中的表格。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the input buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="0f0d2-126">傳回</span><span class="sxs-lookup"><span data-stu-id="0f0d2-126">Returns</span></span>

<span data-ttu-id="0f0d2-127">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="0f0d2-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="0f0d2-128">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="0f0d2-129">否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="0f0d2-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f0d2-130">Return value</span></span>|<span data-ttu-id="0f0d2-131">描述</span><span class="sxs-lookup"><span data-stu-id="0f0d2-131">Description</span></span>|
|-|-|
|<span data-ttu-id="0f0d2-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="0f0d2-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="0f0d2-133">介面卡不再處於有效狀態。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="0f0d2-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="0f0d2-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="0f0d2-135">此作業系統 (OS) 無法辨識 *狀態* 中指定的狀態種類。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="0f0d2-136">呼叫 [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) ，確認此介面卡和作業系統 (OS) 的設定狀態是否可用。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-136">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="0f0d2-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="0f0d2-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="0f0d2-138">介面卡不支援 *狀態* 中指定的狀態種類。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="0f0d2-139">呼叫 [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) ，確認此介面卡和作業系統 (OS) 的設定狀態是否可用。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-139">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="0f0d2-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0f0d2-140">E_INVALIDARG</span></span>|<span data-ttu-id="0f0d2-141">提供的緩衝區大小不足以供 *inputData* (或 *inputStateDetails* ，其中需要輸入狀態詳細資料緩衝區) 。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-141">An insufficient buffer size is provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="0f0d2-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="0f0d2-142">E_POINTER</span></span>|<span data-ttu-id="0f0d2-143">`nullptr` 提供給 *inputData* (或 *inputStateDetails* ，其中需要輸入狀態詳細資料緩衝區) 。</span><span class="sxs-lookup"><span data-stu-id="0f0d2-143">`nullptr` was provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="see-also"></a><span data-ttu-id="0f0d2-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f0d2-144">See also</span></span>

<span data-ttu-id="0f0d2-145">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="0f0d2-145">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
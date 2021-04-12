---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: 取得指定之 LUID 的 DXCore 介面卡物件 ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) （如果有的話）。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376165"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a><span data-ttu-id="bfec3-103">IDXCoreAdapterFactory：： GetAdapterByLuid 方法</span><span class="sxs-lookup"><span data-stu-id="bfec3-103">IDXCoreAdapterFactory::GetAdapterByLuid method</span></span>

<span data-ttu-id="bfec3-104">取得指定之 LUID 的 DXCore 介面卡物件 ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="bfec3-104">Retrieves the DXCore adapter object ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) for a specified LUID, if available.</span></span> <span data-ttu-id="bfec3-105">如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。</span><span class="sxs-lookup"><span data-stu-id="bfec3-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfec3-106">語法</span><span class="sxs-lookup"><span data-stu-id="bfec3-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="bfec3-107">參數</span><span class="sxs-lookup"><span data-stu-id="bfec3-107">Parameters</span></span>

### <a name="adapterluid"></a><span data-ttu-id="bfec3-108">adapterLUID</span><span class="sxs-lookup"><span data-stu-id="bfec3-108">adapterLUID</span></span>

<span data-ttu-id="bfec3-109">類型： **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span><span class="sxs-lookup"><span data-stu-id="bfec3-109">Type: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span></span>

<span data-ttu-id="bfec3-110">識別介面卡實例的本地唯一值。</span><span class="sxs-lookup"><span data-stu-id="bfec3-110">The locally unique value that identifies the adapter instance.</span></span>

### <a name="riid-in"></a><span data-ttu-id="bfec3-111">riid [in]</span><span class="sxs-lookup"><span data-stu-id="bfec3-111">riid [in]</span></span>

<span data-ttu-id="bfec3-112">類型： **REFIID**</span><span class="sxs-lookup"><span data-stu-id="bfec3-112">Type: **REFIID**</span></span>

<span data-ttu-id="bfec3-113">全域唯一識別碼的參考， (您想要在 *ppvAdapter* 中傳回之介面的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="bfec3-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="bfec3-114">這應該是 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)的介面識別碼 (IID) 。</span><span class="sxs-lookup"><span data-stu-id="bfec3-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="bfec3-115">ppvAdapter [out]</span><span class="sxs-lookup"><span data-stu-id="bfec3-115">ppvAdapter [out]</span></span>

<span data-ttu-id="bfec3-116">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="bfec3-116">Type: **void\*\***</span></span>

<span data-ttu-id="bfec3-117">具有在 *riid* 參數中指定之 IID 之介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="bfec3-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="bfec3-118">在成功傳回時， *\* ppvAdapter* (已取值的位址) 包含已建立之 DXCore 介面卡的指標。</span><span class="sxs-lookup"><span data-stu-id="bfec3-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="bfec3-119">傳回</span><span class="sxs-lookup"><span data-stu-id="bfec3-119">Returns</span></span>

<span data-ttu-id="bfec3-120">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="bfec3-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="bfec3-121">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="bfec3-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="bfec3-122">否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。</span><span class="sxs-lookup"><span data-stu-id="bfec3-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="bfec3-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfec3-123">Return value</span></span>|<span data-ttu-id="bfec3-124">描述</span><span class="sxs-lookup"><span data-stu-id="bfec3-124">Description</span></span>|
|-|-|
|<span data-ttu-id="bfec3-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="bfec3-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="bfec3-126">已辨識傳入 *adapterLUID* 的介面卡 LUID，但介面卡已不再處於有效狀態。</span><span class="sxs-lookup"><span data-stu-id="bfec3-126">The adapter LUID passed in *adapterLUID* is recognized, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="bfec3-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="bfec3-127">E_INVALIDARG</span></span>|<span data-ttu-id="bfec3-128">由於 *adapterLUID* 中傳遞的值可透過 DXCore 取得，因此不會有這種介面卡 LUID。</span><span class="sxs-lookup"><span data-stu-id="bfec3-128">No such adapter LUID as the value passed in *adapterLUID* is available through DXCore.</span></span>|
|<span data-ttu-id="bfec3-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="bfec3-129">E_NOINTERFACE</span></span>|<span data-ttu-id="bfec3-130">針對 *riid* 提供的值無效。</span><span class="sxs-lookup"><span data-stu-id="bfec3-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="bfec3-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="bfec3-131">E_POINTER</span></span>|<span data-ttu-id="bfec3-132">`nullptr` 是為 *ppvAdapter* 所提供。</span><span class="sxs-lookup"><span data-stu-id="bfec3-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bfec3-133">備註</span><span class="sxs-lookup"><span data-stu-id="bfec3-133">Remarks</span></span>

<span data-ttu-id="bfec3-134">傳遞相同 [LUID](/windows/win32/api/winnt/ns-winnt-luid) 的多個呼叫會傳回相同的介面指標。</span><span class="sxs-lookup"><span data-stu-id="bfec3-134">Multiple calls passing the same [LUID](/windows/win32/api/winnt/ns-winnt-luid) return identical interface pointers.</span></span> <span data-ttu-id="bfec3-135">因此，可以安全地比較介面指標，以判斷多個指標是否參考相同的介面卡物件。</span><span class="sxs-lookup"><span data-stu-id="bfec3-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="bfec3-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfec3-136">See also</span></span>

<span data-ttu-id="bfec3-137">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="bfec3-137">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
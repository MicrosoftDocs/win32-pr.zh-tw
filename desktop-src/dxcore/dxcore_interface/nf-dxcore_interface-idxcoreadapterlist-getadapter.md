---
title: IDXCoreAdapterList::GetAdapter
description: 從 DXCore 介面卡清單物件的索引抓取特定的介面卡。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023903"
---
# <a name="idxcoreadapterlistgetadapter-method"></a><span data-ttu-id="75d49-103">IDXCoreAdapterList：： GetAdapter 方法</span><span class="sxs-lookup"><span data-stu-id="75d49-103">IDXCoreAdapterList::GetAdapter method</span></span>

<span data-ttu-id="75d49-104">從 DXCore 介面卡清單物件的索引抓取特定的介面卡。</span><span class="sxs-lookup"><span data-stu-id="75d49-104">Retrieves a specific adapter by index from a DXCore adapter list object.</span></span> <span data-ttu-id="75d49-105">如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。</span><span class="sxs-lookup"><span data-stu-id="75d49-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="75d49-106">語法</span><span class="sxs-lookup"><span data-stu-id="75d49-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="75d49-107">參數</span><span class="sxs-lookup"><span data-stu-id="75d49-107">Parameters</span></span>

### <a name="index"></a><span data-ttu-id="75d49-108">索引</span><span class="sxs-lookup"><span data-stu-id="75d49-108">index</span></span>

<span data-ttu-id="75d49-109">類型： **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="75d49-109">Type: **uint32_t**</span></span>

<span data-ttu-id="75d49-110">以零為基底的索引，識別 DXCore 介面卡清單中的介面卡實例。</span><span class="sxs-lookup"><span data-stu-id="75d49-110">A zero-based index, identifying an adapter instance within the DXCore adapter list.</span></span>

### <a name="riid"></a><span data-ttu-id="75d49-111">riid</span><span class="sxs-lookup"><span data-stu-id="75d49-111">riid</span></span>

<span data-ttu-id="75d49-112">類型： **REFIID**</span><span class="sxs-lookup"><span data-stu-id="75d49-112">Type: **REFIID**</span></span>

<span data-ttu-id="75d49-113">全域唯一識別碼的參考， (您想要在 *ppvAdapter* 中傳回之介面的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="75d49-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="75d49-114">這應該是 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)的介面識別碼 (IID) 。</span><span class="sxs-lookup"><span data-stu-id="75d49-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="75d49-115">ppvAdapter [out]</span><span class="sxs-lookup"><span data-stu-id="75d49-115">ppvAdapter [out]</span></span>

<span data-ttu-id="75d49-116">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="75d49-116">Type: **void\*\***</span></span>

<span data-ttu-id="75d49-117">具有在 *riid* 參數中指定之 IID 之介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="75d49-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="75d49-118">在成功傳回時， *\* ppvAdapter* (已取值的位址) 包含已建立之 DXCore 介面卡的指標。</span><span class="sxs-lookup"><span data-stu-id="75d49-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="75d49-119">傳回</span><span class="sxs-lookup"><span data-stu-id="75d49-119">Returns</span></span>

<span data-ttu-id="75d49-120">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="75d49-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="75d49-121">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="75d49-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="75d49-122">否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。</span><span class="sxs-lookup"><span data-stu-id="75d49-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="75d49-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="75d49-123">Return value</span></span>|<span data-ttu-id="75d49-124">描述</span><span class="sxs-lookup"><span data-stu-id="75d49-124">Description</span></span>|
|-|-|
|<span data-ttu-id="75d49-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="75d49-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="75d49-126">*索引* 是有效的，但介面卡不再處於有效的狀態。</span><span class="sxs-lookup"><span data-stu-id="75d49-126">The *index* is valid, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="75d49-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="75d49-127">E_INVALIDARG</span></span>|<span data-ttu-id="75d49-128">提供的 *索引* 無效。</span><span class="sxs-lookup"><span data-stu-id="75d49-128">The provided *index* is not valid.</span></span>|
|<span data-ttu-id="75d49-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="75d49-129">E_NOINTERFACE</span></span>|<span data-ttu-id="75d49-130">針對 *riid* 提供的值無效。</span><span class="sxs-lookup"><span data-stu-id="75d49-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="75d49-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="75d49-131">E_POINTER</span></span>|<span data-ttu-id="75d49-132">`nullptr` 是為 *ppvAdapter* 所提供。</span><span class="sxs-lookup"><span data-stu-id="75d49-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="75d49-133">備註</span><span class="sxs-lookup"><span data-stu-id="75d49-133">Remarks</span></span>

<span data-ttu-id="75d49-134">傳遞代表相同介面卡之索引的多個呼叫會傳回相同的介面指標，甚至是跨不同的介面卡清單。</span><span class="sxs-lookup"><span data-stu-id="75d49-134">Multiple calls passing an index that represents the same adapter return identical interface pointers, even across different adapter lists.</span></span> <span data-ttu-id="75d49-135">因此，可以安全地比較介面指標，以判斷多個指標是否參考相同的介面卡物件。</span><span class="sxs-lookup"><span data-stu-id="75d49-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="75d49-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75d49-136">See also</span></span>

<span data-ttu-id="75d49-137">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="75d49-137">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
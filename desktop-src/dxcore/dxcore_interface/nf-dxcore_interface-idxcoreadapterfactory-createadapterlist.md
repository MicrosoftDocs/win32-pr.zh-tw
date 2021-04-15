---
title: IDXCoreAdapterFactory::CreateAdapterList
description: 產生介面卡物件的清單，表示系統目前的介面卡狀態，並符合指定的準則。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463460"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a><span data-ttu-id="48dfc-103">IDXCoreAdapterFactory：： CreateAdapterList 方法</span><span class="sxs-lookup"><span data-stu-id="48dfc-103">IDXCoreAdapterFactory::CreateAdapterList method</span></span>

<span data-ttu-id="48dfc-104">產生介面卡物件的清單，表示系統目前的介面卡狀態，並符合指定的準則。</span><span class="sxs-lookup"><span data-stu-id="48dfc-104">Generates a list of adapter objects representing the current adapter state of the system, and meeting the criteria specified.</span></span> <span data-ttu-id="48dfc-105">如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。</span><span class="sxs-lookup"><span data-stu-id="48dfc-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="48dfc-106">語法</span><span class="sxs-lookup"><span data-stu-id="48dfc-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a><span data-ttu-id="48dfc-107">參數</span><span class="sxs-lookup"><span data-stu-id="48dfc-107">Parameters</span></span>

### <a name="numattributes"></a><span data-ttu-id="48dfc-108">numAttributes</span><span class="sxs-lookup"><span data-stu-id="48dfc-108">numAttributes</span></span>

<span data-ttu-id="48dfc-109">類型： **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="48dfc-109">Type: **uint32_t**</span></span>

<span data-ttu-id="48dfc-110">*FilterAttributes* 引數所指向之陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="48dfc-110">The number of elements in the array pointed to by the *filterAttributes* argument.</span></span>

### <a name="filterattributes-in"></a><span data-ttu-id="48dfc-111">filterAttributes [in]</span><span class="sxs-lookup"><span data-stu-id="48dfc-111">filterAttributes [in]</span></span>

<span data-ttu-id="48dfc-112">類型： **CONST GUID \***</span><span class="sxs-lookup"><span data-stu-id="48dfc-112">Type: **const GUID\***</span></span>

<span data-ttu-id="48dfc-113">介面卡屬性 Guid 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="48dfc-113">A pointer to an array of adapter attribute GUIDs.</span></span> <span data-ttu-id="48dfc-114">如需屬性 Guid 清單，請參閱 [DXCore adapter 屬性 guid](../dxcore-adapter-attribute-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="48dfc-114">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span> <span data-ttu-id="48dfc-115">至少必須提供一個 GUID。</span><span class="sxs-lookup"><span data-stu-id="48dfc-115">At least one GUID must be provided.</span></span> <span data-ttu-id="48dfc-116">在陣列中提供一個以上的 GUID 的情況下，傳回的清單中只會包含符合 *所有* 要求屬性的介面卡。</span><span class="sxs-lookup"><span data-stu-id="48dfc-116">In the case that more than one GUID is provided in the array, only adapters that meet *all* of the requested attributes will be included in the returned list.</span></span>

### <a name="riid"></a><span data-ttu-id="48dfc-117">riid</span><span class="sxs-lookup"><span data-stu-id="48dfc-117">riid</span></span>

<span data-ttu-id="48dfc-118">類型： **REFIID**</span><span class="sxs-lookup"><span data-stu-id="48dfc-118">Type: **REFIID**</span></span>

<span data-ttu-id="48dfc-119">全域唯一識別碼的參考， (您想要在 *ppvAdapterList* 中傳回之介面的 GUID) 。</span><span class="sxs-lookup"><span data-stu-id="48dfc-119">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapterList*.</span></span> <span data-ttu-id="48dfc-120">這應該是 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)的介面識別碼 (IID) 。</span><span class="sxs-lookup"><span data-stu-id="48dfc-120">This is expected to be the interface identifier (IID) of [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).</span></span>

### <a name="ppvadapterlist-out"></a><span data-ttu-id="48dfc-121">ppvAdapterList [out]</span><span class="sxs-lookup"><span data-stu-id="48dfc-121">ppvAdapterList [out]</span></span>

<span data-ttu-id="48dfc-122">類型： **void \* \***</span><span class="sxs-lookup"><span data-stu-id="48dfc-122">Type: **void\*\***</span></span>

<span data-ttu-id="48dfc-123">具有在 *riid* 參數中指定之 IID 之介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="48dfc-123">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="48dfc-124">在成功傳回時， *\* ppvAdapterList* (已取值的位址) 包含已建立之介面卡清單的指標。</span><span class="sxs-lookup"><span data-stu-id="48dfc-124">Upon successful return, *\*ppvAdapterList* (the dereferenced address) contains a pointer to the adapter list created.</span></span>

## <a name="returns"></a><span data-ttu-id="48dfc-125">傳回</span><span class="sxs-lookup"><span data-stu-id="48dfc-125">Returns</span></span>

<span data-ttu-id="48dfc-126">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="48dfc-126">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="48dfc-127">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="48dfc-127">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="48dfc-128">否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。</span><span class="sxs-lookup"><span data-stu-id="48dfc-128">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="48dfc-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="48dfc-129">Return value</span></span>|<span data-ttu-id="48dfc-130">描述</span><span class="sxs-lookup"><span data-stu-id="48dfc-130">Description</span></span>|
|-|-|
|<span data-ttu-id="48dfc-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="48dfc-131">E_INVALIDARG</span></span>|<span data-ttu-id="48dfc-132">`nullptr` 為 *filterAttributes* 提供，或為 *numAttributes* 提供0。</span><span class="sxs-lookup"><span data-stu-id="48dfc-132">`nullptr` was provided for *filterAttributes*, or 0 was provided for *numAttributes*.</span></span>|
|<span data-ttu-id="48dfc-133">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="48dfc-133">E_NOINTERFACE</span></span>|<span data-ttu-id="48dfc-134">針對 *riid* 提供的值無效。</span><span class="sxs-lookup"><span data-stu-id="48dfc-134">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="48dfc-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="48dfc-135">E_POINTER</span></span>|<span data-ttu-id="48dfc-136">`nullptr` 是為 *ppvAdapterList* 所提供。</span><span class="sxs-lookup"><span data-stu-id="48dfc-136">`nullptr` was provided for *ppvAdapterList*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="48dfc-137">備註</span><span class="sxs-lookup"><span data-stu-id="48dfc-137">Remarks</span></span>

<span data-ttu-id="48dfc-138">即使找不到介面卡，只要引數有效， **CreateAdapterList** 就會建立有效的 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 物件，並傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="48dfc-138">Even if no adapters are found, as long as the arguments are valid, **CreateAdapterList** creates a valid [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object, and returns **S_OK**.</span></span> <span data-ttu-id="48dfc-139">產生之後，此特定清單中的介面卡不會變更。</span><span class="sxs-lookup"><span data-stu-id="48dfc-139">Once generated, the adapters in this specific list won't change.</span></span> <span data-ttu-id="48dfc-140">但是，如果其中一張介面卡變成無效，或新的介面卡抵達符合提供的篩選準則，則會將清單視為過時。</span><span class="sxs-lookup"><span data-stu-id="48dfc-140">But the list will be considered stale if one of the adapters later becomes invalid, or if a new adapter arrives that meets the provided filter criteria.</span></span> <span data-ttu-id="48dfc-141">**CreateAdapterList** 傳回的清單不會以任何特定方式排序，但是清單的順序在多個呼叫之間是一致的，甚至是跨作業系統重新開機。</span><span class="sxs-lookup"><span data-stu-id="48dfc-141">The list returned by **CreateAdapterList** is not ordered in any particular way, but the ordering of a list is consistent across multiple calls, and even across operating system restarts.</span></span> <span data-ttu-id="48dfc-142">順序可能會在系統設定變更時變更，包括新增或移除介面卡，或在現有的介面卡上進行驅動程式更新。</span><span class="sxs-lookup"><span data-stu-id="48dfc-142">The ordering may change upon system configuration changes, including the addition or removal of an adapter, or a driver update on an existing adapter.</span></span> <span data-ttu-id="48dfc-143">您可以使用 [IDXCoreAdapterFactory：： RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) 來註冊這些變更，其方式是使用通知類型 **DXCoreNotificationType. AdapterListStale**。</span><span class="sxs-lookup"><span data-stu-id="48dfc-143">You can register for these changes with [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) using the notification type **DXCoreNotificationType.AdapterListStale**.</span></span>

## <a name="see-also"></a><span data-ttu-id="48dfc-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48dfc-144">See also</span></span>

<span data-ttu-id="48dfc-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="48dfc-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
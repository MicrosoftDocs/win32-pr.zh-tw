---
title: IDXCoreAdapterList::Sort
description: 根據提供的排序準則輸入陣列來排序 DXCore 介面卡清單物件。
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093155"
---
# <a name="idxcoreadapterlistsort-method"></a><span data-ttu-id="03687-103">IDXCoreAdapterList：： Sort 方法</span><span class="sxs-lookup"><span data-stu-id="03687-103">IDXCoreAdapterList::Sort method</span></span>

## <a name="description"></a><span data-ttu-id="03687-104">Description</span><span class="sxs-lookup"><span data-stu-id="03687-104">Description</span></span>

<span data-ttu-id="03687-105">根據提供的排序準則輸入陣列排序 DXCore 介面卡清單物件，其中較早在準則陣列中的陣列專案會獲得較高的加權。</span><span class="sxs-lookup"><span data-stu-id="03687-105">Sorts a DXCore adapter list object based on a provided input array of sort criteria, where array items earlier in the array of criteria are given a higher weight.</span></span> <span data-ttu-id="03687-106">**排序** 可協助您更輕鬆地在介面卡清單中尋找理想的介面卡。</span><span class="sxs-lookup"><span data-stu-id="03687-106">**Sort** helps you to more easily find your ideal adapter in an adapter list.</span></span>

## <a name="syntax"></a><span data-ttu-id="03687-107">語法</span><span class="sxs-lookup"><span data-stu-id="03687-107">Syntax</span></span>

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a><span data-ttu-id="03687-108">參數</span><span class="sxs-lookup"><span data-stu-id="03687-108">Parameters</span></span>

### <a name="numpreferences"></a><span data-ttu-id="03687-109">numPreferences</span><span class="sxs-lookup"><span data-stu-id="03687-109">numPreferences</span></span>

<span data-ttu-id="03687-110">類型： **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="03687-110">Type: **uint32_t**</span></span>

<span data-ttu-id="03687-111">*喜好* 設定參數所指向之陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="03687-111">The number of elements that are in the array pointed to by the *preferences* parameter.</span></span>

### <a name="preferences-in"></a><span data-ttu-id="03687-112">喜好設定 [in]</span><span class="sxs-lookup"><span data-stu-id="03687-112">preferences [in]</span></span>

<span data-ttu-id="03687-113">Type： **Const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***</span><span class="sxs-lookup"><span data-stu-id="03687-113">Type: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)\***</span></span>

<span data-ttu-id="03687-114">[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)值之常數陣列的指標，代表排序準則。</span><span class="sxs-lookup"><span data-stu-id="03687-114">A pointer to a constant array of [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) values, representing sort criteria.</span></span>

## <a name="returns"></a><span data-ttu-id="03687-115">傳回</span><span class="sxs-lookup"><span data-stu-id="03687-115">Returns</span></span>

<span data-ttu-id="03687-116">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="03687-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="03687-117">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="03687-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="03687-118">否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。</span><span class="sxs-lookup"><span data-stu-id="03687-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="03687-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="03687-119">Return value</span></span>|<span data-ttu-id="03687-120">描述</span><span class="sxs-lookup"><span data-stu-id="03687-120">Description</span></span>|
|-|-|
|<span data-ttu-id="03687-121">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="03687-121">E_INVALIDARG</span></span>|<span data-ttu-id="03687-122">*NumPreferences* 引數為零，或 *喜好* 設定引數為 `nullptr` 。</span><span class="sxs-lookup"><span data-stu-id="03687-122">The *numPreferences* argument is zero, or the *preferences* argument is `nullptr`.</span></span>|

## <a name="remarks"></a><span data-ttu-id="03687-123">備註</span><span class="sxs-lookup"><span data-stu-id="03687-123">Remarks</span></span>

<span data-ttu-id="03687-124">如果作業系統 (OS) 無法辨識提供的 [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) 值，則會予以忽略，而不會導致 API 失敗。</span><span class="sxs-lookup"><span data-stu-id="03687-124">In cases where a provided [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value isn't recognized by the operating system (OS), it is ignored, and won't cause the API to fail.</span></span> <span data-ttu-id="03687-125">在此情況下，仍會考慮已知的 **DXCoreAdapterPreference** 值。</span><span class="sxs-lookup"><span data-stu-id="03687-125">Known **DXCoreAdapterPreference** values will still be considered in this case.</span></span> <span data-ttu-id="03687-126">若要判斷 API 是否可理解排序類型，請呼叫 [IDXCoreAdapterList：： IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md)。</span><span class="sxs-lookup"><span data-stu-id="03687-126">To determine whether a sort type is understood by the API, call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

<span data-ttu-id="03687-127">稍早在提供的 *喜好* 設定陣列中所發生的 **DXCoreAdapterPreference** 值會被視為較高的優先順序。</span><span class="sxs-lookup"><span data-stu-id="03687-127">**DXCoreAdapterPreference** values that occur earlier in the provided *preferences* array are treated with higher priority.</span></span> 

<span data-ttu-id="03687-128">如需每個類型所套用邏輯的詳細資訊，請參閱 **DXCoreAdapterPreference** 列舉檔。</span><span class="sxs-lookup"><span data-stu-id="03687-128">Refer to the **DXCoreAdapterPreference** enumeration documentation for details about what logic is applied for each type.</span></span> <span data-ttu-id="03687-129">型別的內部邏輯可能會隨著作業系統開發而開發。</span><span class="sxs-lookup"><span data-stu-id="03687-129">The internal logic for a type may develop as the OS develops.</span></span>

<span data-ttu-id="03687-130">當 **排序** 傳回時，DXCore 介面卡清單中的專案會從最慣用到最不理想的順序排序。</span><span class="sxs-lookup"><span data-stu-id="03687-130">When **Sort** returns, items in the DXCore adapter list will have been sorted from most preferable to least preferable.</span></span> <span data-ttu-id="03687-131">因此，以索引0呼叫 [IDXCoreAdapterList：： GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) 會抓取最符合所要求之排序喜好設定類型的介面卡;索引1是下一個最相符的結果，依此類推。</span><span class="sxs-lookup"><span data-stu-id="03687-131">So, calling [IDXCoreAdapterList::GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) with index 0 retrieves the adapter that best matches the requested sort preference types; index 1 is the next best match, and so on.</span></span>

## <a name="see-also"></a><span data-ttu-id="03687-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03687-132">See also</span></span>

<span data-ttu-id="03687-133">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="03687-133">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
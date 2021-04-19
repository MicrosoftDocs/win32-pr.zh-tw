---
title: IDXCoreAdapter::GetPropertySize
description: 針對指定的介面卡屬性，會抓取 [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)呼叫所需的緩衝區大小（以位元組為單位）。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967486"
---
# <a name="idxcoreadaptergetpropertysize-method"></a><span data-ttu-id="fd7b7-103">IDXCoreAdapter：： GetPropertySize 方法</span><span class="sxs-lookup"><span data-stu-id="fd7b7-103">IDXCoreAdapter::GetPropertySize method</span></span>

<span data-ttu-id="fd7b7-104">針對指定的介面卡屬性，會抓取 [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)呼叫所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-104">For a specified adapter property, retrieves the size of buffer, in bytes, that is required for a call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span> <span data-ttu-id="fd7b7-105">在呼叫屬性類型的 **GetPropertySize** 之前，請先呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) ，確認此介面卡與作業系統 (OS) 可使用此屬性類型。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-105">Before calling **GetPropertySize** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7b7-106">語法</span><span class="sxs-lookup"><span data-stu-id="fd7b7-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a><span data-ttu-id="fd7b7-107">參數</span><span class="sxs-lookup"><span data-stu-id="fd7b7-107">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="fd7b7-108">屬性</span><span class="sxs-lookup"><span data-stu-id="fd7b7-108">property</span></span>

<span data-ttu-id="fd7b7-109">類型： **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="fd7b7-109">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="fd7b7-110">您要取得其大小（以位元組為單位）的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-110">The type of the property whose size, in bytes, you wish to retrieve.</span></span>

### <a name="buffersize-out"></a><span data-ttu-id="fd7b7-111">bufferSize [out]</span><span class="sxs-lookup"><span data-stu-id="fd7b7-111">bufferSize [out]</span></span>

<span data-ttu-id="fd7b7-112">類型： **size_t \***</span><span class="sxs-lookup"><span data-stu-id="fd7b7-112">Type: **size_t\***</span></span>

<span data-ttu-id="fd7b7-113">**Size_t** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-113">A pointer to a **size_t** value.</span></span> <span data-ttu-id="fd7b7-114">函式會對指標進行取值，並將值設定為輸出緩衝區的大小（以位元組為單位），您應該在呼叫 [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md)時，將其配置並傳遞為 *propertyData* 引數。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-114">The function dereferences the pointer and sets the value to the size, in bytes, of the output buffer that you should allocate and pass as the *propertyData* argument in your call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

## <a name="returns"></a><span data-ttu-id="fd7b7-115">傳回</span><span class="sxs-lookup"><span data-stu-id="fd7b7-115">Returns</span></span>

<span data-ttu-id="fd7b7-116">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="fd7b7-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="fd7b7-117">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="fd7b7-118">否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="fd7b7-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd7b7-119">Return value</span></span>|<span data-ttu-id="fd7b7-120">描述</span><span class="sxs-lookup"><span data-stu-id="fd7b7-120">Description</span></span>|
|-|-|
|<span data-ttu-id="fd7b7-121">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="fd7b7-121">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="fd7b7-122">此作業系統 (OS) 無法辨識 *屬性* 中指定的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-122">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="fd7b7-123">呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) 確認此介面卡與作業系統 (OS) 可使用此屬性類型。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-123">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="fd7b7-124">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="fd7b7-124">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="fd7b7-125">介面卡不支援 *屬性* 中指定的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-125">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="fd7b7-126">呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) 確認此介面卡與作業系統 (OS) 可使用此屬性類型。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-126">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="fd7b7-127">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="fd7b7-127">E_POINTER</span></span>|<span data-ttu-id="fd7b7-128">`nullptr` 是針對 *bufferSize* 提供的。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-128">`nullptr` was provided for *bufferSize*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fd7b7-129">備註</span><span class="sxs-lookup"><span data-stu-id="fd7b7-129">Remarks</span></span>

<span data-ttu-id="fd7b7-130">您可以在不再有效的介面卡上呼叫 **GetPropertySize** ，函式 &mdash; 將不會失敗。</span><span class="sxs-lookup"><span data-stu-id="fd7b7-130">You can call **GetPropertySize** on an adapter that's no longer valid&mdash;the function won't fail.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd7b7-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd7b7-131">See also</span></span>

<span data-ttu-id="fd7b7-132">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="fd7b7-132">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
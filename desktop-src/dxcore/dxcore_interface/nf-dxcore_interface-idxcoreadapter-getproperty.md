---
title: IDXCoreAdapter::GetProperty
description: 抓取指定之介面卡屬性的值。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c8a7f7b36fdb0128b4047335051823da07a074c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316261"
---
# <a name="idxcoreadaptergetproperty-method"></a><span data-ttu-id="43ff7-103">IDXCoreAdapter：： GetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="43ff7-103">IDXCoreAdapter::GetProperty method</span></span>

<span data-ttu-id="43ff7-104">抓取指定之介面卡屬性的值。</span><span class="sxs-lookup"><span data-stu-id="43ff7-104">Retrieves the value of the specified adapter property.</span></span> <span data-ttu-id="43ff7-105">在呼叫屬性類型的 **GetProperty** 之前，請先呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) ，確認此介面卡與作業系統 (OS) 可使用此屬性類型。</span><span class="sxs-lookup"><span data-stu-id="43ff7-105">Before calling **GetProperty** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span> <span data-ttu-id="43ff7-106">此外，在呼叫 **GetProperty** 之前，請先呼叫 [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) ，以判斷接收屬性值所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="43ff7-106">Also before calling **GetProperty**, call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the necessary size of the buffer in which to receive the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ff7-107">語法</span><span class="sxs-lookup"><span data-stu-id="43ff7-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a><span data-ttu-id="43ff7-108">參數</span><span class="sxs-lookup"><span data-stu-id="43ff7-108">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="43ff7-109">屬性</span><span class="sxs-lookup"><span data-stu-id="43ff7-109">property</span></span>

<span data-ttu-id="43ff7-110">類型： **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="43ff7-110">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="43ff7-111">您要取得其值之屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="43ff7-111">The type of the property whose value you wish to retrieve.</span></span> <span data-ttu-id="43ff7-112">如需每個介面卡屬性的詳細資訊，請參閱 [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) 中的表格。</span><span class="sxs-lookup"><span data-stu-id="43ff7-112">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

### <a name="buffersize"></a><span data-ttu-id="43ff7-113">bufferSize</span><span class="sxs-lookup"><span data-stu-id="43ff7-113">bufferSize</span></span>

<span data-ttu-id="43ff7-114">類型： **size_t**</span><span class="sxs-lookup"><span data-stu-id="43ff7-114">Type: **size_t**</span></span>

<span data-ttu-id="43ff7-115">您在 *propertyData* 中配置並提供之輸出緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="43ff7-115">The size, in bytes, of the output buffer that you allocate and provide in *propertyData*.</span></span>

### <a name="propertydata-out"></a><span data-ttu-id="43ff7-116">propertyData [out]</span><span class="sxs-lookup"><span data-stu-id="43ff7-116">propertyData [out]</span></span>

<span data-ttu-id="43ff7-117">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="43ff7-117">Type: **void\***</span></span>

<span data-ttu-id="43ff7-118">您在應用程式中配置的輸出緩衝區指標，且該函式會填入。</span><span class="sxs-lookup"><span data-stu-id="43ff7-118">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="43ff7-119">呼叫 [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) 來判斷 *propertyData* 緩衝區應針對指定介面卡屬性的大小。</span><span class="sxs-lookup"><span data-stu-id="43ff7-119">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="43ff7-120">傳回</span><span class="sxs-lookup"><span data-stu-id="43ff7-120">Returns</span></span>

<span data-ttu-id="43ff7-121">類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="43ff7-121">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="43ff7-122">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="43ff7-122">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="43ff7-123">否則，它會傳回 [**HRESULT**](../../com/structure-of-com-error-codes.md) [錯誤碼](../../com/com-error-codes-10.md)。</span><span class="sxs-lookup"><span data-stu-id="43ff7-123">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="43ff7-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="43ff7-124">Return value</span></span>|<span data-ttu-id="43ff7-125">描述</span><span class="sxs-lookup"><span data-stu-id="43ff7-125">Description</span></span>|
|-|-|
|<span data-ttu-id="43ff7-126">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="43ff7-126">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="43ff7-127">此作業系統 (OS) 無法辨識 *屬性* 中指定的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="43ff7-127">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="43ff7-128">呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) 確認此介面卡與作業系統 (OS) 可使用此屬性類型。</span><span class="sxs-lookup"><span data-stu-id="43ff7-128">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="43ff7-129">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="43ff7-129">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="43ff7-130">介面卡不支援 *屬性* 中指定的屬性類型。</span><span class="sxs-lookup"><span data-stu-id="43ff7-130">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="43ff7-131">呼叫 [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) 確認此介面卡與作業系統 (OS) 可使用此屬性類型。</span><span class="sxs-lookup"><span data-stu-id="43ff7-131">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="43ff7-132">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="43ff7-132">E_INVALIDARG</span></span>|<span data-ttu-id="43ff7-133">*PropertyData* 中提供的緩衝區大小不足。</span><span class="sxs-lookup"><span data-stu-id="43ff7-133">An insufficient buffer size is provided in *propertyData*.</span></span> <span data-ttu-id="43ff7-134">呼叫 [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) 來判斷 *propertyData* 緩衝區應針對指定介面卡屬性的大小。</span><span class="sxs-lookup"><span data-stu-id="43ff7-134">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>|
|<span data-ttu-id="43ff7-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="43ff7-135">E_POINTER</span></span>|<span data-ttu-id="43ff7-136">`nullptr` 是為 *propertyData* 所提供。</span><span class="sxs-lookup"><span data-stu-id="43ff7-136">`nullptr` was provided for *propertyData*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="43ff7-137">備註</span><span class="sxs-lookup"><span data-stu-id="43ff7-137">Remarks</span></span>

<span data-ttu-id="43ff7-138">您可以在不再有效的介面卡上呼叫 **GetProperty** ， &mdash; 因為這樣會導致該函式無法運作。</span><span class="sxs-lookup"><span data-stu-id="43ff7-138">You can call **GetProperty** on an adapter that's no longer valid&mdash;the function won't fail as a result of that.</span></span> <span data-ttu-id="43ff7-139">在填入之前，此函式會將 *propertyData* 緩衝區設為零。</span><span class="sxs-lookup"><span data-stu-id="43ff7-139">This function zeros out the *propertyData* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="43ff7-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43ff7-140">See also</span></span>

<span data-ttu-id="43ff7-141">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="43ff7-141">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
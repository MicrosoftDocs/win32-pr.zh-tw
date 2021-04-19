---
description: GetBufferFromIPortableDeviceValues 方法會將提交的 IPortableDeviceValues 介面序列化為配置的位元組陣列。 傳回的位元組陣列是針對呼叫端配置的，而且應該由呼叫端使用 CoTaskMemFree 來釋放。
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'IWpdSerializer：： GetBufferFromIPortableDeviceValues 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44f4e9e7011e6a4766183307e81ef7e783da899f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000667"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a><span data-ttu-id="f16dd-104">IWpdSerializer：： GetBufferFromIPortableDeviceValues 方法</span><span class="sxs-lookup"><span data-stu-id="f16dd-104">IWpdSerializer::GetBufferFromIPortableDeviceValues method</span></span>

<span data-ttu-id="f16dd-105">**GetBufferFromIPortableDeviceValues** 方法會將提交的 **IPortableDeviceValues** 介面序列化為配置的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="f16dd-105">The **GetBufferFromIPortableDeviceValues** method serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span> <span data-ttu-id="f16dd-106">傳回的位元組陣列是針對呼叫端配置的，而且應該由呼叫端使用 **CoTaskMemFree** 來釋放。</span><span class="sxs-lookup"><span data-stu-id="f16dd-106">The byte array returned is allocated for the caller and should be freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16dd-107">語法</span><span class="sxs-lookup"><span data-stu-id="f16dd-107">Syntax</span></span>


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="f16dd-108">參數</span><span class="sxs-lookup"><span data-stu-id="f16dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f16dd-109">*pSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f16dd-109">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f16dd-110">要序列化之 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f16dd-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="f16dd-111">*ppBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f16dd-111">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f16dd-112">\*\*位元組 \* \*_ 的指標，其中包含已序列化的資料。Windows 可攜式裝置配置此記憶體;呼叫者必須藉由呼叫 _ CoTaskMemFree 來釋放它\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="f16dd-112">Pointer to a \**BYTE\**_ that contains the serialized data. Windows Portable Devices allocates this memory; the caller must free it by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="f16dd-113">*pdwBufferSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f16dd-113">*pdwBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f16dd-114">**DWORD** 的指標，指定配置的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f16dd-114">Pointer to a **DWORD** that specifies the size of allocated buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f16dd-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f16dd-115">Return value</span></span>

<span data-ttu-id="f16dd-116">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f16dd-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f16dd-117">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f16dd-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f16dd-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f16dd-118">Return code</span></span>                                                                                   | <span data-ttu-id="f16dd-119">Description</span><span class="sxs-lookup"><span data-stu-id="f16dd-119">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f16dd-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f16dd-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f16dd-121">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f16dd-121">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="f16dd-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f16dd-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f16dd-123">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f16dd-123">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="f16dd-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f16dd-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f16dd-125">沒有足夠的記憶體可用來建立緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f16dd-125">There was not enough memory available to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f16dd-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f16dd-126">Requirements</span></span>



| <span data-ttu-id="f16dd-127">需求</span><span class="sxs-lookup"><span data-stu-id="f16dd-127">Requirement</span></span> | <span data-ttu-id="f16dd-128">值</span><span class="sxs-lookup"><span data-stu-id="f16dd-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f16dd-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f16dd-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f16dd-130"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="f16dd-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f16dd-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="f16dd-131">Library</span></span><br/> | <dl> <span data-ttu-id="f16dd-132"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f16dd-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16dd-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f16dd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16dd-134">**IWpdSerializer 介面**</span><span class="sxs-lookup"><span data-stu-id="f16dd-134">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 





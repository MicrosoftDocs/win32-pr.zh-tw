---
description: WriteIPortableDeviceValuesToBuffer 方法會將 IPortableDeviceValues 介面序列化為呼叫端配置的位元組陣列。
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'IWpdSerializer：： WriteIPortableDeviceValuesToBuffer 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986147"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a><span data-ttu-id="6522b-103">IWpdSerializer：： WriteIPortableDeviceValuesToBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="6522b-103">IWpdSerializer::WriteIPortableDeviceValuesToBuffer method</span></span>

<span data-ttu-id="6522b-104">**WriteIPortableDeviceValuesToBuffer** 方法會將 **IPortableDeviceValues** 介面序列化為呼叫端配置的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="6522b-104">The **WriteIPortableDeviceValuesToBuffer** method serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="6522b-105">語法</span><span class="sxs-lookup"><span data-stu-id="6522b-105">Syntax</span></span>


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a><span data-ttu-id="6522b-106">參數</span><span class="sxs-lookup"><span data-stu-id="6522b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6522b-107">*dwOutputBufferLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6522b-107">*dwOutputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6522b-108">指定 *pBuffer* 大小的 **DWORD** （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6522b-108">**DWORD** that specifies the size of *pBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6522b-109">*pResults* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6522b-109">*pResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6522b-110">要序列化之 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6522b-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="6522b-111">*pBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6522b-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6522b-112">呼叫端配置之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="6522b-112">Pointer to a caller-allocated buffer.</span></span> <span data-ttu-id="6522b-113">若要瞭解所需的緩衝區大小，請呼叫 **GetSerializedSize**。</span><span class="sxs-lookup"><span data-stu-id="6522b-113">To learn the size of the required buffer, call **GetSerializedSize**.</span></span>

</dd> <dt>

<span data-ttu-id="6522b-114">*pdwBytesWritten* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6522b-114">*pdwBytesWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6522b-115">**DWORD** 的指標，指出實際寫入至呼叫端配置之緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="6522b-115">Pointer to a **DWORD** that indicates the number of bytes that was actually written to the caller-allocated buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6522b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6522b-116">Return value</span></span>

<span data-ttu-id="6522b-117">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="6522b-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6522b-118">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="6522b-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6522b-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6522b-119">Return code</span></span>                                                                                   | <span data-ttu-id="6522b-120">Description</span><span class="sxs-lookup"><span data-stu-id="6522b-120">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="6522b-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6522b-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6522b-122">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="6522b-122">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="6522b-123"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="6522b-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6522b-124">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6522b-124">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="6522b-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6522b-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6522b-126">呼叫端提供的緩衝區不夠大。</span><span class="sxs-lookup"><span data-stu-id="6522b-126">The caller-provided buffer was not big enough.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6522b-127">備註</span><span class="sxs-lookup"><span data-stu-id="6522b-127">Remarks</span></span>

<span data-ttu-id="6522b-128">這個方法會將 **IPortableDeviceValues** 介面複製到現有的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6522b-128">This method copies an **IPortableDeviceValues** interface into an existing buffer.</span></span> <span data-ttu-id="6522b-129">如果您想要配置新的緩衝區，請使用 [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md)。</span><span class="sxs-lookup"><span data-stu-id="6522b-129">If you want to allocate a new buffer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6522b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="6522b-130">Requirements</span></span>



| <span data-ttu-id="6522b-131">需求</span><span class="sxs-lookup"><span data-stu-id="6522b-131">Requirement</span></span> | <span data-ttu-id="6522b-132">值</span><span class="sxs-lookup"><span data-stu-id="6522b-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6522b-133">標頭</span><span class="sxs-lookup"><span data-stu-id="6522b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="6522b-134"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="6522b-134"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6522b-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="6522b-135">Library</span></span><br/> | <dl> <span data-ttu-id="6522b-136"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6522b-136"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6522b-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6522b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6522b-138">**IWpdSerializer 介面**</span><span class="sxs-lookup"><span data-stu-id="6522b-138">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 





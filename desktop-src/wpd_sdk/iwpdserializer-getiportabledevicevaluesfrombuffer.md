---
description: GetIPortableDeviceValuesFromBuffer 方法會將位元組陣列還原序列化為 IPortableDeviceValues 介面。
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'IWpdSerializer：： GetIPortableDeviceValuesFromBuffer 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999990"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a><span data-ttu-id="4fe17-103">IWpdSerializer：： GetIPortableDeviceValuesFromBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="4fe17-103">IWpdSerializer::GetIPortableDeviceValuesFromBuffer method</span></span>

<span data-ttu-id="4fe17-104">**GetIPortableDeviceValuesFromBuffer** 方法會將位元組陣列還原序列化為 **IPortableDeviceValues** 介面。</span><span class="sxs-lookup"><span data-stu-id="4fe17-104">The **GetIPortableDeviceValuesFromBuffer** method deserializes a byte array to an **IPortableDeviceValues** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fe17-105">語法</span><span class="sxs-lookup"><span data-stu-id="4fe17-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a><span data-ttu-id="4fe17-106">參數</span><span class="sxs-lookup"><span data-stu-id="4fe17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fe17-107">*pBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4fe17-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe17-108">要還原序列化的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="4fe17-108">Pointer to the buffer to deserialize.</span></span>

</dd> <dt>

<span data-ttu-id="4fe17-109">*dwInputBufferLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4fe17-109">*dwInputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe17-110">指定緩衝區大小的 **DWORD** （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4fe17-110">**DWORD** that specifies the size of the buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4fe17-111">*ppParams* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4fe17-111">*ppParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe17-112">變數的位址，此變數會接收從緩衝區建立之 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4fe17-112">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface created from the buffer.</span></span> <span data-ttu-id="4fe17-113">應用程式會負責在介面上呼叫 **Release** 。</span><span class="sxs-lookup"><span data-stu-id="4fe17-113">The application is responsible for calling **Release** on the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fe17-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="4fe17-114">Return value</span></span>

<span data-ttu-id="4fe17-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="4fe17-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4fe17-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="4fe17-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4fe17-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4fe17-117">Return code</span></span>                                                                                  | <span data-ttu-id="4fe17-118">Description</span><span class="sxs-lookup"><span data-stu-id="4fe17-118">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="4fe17-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe17-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4fe17-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="4fe17-120">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="4fe17-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe17-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="4fe17-122">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4fe17-122">A required pointer argument was **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="4fe17-123"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe17-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="4fe17-124">發生未指定的轉換錯誤。</span><span class="sxs-lookup"><span data-stu-id="4fe17-124">An unspecified conversion error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4fe17-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fe17-125">Requirements</span></span>



| <span data-ttu-id="4fe17-126">需求</span><span class="sxs-lookup"><span data-stu-id="4fe17-126">Requirement</span></span> | <span data-ttu-id="4fe17-127">值</span><span class="sxs-lookup"><span data-stu-id="4fe17-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe17-128">標頭</span><span class="sxs-lookup"><span data-stu-id="4fe17-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4fe17-129"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="4fe17-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fe17-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="4fe17-130">Library</span></span><br/> | <dl> <span data-ttu-id="4fe17-131"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fe17-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fe17-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fe17-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe17-133">**IWpdSerializer 介面**</span><span class="sxs-lookup"><span data-stu-id="4fe17-133">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 





---
description: GetSerializedSize 方法會計算保存序列化 IPortableDeviceValues 介面所需的緩衝區大小。
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'IWpdSerializer：： GetSerializedSize 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7b50f7f6158145cd71125b5e5f26649712bb065b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000666"
---
# <a name="iwpdserializergetserializedsize-method"></a><span data-ttu-id="6249f-103">IWpdSerializer：： GetSerializedSize 方法</span><span class="sxs-lookup"><span data-stu-id="6249f-103">IWpdSerializer::GetSerializedSize method</span></span>

<span data-ttu-id="6249f-104">**GetSerializedSize** 方法會計算保存序列化 [**IPortableDeviceValues**](iportabledevicevalues.md)介面所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="6249f-104">The **GetSerializedSize** method calculates the buffer size that is required to hold a serialized [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6249f-105">語法</span><span class="sxs-lookup"><span data-stu-id="6249f-105">Syntax</span></span>


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="6249f-106">參數</span><span class="sxs-lookup"><span data-stu-id="6249f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6249f-107">*pSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6249f-107">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6249f-108">要要求其大小之 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6249f-108">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface whose size you want to request.</span></span>

</dd> <dt>

<span data-ttu-id="6249f-109">*pdwSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6249f-109">*pdwSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6249f-110">**DWORD** 的指標，指出序列化 *pSource* 所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6249f-110">Pointer to a **DWORD** that indicates the buffer size that is required to serialize *pSource*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6249f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6249f-111">Return value</span></span>

<span data-ttu-id="6249f-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="6249f-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6249f-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="6249f-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6249f-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6249f-114">Return code</span></span>                                                                                   | <span data-ttu-id="6249f-115">Description</span><span class="sxs-lookup"><span data-stu-id="6249f-115">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6249f-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6249f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6249f-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="6249f-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="6249f-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="6249f-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6249f-119">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6249f-119">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="6249f-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6249f-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6249f-121">沒有足夠的可用記憶體來建立緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6249f-121">There was not enough available memory to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6249f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6249f-122">Requirements</span></span>



| <span data-ttu-id="6249f-123">需求</span><span class="sxs-lookup"><span data-stu-id="6249f-123">Requirement</span></span> | <span data-ttu-id="6249f-124">值</span><span class="sxs-lookup"><span data-stu-id="6249f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6249f-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6249f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6249f-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="6249f-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6249f-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="6249f-127">Library</span></span><br/> | <dl> <span data-ttu-id="6249f-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6249f-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6249f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6249f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6249f-130">**IWpdSerializer 介面**</span><span class="sxs-lookup"><span data-stu-id="6249f-130">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 





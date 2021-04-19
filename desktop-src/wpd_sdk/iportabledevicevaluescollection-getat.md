---
description: GetAt 方法會依據以零為基底的索引，從集合中抓取專案。
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'IPortableDeviceValuesCollection：： GetAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ffbc65f39aab63189aa451005008f585c46bd8d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995911"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a><span data-ttu-id="161d7-103">IPortableDeviceValuesCollection：： GetAt 方法</span><span class="sxs-lookup"><span data-stu-id="161d7-103">IPortableDeviceValuesCollection::GetAt method</span></span>

<span data-ttu-id="161d7-104">**GetAt** 方法會依據以零為基底的索引，從集合中抓取專案。</span><span class="sxs-lookup"><span data-stu-id="161d7-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="161d7-105">語法</span><span class="sxs-lookup"><span data-stu-id="161d7-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a><span data-ttu-id="161d7-106">參數</span><span class="sxs-lookup"><span data-stu-id="161d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="161d7-107">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="161d7-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="161d7-108">**DWORD** ，指定集合中以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="161d7-108">**DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="161d7-109">*ppValues* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="161d7-109">*ppValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="161d7-110">從集合接收 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="161d7-110">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface from the collection.</span></span> <span data-ttu-id="161d7-111">當呼叫端完成時，呼叫端會負責呼叫此介面上的 **釋放** 。</span><span class="sxs-lookup"><span data-stu-id="161d7-111">The caller is responsible for calling **Release** on this interface when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="161d7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="161d7-112">Return value</span></span>

<span data-ttu-id="161d7-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="161d7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="161d7-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="161d7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="161d7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="161d7-115">Return code</span></span>                                                                                  | <span data-ttu-id="161d7-116">Description</span><span class="sxs-lookup"><span data-stu-id="161d7-116">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="161d7-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="161d7-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="161d7-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="161d7-118">The method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="161d7-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="161d7-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="161d7-120">傳入的以零為基底的索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="161d7-120">The zero-based index that was passed in was out of range.</span></span><br/>             |
| <dl> <span data-ttu-id="161d7-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="161d7-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="161d7-122">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="161d7-122">A required pointer argument was **NULL**.</span></span><br/>                             |
| <dl> <span data-ttu-id="161d7-123"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="161d7-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="161d7-124">集合包含 **Null** **IPortableDeviceValues** 指標。</span><span class="sxs-lookup"><span data-stu-id="161d7-124">The collection contains a **NULL** **IPortableDeviceValues** pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="161d7-125">備註</span><span class="sxs-lookup"><span data-stu-id="161d7-125">Remarks</span></span>

<span data-ttu-id="161d7-126">對已抓取介面中的值所做的任何變更，都會對儲存在集合中的版本進行。</span><span class="sxs-lookup"><span data-stu-id="161d7-126">Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="161d7-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="161d7-127">Requirements</span></span>



| <span data-ttu-id="161d7-128">需求</span><span class="sxs-lookup"><span data-stu-id="161d7-128">Requirement</span></span> | <span data-ttu-id="161d7-129">值</span><span class="sxs-lookup"><span data-stu-id="161d7-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="161d7-130">標頭</span><span class="sxs-lookup"><span data-stu-id="161d7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="161d7-131"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="161d7-131"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="161d7-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="161d7-132">Library</span></span><br/> | <dl> <span data-ttu-id="161d7-133"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="161d7-133"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="161d7-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="161d7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="161d7-135">**IPortableDeviceValuesCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="161d7-135">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 





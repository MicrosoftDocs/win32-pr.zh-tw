---
description: IPortableDeviceValuesCollection：： GetAt 方法-GetAt 方法會依據以零為基底的索引，從集合中抓取專案。
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
ms.openlocfilehash: 2ad10a7b9cc3c252a0cee4cb71df05cb108e0a18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083251"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a><span data-ttu-id="f79f6-103">IPortableDeviceValuesCollection：： GetAt 方法</span><span class="sxs-lookup"><span data-stu-id="f79f6-103">IPortableDeviceValuesCollection::GetAt method</span></span>

<span data-ttu-id="f79f6-104">**GetAt** 方法會依據以零為基底的索引，從集合中抓取專案。</span><span class="sxs-lookup"><span data-stu-id="f79f6-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f79f6-105">語法</span><span class="sxs-lookup"><span data-stu-id="f79f6-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a><span data-ttu-id="f79f6-106">參數</span><span class="sxs-lookup"><span data-stu-id="f79f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f79f6-107">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f79f6-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f79f6-108">**DWORD** ，指定集合中以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="f79f6-108">**DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="f79f6-109">*ppValues* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f79f6-109">*ppValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f79f6-110">從集合接收 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="f79f6-110">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface from the collection.</span></span> <span data-ttu-id="f79f6-111">當呼叫端完成時，呼叫端會負責呼叫此介面上的 **釋放** 。</span><span class="sxs-lookup"><span data-stu-id="f79f6-111">The caller is responsible for calling **Release** on this interface when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f79f6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f79f6-112">Return value</span></span>

<span data-ttu-id="f79f6-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f79f6-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f79f6-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f79f6-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f79f6-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f79f6-115">Return code</span></span>                                                                                  | <span data-ttu-id="f79f6-116">Description</span><span class="sxs-lookup"><span data-stu-id="f79f6-116">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f79f6-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f79f6-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f79f6-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f79f6-118">The method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="f79f6-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f79f6-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f79f6-120">傳入的以零為基底的索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="f79f6-120">The zero-based index that was passed in was out of range.</span></span><br/>             |
| <dl> <span data-ttu-id="f79f6-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f79f6-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="f79f6-122">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f79f6-122">A required pointer argument was **NULL**.</span></span><br/>                             |
| <dl> <span data-ttu-id="f79f6-123"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="f79f6-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="f79f6-124">集合包含 **Null** **IPortableDeviceValues** 指標。</span><span class="sxs-lookup"><span data-stu-id="f79f6-124">The collection contains a **NULL** **IPortableDeviceValues** pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f79f6-125">備註</span><span class="sxs-lookup"><span data-stu-id="f79f6-125">Remarks</span></span>

<span data-ttu-id="f79f6-126">對已抓取介面中的值所做的任何變更，都會對儲存在集合中的版本進行。</span><span class="sxs-lookup"><span data-stu-id="f79f6-126">Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f79f6-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f79f6-127">Requirements</span></span>



| <span data-ttu-id="f79f6-128">需求</span><span class="sxs-lookup"><span data-stu-id="f79f6-128">Requirement</span></span> | <span data-ttu-id="f79f6-129">值</span><span class="sxs-lookup"><span data-stu-id="f79f6-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f79f6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f79f6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f79f6-131"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="f79f6-131"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f79f6-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="f79f6-132">Library</span></span><br/> | <dl> <span data-ttu-id="f79f6-133"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f79f6-133"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f79f6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f79f6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79f6-135">**IPortableDeviceValuesCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="f79f6-135">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 





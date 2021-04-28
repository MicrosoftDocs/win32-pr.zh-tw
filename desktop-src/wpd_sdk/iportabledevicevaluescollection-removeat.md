---
description: IPortableDeviceValuesCollection：： RemoveAt 方法-RemoveAt 方法會移除儲存在指定索引所指定之位置的元素。
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: 'IPortableDeviceValuesCollection：： RemoveAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7db15480906bee8181bb0fc589c4f3e30ce4753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083166"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a><span data-ttu-id="5c1c6-103">IPortableDeviceValuesCollection：： RemoveAt 方法</span><span class="sxs-lookup"><span data-stu-id="5c1c6-103">IPortableDeviceValuesCollection::RemoveAt method</span></span>

<span data-ttu-id="5c1c6-104">**RemoveAt** 方法會移除儲存在指定索引所指定之位置的元素。</span><span class="sxs-lookup"><span data-stu-id="5c1c6-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c1c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="5c1c6-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="5c1c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="5c1c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c1c6-107">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c1c6-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c1c6-108">指定要移除之元素的索引。</span><span class="sxs-lookup"><span data-stu-id="5c1c6-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c1c6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c1c6-109">Return value</span></span>

<span data-ttu-id="5c1c6-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="5c1c6-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5c1c6-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="5c1c6-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5c1c6-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5c1c6-112">Return code</span></span>                                                                                  | <span data-ttu-id="5c1c6-113">Description</span><span class="sxs-lookup"><span data-stu-id="5c1c6-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="5c1c6-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5c1c6-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5c1c6-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="5c1c6-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="5c1c6-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5c1c6-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5c1c6-117">指定的索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="5c1c6-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c1c6-118">備註</span><span class="sxs-lookup"><span data-stu-id="5c1c6-118">Remarks</span></span>

<span data-ttu-id="5c1c6-119">您必須指定以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="5c1c6-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c1c6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c1c6-120">Requirements</span></span>



| <span data-ttu-id="5c1c6-121">需求</span><span class="sxs-lookup"><span data-stu-id="5c1c6-121">Requirement</span></span> | <span data-ttu-id="5c1c6-122">值</span><span class="sxs-lookup"><span data-stu-id="5c1c6-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c1c6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5c1c6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5c1c6-124"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c1c6-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c1c6-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="5c1c6-125">Library</span></span><br/> | <dl> <span data-ttu-id="5c1c6-126"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c1c6-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c1c6-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c1c6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c1c6-128">**IPortableDeviceValuesCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="5c1c6-128">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 





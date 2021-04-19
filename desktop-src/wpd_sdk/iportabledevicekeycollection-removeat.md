---
description: RemoveAt 方法會移除儲存在指定索引所指定之位置的元素。
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: 'IPortableDeviceKeyCollection：： RemoveAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f4e126ef5fcad74b7cee5f748322f15e75481e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995458"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a><span data-ttu-id="84a90-103">IPortableDeviceKeyCollection：： RemoveAt 方法</span><span class="sxs-lookup"><span data-stu-id="84a90-103">IPortableDeviceKeyCollection::RemoveAt method</span></span>

<span data-ttu-id="84a90-104">**RemoveAt** 方法會移除儲存在指定索引所指定之位置的元素。</span><span class="sxs-lookup"><span data-stu-id="84a90-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a90-105">語法</span><span class="sxs-lookup"><span data-stu-id="84a90-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="84a90-106">參數</span><span class="sxs-lookup"><span data-stu-id="84a90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84a90-107">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84a90-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84a90-108">指定要移除之元素的索引。</span><span class="sxs-lookup"><span data-stu-id="84a90-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84a90-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="84a90-109">Return value</span></span>

<span data-ttu-id="84a90-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="84a90-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="84a90-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="84a90-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="84a90-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="84a90-112">Return code</span></span>                                                                                  | <span data-ttu-id="84a90-113">Description</span><span class="sxs-lookup"><span data-stu-id="84a90-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="84a90-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="84a90-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="84a90-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="84a90-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="84a90-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="84a90-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="84a90-117">指定的索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="84a90-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="84a90-118">備註</span><span class="sxs-lookup"><span data-stu-id="84a90-118">Remarks</span></span>

<span data-ttu-id="84a90-119">您必須指定以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="84a90-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="84a90-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="84a90-120">Requirements</span></span>



| <span data-ttu-id="84a90-121">需求</span><span class="sxs-lookup"><span data-stu-id="84a90-121">Requirement</span></span> | <span data-ttu-id="84a90-122">值</span><span class="sxs-lookup"><span data-stu-id="84a90-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a90-123">標頭</span><span class="sxs-lookup"><span data-stu-id="84a90-123">Header</span></span><br/>  | <dl> <span data-ttu-id="84a90-124"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="84a90-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="84a90-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="84a90-125">Library</span></span><br/> | <dl> <span data-ttu-id="84a90-126"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="84a90-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84a90-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84a90-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a90-128">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="84a90-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> </dl>

 

 





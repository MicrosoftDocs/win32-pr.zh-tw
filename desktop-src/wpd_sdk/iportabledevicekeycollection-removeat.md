---
description: IPortableDeviceKeyCollection：： RemoveAt 方法-RemoveAt 方法會移除儲存在指定索引所指定之位置的元素。
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
ms.openlocfilehash: 3ec2b1137e7959a646c2943ab1aa7a5c3428d3c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109938"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a><span data-ttu-id="1c6fe-103">IPortableDeviceKeyCollection：： RemoveAt 方法</span><span class="sxs-lookup"><span data-stu-id="1c6fe-103">IPortableDeviceKeyCollection::RemoveAt method</span></span>

<span data-ttu-id="1c6fe-104">**RemoveAt** 方法會移除儲存在指定索引所指定之位置的元素。</span><span class="sxs-lookup"><span data-stu-id="1c6fe-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c6fe-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c6fe-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="1c6fe-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c6fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c6fe-107">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c6fe-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c6fe-108">指定要移除之元素的索引。</span><span class="sxs-lookup"><span data-stu-id="1c6fe-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c6fe-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c6fe-109">Return value</span></span>

<span data-ttu-id="1c6fe-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="1c6fe-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1c6fe-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="1c6fe-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1c6fe-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1c6fe-112">Return code</span></span>                                                                                  | <span data-ttu-id="1c6fe-113">Description</span><span class="sxs-lookup"><span data-stu-id="1c6fe-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="1c6fe-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1c6fe-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1c6fe-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="1c6fe-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="1c6fe-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1c6fe-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1c6fe-117">指定的索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="1c6fe-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c6fe-118">備註</span><span class="sxs-lookup"><span data-stu-id="1c6fe-118">Remarks</span></span>

<span data-ttu-id="1c6fe-119">您必須指定以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="1c6fe-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c6fe-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c6fe-120">Requirements</span></span>



| <span data-ttu-id="1c6fe-121">需求</span><span class="sxs-lookup"><span data-stu-id="1c6fe-121">Requirement</span></span> | <span data-ttu-id="1c6fe-122">值</span><span class="sxs-lookup"><span data-stu-id="1c6fe-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6fe-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1c6fe-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1c6fe-124"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c6fe-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c6fe-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="1c6fe-125">Library</span></span><br/> | <dl> <span data-ttu-id="1c6fe-126"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c6fe-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c6fe-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c6fe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6fe-128">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="1c6fe-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> </dl>

 

 





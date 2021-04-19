---
description: RemoveAt 方法會移除儲存在指定索引所指定之位置的元素。
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'IPortableDevicePropVariantCollection：： RemoveAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 74c7900340caab6adfda1b4607df607a4f6f0811
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989521"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a><span data-ttu-id="1ce55-103">IPortableDevicePropVariantCollection：： RemoveAt 方法</span><span class="sxs-lookup"><span data-stu-id="1ce55-103">IPortableDevicePropVariantCollection::RemoveAt method</span></span>

<span data-ttu-id="1ce55-104">**RemoveAt** 方法會移除儲存在指定索引所指定之位置的元素。</span><span class="sxs-lookup"><span data-stu-id="1ce55-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ce55-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ce55-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="1ce55-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ce55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ce55-107">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1ce55-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ce55-108">指定要移除之元素的索引。</span><span class="sxs-lookup"><span data-stu-id="1ce55-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ce55-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ce55-109">Return value</span></span>

<span data-ttu-id="1ce55-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="1ce55-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1ce55-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="1ce55-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1ce55-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1ce55-112">Return code</span></span>                                                                                  | <span data-ttu-id="1ce55-113">Description</span><span class="sxs-lookup"><span data-stu-id="1ce55-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="1ce55-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1ce55-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1ce55-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="1ce55-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="1ce55-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1ce55-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1ce55-117">指定的索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="1ce55-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ce55-118">備註</span><span class="sxs-lookup"><span data-stu-id="1ce55-118">Remarks</span></span>

<span data-ttu-id="1ce55-119">您必須指定以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="1ce55-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce55-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ce55-120">Requirements</span></span>



| <span data-ttu-id="1ce55-121">需求</span><span class="sxs-lookup"><span data-stu-id="1ce55-121">Requirement</span></span> | <span data-ttu-id="1ce55-122">值</span><span class="sxs-lookup"><span data-stu-id="1ce55-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce55-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1ce55-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1ce55-124"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ce55-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ce55-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ce55-125">Library</span></span><br/> | <dl> <span data-ttu-id="1ce55-126"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ce55-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ce55-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ce55-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce55-128">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="1ce55-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 





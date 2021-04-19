---
description: GetType 方法會抓取集合中專案的資料類型。
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'IPortableDevicePropVariantCollection：： GetType 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982957"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a><span data-ttu-id="15452-103">IPortableDevicePropVariantCollection：： GetType 方法</span><span class="sxs-lookup"><span data-stu-id="15452-103">IPortableDevicePropVariantCollection::GetType method</span></span>

<span data-ttu-id="15452-104">**GetType** 方法會抓取集合中專案的資料類型。</span><span class="sxs-lookup"><span data-stu-id="15452-104">The **GetType** method retrieves the data type of the items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="15452-105">語法</span><span class="sxs-lookup"><span data-stu-id="15452-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a><span data-ttu-id="15452-106">參數</span><span class="sxs-lookup"><span data-stu-id="15452-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15452-107">*pvt* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="15452-107">*pvt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15452-108">Platform SDK **VARTYPE** 列舉值，指出集合中所有專案的資料類型。</span><span class="sxs-lookup"><span data-stu-id="15452-108">A Platform SDK **VARTYPE** enumeration value that indicates the data type of all the items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15452-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="15452-109">Return value</span></span>

<span data-ttu-id="15452-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="15452-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="15452-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="15452-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="15452-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="15452-112">Return code</span></span>                                                                               | <span data-ttu-id="15452-113">Description</span><span class="sxs-lookup"><span data-stu-id="15452-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="15452-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="15452-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="15452-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="15452-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="15452-116"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="15452-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="15452-117">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="15452-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="15452-118">備註</span><span class="sxs-lookup"><span data-stu-id="15452-118">Remarks</span></span>

<span data-ttu-id="15452-119">儲存在 **IPortableDevicePropVariantCollection** 中的所有專案都是相同的類型。</span><span class="sxs-lookup"><span data-stu-id="15452-119">All items that are stored in an **IPortableDevicePropVariantCollection** are the same type.</span></span>

## <a name="requirements"></a><span data-ttu-id="15452-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="15452-120">Requirements</span></span>



| <span data-ttu-id="15452-121">需求</span><span class="sxs-lookup"><span data-stu-id="15452-121">Requirement</span></span> | <span data-ttu-id="15452-122">值</span><span class="sxs-lookup"><span data-stu-id="15452-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15452-123">標頭</span><span class="sxs-lookup"><span data-stu-id="15452-123">Header</span></span><br/>  | <dl> <span data-ttu-id="15452-124"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="15452-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="15452-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="15452-125">Library</span></span><br/> | <dl> <span data-ttu-id="15452-126"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="15452-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15452-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15452-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15452-128">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="15452-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 





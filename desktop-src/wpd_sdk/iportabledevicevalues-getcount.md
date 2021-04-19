---
description: GetCount 方法會抓取集合中的專案數。
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: 'IPortableDeviceValues：： GetCount 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 710348b2f2626d39efcbdf68373d1e556ecc335c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983220"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="d7f15-103">IPortableDeviceValues：： GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="d7f15-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="d7f15-104">**GetCount** 方法會抓取集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="d7f15-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f15-105">語法</span><span class="sxs-lookup"><span data-stu-id="d7f15-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="d7f15-106">參數</span><span class="sxs-lookup"><span data-stu-id="d7f15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f15-107">*pcelt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d7f15-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f15-108">**DWORD** 的指標，其中包含集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="d7f15-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f15-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7f15-109">Return value</span></span>

<span data-ttu-id="d7f15-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d7f15-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d7f15-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d7f15-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d7f15-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d7f15-112">Return code</span></span>                                                                          | <span data-ttu-id="d7f15-113">Description</span><span class="sxs-lookup"><span data-stu-id="d7f15-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d7f15-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f15-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d7f15-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d7f15-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d7f15-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7f15-116">Requirements</span></span>



| <span data-ttu-id="d7f15-117">需求</span><span class="sxs-lookup"><span data-stu-id="d7f15-117">Requirement</span></span> | <span data-ttu-id="d7f15-118">值</span><span class="sxs-lookup"><span data-stu-id="d7f15-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f15-119">標頭</span><span class="sxs-lookup"><span data-stu-id="d7f15-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d7f15-120"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f15-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7f15-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="d7f15-121">Library</span></span><br/> | <dl> <span data-ttu-id="d7f15-122"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7f15-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f15-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7f15-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f15-124">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="d7f15-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 





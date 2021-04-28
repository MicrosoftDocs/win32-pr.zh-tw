---
description: IPortableDeviceValuesCollection：： GetCount 方法-GetCount 方法會抓取集合中的專案數。
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: 'IPortableDeviceValuesCollection：： GetCount 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8304184f3323feb92a14b523dc629c6ae45f6a85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083176"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a><span data-ttu-id="5aa57-103">IPortableDeviceValuesCollection：： GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="5aa57-103">IPortableDeviceValuesCollection::GetCount method</span></span>

<span data-ttu-id="5aa57-104">**GetCount** 方法會抓取集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="5aa57-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa57-105">語法</span><span class="sxs-lookup"><span data-stu-id="5aa57-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="5aa57-106">參數</span><span class="sxs-lookup"><span data-stu-id="5aa57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa57-107">*pcElems* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5aa57-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa57-108">**DWORD** 的指標，其中包含集合中 **IPortableDeviceValues** 介面的數目。</span><span class="sxs-lookup"><span data-stu-id="5aa57-108">Pointer to a **DWORD** that contains the number of **IPortableDeviceValues** interfaces in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa57-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5aa57-109">Return value</span></span>

<span data-ttu-id="5aa57-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="5aa57-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5aa57-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="5aa57-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5aa57-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5aa57-112">Return code</span></span>                                                                               | <span data-ttu-id="5aa57-113">Description</span><span class="sxs-lookup"><span data-stu-id="5aa57-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="5aa57-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5aa57-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5aa57-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="5aa57-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="5aa57-116"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="5aa57-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5aa57-117">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5aa57-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5aa57-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5aa57-118">Requirements</span></span>



| <span data-ttu-id="5aa57-119">需求</span><span class="sxs-lookup"><span data-stu-id="5aa57-119">Requirement</span></span> | <span data-ttu-id="5aa57-120">值</span><span class="sxs-lookup"><span data-stu-id="5aa57-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa57-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5aa57-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5aa57-122"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="5aa57-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5aa57-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="5aa57-123">Library</span></span><br/> | <dl> <span data-ttu-id="5aa57-124"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5aa57-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aa57-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5aa57-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa57-126">**IPortableDeviceValuesCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="5aa57-126">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 





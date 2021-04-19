---
description: Clear 方法會釋放集合中的所有專案。
ms.assetid: 151d1f61-11f0-40f0-8da1-79e9eb2001ce
title: 'IPortableDeviceValuesCollection：： Clear 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bf826b8e8a2035a0d84aec76979616fcccee9948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992784"
---
# <a name="iportabledevicevaluescollectionclear-method"></a><span data-ttu-id="0cb9a-103">IPortableDeviceValuesCollection：： Clear 方法</span><span class="sxs-lookup"><span data-stu-id="0cb9a-103">IPortableDeviceValuesCollection::Clear method</span></span>

<span data-ttu-id="0cb9a-104">**Clear** 方法會釋放集合中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="0cb9a-104">The **Clear** method releases all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb9a-105">語法</span><span class="sxs-lookup"><span data-stu-id="0cb9a-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="0cb9a-106">參數</span><span class="sxs-lookup"><span data-stu-id="0cb9a-106">Parameters</span></span>

<span data-ttu-id="0cb9a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0cb9a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0cb9a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="0cb9a-108">Return value</span></span>

<span data-ttu-id="0cb9a-109">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="0cb9a-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0cb9a-110">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="0cb9a-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0cb9a-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0cb9a-111">Return code</span></span>                                                                          | <span data-ttu-id="0cb9a-112">Description</span><span class="sxs-lookup"><span data-stu-id="0cb9a-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0cb9a-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0cb9a-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0cb9a-114">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="0cb9a-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0cb9a-115">備註</span><span class="sxs-lookup"><span data-stu-id="0cb9a-115">Remarks</span></span>

<span data-ttu-id="0cb9a-116">方法會釋放配置給集合中專案的所有記憶體。</span><span class="sxs-lookup"><span data-stu-id="0cb9a-116">The method releases all memory that is allocated for the items in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb9a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cb9a-117">Requirements</span></span>



| <span data-ttu-id="0cb9a-118">需求</span><span class="sxs-lookup"><span data-stu-id="0cb9a-118">Requirement</span></span> | <span data-ttu-id="0cb9a-119">值</span><span class="sxs-lookup"><span data-stu-id="0cb9a-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb9a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0cb9a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0cb9a-121"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="0cb9a-121"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cb9a-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="0cb9a-122">Library</span></span><br/> | <dl> <span data-ttu-id="0cb9a-123"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0cb9a-123"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb9a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cb9a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb9a-125">**IPortableDeviceValuesCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="0cb9a-125">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 





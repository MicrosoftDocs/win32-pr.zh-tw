---
description: GetTypeInfoCount 方法會抓取物件提供的類型資訊介面數目。
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: 'CMediaPosition. GetTypeInfoCount 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cac543c49b7f2f6b9dc3357bbb1c691477d9b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977570"
---
# <a name="cmediapositiongettypeinfocount-method"></a><span data-ttu-id="fe2c9-103">CMediaPosition. GetTypeInfoCount 方法</span><span class="sxs-lookup"><span data-stu-id="fe2c9-103">CMediaPosition.GetTypeInfoCount method</span></span>

<span data-ttu-id="fe2c9-104">方法會抓取 `GetTypeInfoCount` 物件提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="fe2c9-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2c9-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe2c9-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="fe2c9-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe2c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe2c9-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="fe2c9-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="fe2c9-108">變數的指標，此變數會接收物件提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="fe2c9-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="fe2c9-109">當方法傳回時，值為1。</span><span class="sxs-lookup"><span data-stu-id="fe2c9-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe2c9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe2c9-110">Return value</span></span>

<span data-ttu-id="fe2c9-111">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fe2c9-111">Returns one of the following values.</span></span>



| <span data-ttu-id="fe2c9-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fe2c9-112">Return code</span></span>                                                                               | <span data-ttu-id="fe2c9-113">Description</span><span class="sxs-lookup"><span data-stu-id="fe2c9-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="fe2c9-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fe2c9-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="fe2c9-115">成功。</span><span class="sxs-lookup"><span data-stu-id="fe2c9-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="fe2c9-116"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="fe2c9-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="fe2c9-117">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="fe2c9-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fe2c9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe2c9-118">Requirements</span></span>



| <span data-ttu-id="fe2c9-119">需求</span><span class="sxs-lookup"><span data-stu-id="fe2c9-119">Requirement</span></span> | <span data-ttu-id="fe2c9-120">值</span><span class="sxs-lookup"><span data-stu-id="fe2c9-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe2c9-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fe2c9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fe2c9-122"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fe2c9-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fe2c9-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe2c9-123">Library</span></span><br/> | <dl> <span data-ttu-id="fe2c9-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fe2c9-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe2c9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe2c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe2c9-126">**CMediaPosition 類別**</span><span class="sxs-lookup"><span data-stu-id="fe2c9-126">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 





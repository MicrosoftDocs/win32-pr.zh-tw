---
description: CMediaPosition. GetTypeInfoCount 方法-GetTypeInfoCount 方法會抓取物件提供的類型資訊介面數目。
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
ms.openlocfilehash: 8cfc54f414a6722f7f69a0330fad2d1a0cfab425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095476"
---
# <a name="cmediapositiongettypeinfocount-method"></a><span data-ttu-id="04f73-103">CMediaPosition. GetTypeInfoCount 方法</span><span class="sxs-lookup"><span data-stu-id="04f73-103">CMediaPosition.GetTypeInfoCount method</span></span>

<span data-ttu-id="04f73-104">方法會抓取 `GetTypeInfoCount` 物件提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="04f73-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="04f73-105">語法</span><span class="sxs-lookup"><span data-stu-id="04f73-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="04f73-106">參數</span><span class="sxs-lookup"><span data-stu-id="04f73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04f73-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="04f73-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="04f73-108">變數的指標，此變數會接收物件提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="04f73-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="04f73-109">當方法傳回時，值為1。</span><span class="sxs-lookup"><span data-stu-id="04f73-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04f73-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="04f73-110">Return value</span></span>

<span data-ttu-id="04f73-111">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="04f73-111">Returns one of the following values.</span></span>



| <span data-ttu-id="04f73-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="04f73-112">Return code</span></span>                                                                               | <span data-ttu-id="04f73-113">Description</span><span class="sxs-lookup"><span data-stu-id="04f73-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="04f73-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="04f73-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="04f73-115">成功。</span><span class="sxs-lookup"><span data-stu-id="04f73-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="04f73-116"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="04f73-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="04f73-117">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="04f73-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="04f73-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="04f73-118">Requirements</span></span>



| <span data-ttu-id="04f73-119">需求</span><span class="sxs-lookup"><span data-stu-id="04f73-119">Requirement</span></span> | <span data-ttu-id="04f73-120">值</span><span class="sxs-lookup"><span data-stu-id="04f73-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04f73-121">標頭</span><span class="sxs-lookup"><span data-stu-id="04f73-121">Header</span></span><br/>  | <dl> <span data-ttu-id="04f73-122"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="04f73-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="04f73-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="04f73-123">Library</span></span><br/> | <dl> <span data-ttu-id="04f73-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="04f73-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04f73-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04f73-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f73-126">**CMediaPosition 類別**</span><span class="sxs-lookup"><span data-stu-id="04f73-126">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 





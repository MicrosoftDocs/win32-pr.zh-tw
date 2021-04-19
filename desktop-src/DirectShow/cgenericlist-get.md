---
description: Get 方法會在指定的位置抓取專案。
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: 'CGenericList： Get 方法 (Wxlist) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994150"
---
# <a name="cgenericlistget-method"></a><span data-ttu-id="7f041-103">CGenericList. Get 方法</span><span class="sxs-lookup"><span data-stu-id="7f041-103">CGenericList.Get method</span></span>

<span data-ttu-id="7f041-104">`Get`方法會在指定的位置抓取專案。</span><span class="sxs-lookup"><span data-stu-id="7f041-104">The `Get` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f041-105">語法</span><span class="sxs-lookup"><span data-stu-id="7f041-105">Syntax</span></span>


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="7f041-106">參數</span><span class="sxs-lookup"><span data-stu-id="7f041-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f041-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="7f041-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="7f041-108">要取得之專案的位置指標。</span><span class="sxs-lookup"><span data-stu-id="7f041-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f041-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f041-109">Return value</span></span>

<span data-ttu-id="7f041-110">傳回)  (範本型別 **物件** 之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="7f041-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f041-111">備註</span><span class="sxs-lookup"><span data-stu-id="7f041-111">Remarks</span></span>

<span data-ttu-id="7f041-112">如果 *pos* 是 **null**，則方法會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="7f041-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f041-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f041-113">Requirements</span></span>



| <span data-ttu-id="7f041-114">需求</span><span class="sxs-lookup"><span data-stu-id="7f041-114">Requirement</span></span> | <span data-ttu-id="7f041-115">值</span><span class="sxs-lookup"><span data-stu-id="7f041-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f041-116">標頭</span><span class="sxs-lookup"><span data-stu-id="7f041-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7f041-117"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7f041-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7f041-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f041-118">Library</span></span><br/> | <dl> <span data-ttu-id="7f041-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7f041-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f041-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f041-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f041-121">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="7f041-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 





---
description: Unadvise 方法會移除建議的要求。
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: 'CAMSchedule. Unadvise 方法 (Dsschedule .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993403"
---
# <a name="camscheduleunadvise-method"></a><span data-ttu-id="c7fa6-103">CAMSchedule. Unadvise 方法</span><span class="sxs-lookup"><span data-stu-id="c7fa6-103">CAMSchedule.Unadvise method</span></span>

<span data-ttu-id="c7fa6-104">`Unadvise`方法會移除建議的要求。</span><span class="sxs-lookup"><span data-stu-id="c7fa6-104">The `Unadvise` method removes an advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fa6-105">語法</span><span class="sxs-lookup"><span data-stu-id="c7fa6-105">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="c7fa6-106">參數</span><span class="sxs-lookup"><span data-stu-id="c7fa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7fa6-107">*dwAdviseCookie*</span><span class="sxs-lookup"><span data-stu-id="c7fa6-107">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="c7fa6-108">[**CAMSchedule：： AddAdvisePacket**](camschedule-addadvisepacket.md)方法所傳回之建議要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7fa6-108">Identifier of the advise request, returned by the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7fa6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7fa6-109">Return value</span></span>

<span data-ttu-id="c7fa6-110">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c7fa6-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c7fa6-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c7fa6-111">Return code</span></span>                                                                             | <span data-ttu-id="c7fa6-112">Description</span><span class="sxs-lookup"><span data-stu-id="c7fa6-112">Description</span></span>          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="c7fa6-113"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa6-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c7fa6-114">找不到</span><span class="sxs-lookup"><span data-stu-id="c7fa6-114">Not found</span></span><br/> |
| <dl> <span data-ttu-id="c7fa6-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa6-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c7fa6-116">Success</span><span class="sxs-lookup"><span data-stu-id="c7fa6-116">Success</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="c7fa6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7fa6-117">Requirements</span></span>



| <span data-ttu-id="c7fa6-118">需求</span><span class="sxs-lookup"><span data-stu-id="c7fa6-118">Requirement</span></span> | <span data-ttu-id="c7fa6-119">值</span><span class="sxs-lookup"><span data-stu-id="c7fa6-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fa6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c7fa6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c7fa6-121"><dt>Dsschedule (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c7fa6-121"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="c7fa6-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7fa6-122">Library</span></span><br/> | <dl> <span data-ttu-id="c7fa6-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c7fa6-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7fa6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7fa6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fa6-125">**CAMSchedule 類別**</span><span class="sxs-lookup"><span data-stu-id="c7fa6-125">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 





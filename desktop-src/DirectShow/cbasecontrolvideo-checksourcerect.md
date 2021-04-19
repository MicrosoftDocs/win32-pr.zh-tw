---
description: 判斷來源矩形是否有效。
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: 'CBaseControlVideo. CheckSourceRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa219687dabcf9124662e3269d157fb0a163a6a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994060"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a><span data-ttu-id="64b51-103">CBaseControlVideo. CheckSourceRect 方法</span><span class="sxs-lookup"><span data-stu-id="64b51-103">CBaseControlVideo.CheckSourceRect method</span></span>

<span data-ttu-id="64b51-104">判斷來源矩形是否有效。</span><span class="sxs-lookup"><span data-stu-id="64b51-104">Determines if a source rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b51-105">語法</span><span class="sxs-lookup"><span data-stu-id="64b51-105">Syntax</span></span>


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="64b51-106">參數</span><span class="sxs-lookup"><span data-stu-id="64b51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64b51-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="64b51-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="64b51-108">要檢查的來源矩形指標。</span><span class="sxs-lookup"><span data-stu-id="64b51-108">Pointer to the source rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64b51-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="64b51-109">Return value</span></span>

<span data-ttu-id="64b51-110">如果無效 \_ ，則傳回 E INVALIDARG，否則會傳回 >aad-userreadusingalternativesecurityid-noerror (S \_ OK) 。</span><span class="sxs-lookup"><span data-stu-id="64b51-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="64b51-111">備註</span><span class="sxs-lookup"><span data-stu-id="64b51-111">Remarks</span></span>

<span data-ttu-id="64b51-112">此成員函式會檢查所要求的來源矩形是否未超過可用的來源影片。</span><span class="sxs-lookup"><span data-stu-id="64b51-112">This member function checks that the source rectangle requested does not exceed the available source video.</span></span> <span data-ttu-id="64b51-113">左邊和上座標不可為負值，而且寬度和高度不能超過影片的右邊和底部。</span><span class="sxs-lookup"><span data-stu-id="64b51-113">The left and top coordinates cannot be negative, and the width and height cannot exceed the right and bottom of the video.</span></span>

## <a name="requirements"></a><span data-ttu-id="64b51-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="64b51-114">Requirements</span></span>



| <span data-ttu-id="64b51-115">需求</span><span class="sxs-lookup"><span data-stu-id="64b51-115">Requirement</span></span> | <span data-ttu-id="64b51-116">值</span><span class="sxs-lookup"><span data-stu-id="64b51-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64b51-117">標頭</span><span class="sxs-lookup"><span data-stu-id="64b51-117">Header</span></span><br/>  | <dl> <span data-ttu-id="64b51-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="64b51-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="64b51-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="64b51-119">Library</span></span><br/> | <dl> <span data-ttu-id="64b51-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="64b51-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64b51-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64b51-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b51-122">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="64b51-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





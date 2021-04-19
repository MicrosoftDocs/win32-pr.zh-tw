---
description: CheckTargetRect 方法會判斷目標矩形是否有效。
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: 'CBaseControlVideo. CheckTargetRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993495"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a><span data-ttu-id="f24fc-103">CBaseControlVideo. CheckTargetRect 方法</span><span class="sxs-lookup"><span data-stu-id="f24fc-103">CBaseControlVideo.CheckTargetRect method</span></span>

<span data-ttu-id="f24fc-104">`CheckTargetRect`方法會判斷目標矩形是否有效。</span><span class="sxs-lookup"><span data-stu-id="f24fc-104">The `CheckTargetRect` method determines if a target rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="f24fc-105">語法</span><span class="sxs-lookup"><span data-stu-id="f24fc-105">Syntax</span></span>


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="f24fc-106">參數</span><span class="sxs-lookup"><span data-stu-id="f24fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f24fc-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="f24fc-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="f24fc-108">要檢查的目標矩形指標。</span><span class="sxs-lookup"><span data-stu-id="f24fc-108">Pointer to the target rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f24fc-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f24fc-109">Return value</span></span>

<span data-ttu-id="f24fc-110">如果無效 \_ ，則傳回 E INVALIDARG，否則會傳回 >aad-userreadusingalternativesecurityid-noerror (S \_ OK) 。</span><span class="sxs-lookup"><span data-stu-id="f24fc-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="f24fc-111">備註</span><span class="sxs-lookup"><span data-stu-id="f24fc-111">Remarks</span></span>

<span data-ttu-id="f24fc-112">此成員函式會判斷所要求的目標矩形是否有效。</span><span class="sxs-lookup"><span data-stu-id="f24fc-112">This member function determines if the target rectangle requested is valid.</span></span> <span data-ttu-id="f24fc-113">因為目的矩形會在視窗的邏輯用戶端中指定位置，所以座標可以是負數，但整體寬度和高度不能是零或負數值。</span><span class="sxs-lookup"><span data-stu-id="f24fc-113">Because the destination rectangle specifies a position in the logical client of the window, the coordinates can be negative, although the overall width and height cannot be zero or a negative value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f24fc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f24fc-114">Requirements</span></span>



| <span data-ttu-id="f24fc-115">需求</span><span class="sxs-lookup"><span data-stu-id="f24fc-115">Requirement</span></span> | <span data-ttu-id="f24fc-116">值</span><span class="sxs-lookup"><span data-stu-id="f24fc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f24fc-117">標頭</span><span class="sxs-lookup"><span data-stu-id="f24fc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f24fc-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f24fc-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f24fc-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="f24fc-119">Library</span></span><br/> | <dl> <span data-ttu-id="f24fc-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f24fc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f24fc-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f24fc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f24fc-122">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="f24fc-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





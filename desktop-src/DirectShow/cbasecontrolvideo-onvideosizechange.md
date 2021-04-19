---
description: 將 EC \_ 影片 \_ 大小變更的訊息傳遞 \_ 至篩選圖形管理員。
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: 'CBaseControlVideo. OnVideoSizeChange 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985955"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a><span data-ttu-id="737e5-103">CBaseControlVideo. OnVideoSizeChange 方法</span><span class="sxs-lookup"><span data-stu-id="737e5-103">CBaseControlVideo.OnVideoSizeChange method</span></span>

<span data-ttu-id="737e5-104">將 EC \_ 影片 \_ 大小變更的訊息傳遞 \_ 至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="737e5-104">Passes an EC\_VIDEO\_SIZE\_CHANGED message to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="737e5-105">語法</span><span class="sxs-lookup"><span data-stu-id="737e5-105">Syntax</span></span>


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a><span data-ttu-id="737e5-106">參數</span><span class="sxs-lookup"><span data-stu-id="737e5-106">Parameters</span></span>

<span data-ttu-id="737e5-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="737e5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="737e5-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="737e5-108">Return value</span></span>

<span data-ttu-id="737e5-109">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="737e5-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="737e5-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="737e5-110">Return code</span></span>                                                                                   | <span data-ttu-id="737e5-111">Description</span><span class="sxs-lookup"><span data-stu-id="737e5-111">Description</span></span>               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="737e5-112"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="737e5-112"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="737e5-113">失敗。</span><span class="sxs-lookup"><span data-stu-id="737e5-113">Failure.</span></span><br/>       |
| <dl> <span data-ttu-id="737e5-114"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="737e5-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="737e5-115">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="737e5-115">Out of memory.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="737e5-116">備註</span><span class="sxs-lookup"><span data-stu-id="737e5-116">Remarks</span></span>

<span data-ttu-id="737e5-117">影片轉譯器會在每次影片大小變更時呼叫此成員函式;這通常會在初始連接之後呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="737e5-117">A video renderer should call this member function each time the video size is changed; this will typically be called once after initial connection.</span></span> <span data-ttu-id="737e5-118">如果轉譯器可支援從 320 x 240 到 160 x 120)  (動態格式變更，它也應該在每次變更之後呼叫它。</span><span class="sxs-lookup"><span data-stu-id="737e5-118">If the renderer can support dynamic format changes (from 320 x 240 to 160 x 120), it should also call it after each change.</span></span>

## <a name="requirements"></a><span data-ttu-id="737e5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="737e5-119">Requirements</span></span>



| <span data-ttu-id="737e5-120">需求</span><span class="sxs-lookup"><span data-stu-id="737e5-120">Requirement</span></span> | <span data-ttu-id="737e5-121">值</span><span class="sxs-lookup"><span data-stu-id="737e5-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="737e5-122">標頭</span><span class="sxs-lookup"><span data-stu-id="737e5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="737e5-123"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="737e5-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="737e5-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="737e5-124">Library</span></span><br/> | <dl> <span data-ttu-id="737e5-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="737e5-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="737e5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="737e5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737e5-127">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="737e5-127">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





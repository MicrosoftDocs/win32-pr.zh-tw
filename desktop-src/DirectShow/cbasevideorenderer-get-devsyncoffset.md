---
description: Get \_ DevSyncOffset 方法會從開始串流之後的所有畫面格，取得時間（以毫秒為單位）之間的標準差（以毫秒為單位）。
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: 'CBaseVideoRenderer.get_DevSyncOffset 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989751"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a><span data-ttu-id="e2b82-103">CBaseVideoRenderer. 取得 \_ DevSyncOffset 方法</span><span class="sxs-lookup"><span data-stu-id="e2b82-103">CBaseVideoRenderer.get\_DevSyncOffset method</span></span>

<span data-ttu-id="e2b82-104">方法會從 `get_DevSyncOffset` 開始串流之後的所有框架，取得時間（以毫秒為單位）之間的標準差（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e2b82-104">The `get_DevSyncOffset` method retrieves the standard deviation of the time in milliseconds between when each frame was due and when it was actually rendered, for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b82-105">語法</span><span class="sxs-lookup"><span data-stu-id="e2b82-105">Syntax</span></span>


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a><span data-ttu-id="e2b82-106">參數</span><span class="sxs-lookup"><span data-stu-id="e2b82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2b82-107">*piDev*</span><span class="sxs-lookup"><span data-stu-id="e2b82-107">*piDev*</span></span> 
</dt> <dd>

<span data-ttu-id="e2b82-108">先前所述時間的標準差指標。</span><span class="sxs-lookup"><span data-stu-id="e2b82-108">Pointer to the standard deviation of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2b82-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2b82-109">Return value</span></span>

<span data-ttu-id="e2b82-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e2b82-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2b82-111">備註</span><span class="sxs-lookup"><span data-stu-id="e2b82-111">Remarks</span></span>

<span data-ttu-id="e2b82-112">此成員函式會實 [**IQualProp：： get \_ DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) 方法。</span><span class="sxs-lookup"><span data-stu-id="e2b82-112">This member function implements the [**IQualProp::get\_DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b82-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2b82-113">Requirements</span></span>



| <span data-ttu-id="e2b82-114">需求</span><span class="sxs-lookup"><span data-stu-id="e2b82-114">Requirement</span></span> | <span data-ttu-id="e2b82-115">值</span><span class="sxs-lookup"><span data-stu-id="e2b82-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b82-116">標頭</span><span class="sxs-lookup"><span data-stu-id="e2b82-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e2b82-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e2b82-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e2b82-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2b82-118">Library</span></span><br/> | <dl> <span data-ttu-id="e2b82-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e2b82-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b82-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2b82-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b82-121">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="e2b82-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 





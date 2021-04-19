---
description: 「取得 \_ 抖動」方法會將每個畫面格之間的標準差（以毫秒為單位），從串流開始的所有框架中取出。
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: 'CBaseVideoRenderer.get_Jitter 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989750"
---
# <a name="cbasevideorendererget_jitter-method"></a><span data-ttu-id="f93cd-103">CBaseVideoRenderer。取得 \_ 抖動方法</span><span class="sxs-lookup"><span data-stu-id="f93cd-103">CBaseVideoRenderer.get\_Jitter method</span></span>

<span data-ttu-id="f93cd-104">此 `get_Jitter` 方法會在串流開始之後，從每個畫面格與所有畫面格之間的間隔中，取得時間的標準差（毫秒）。</span><span class="sxs-lookup"><span data-stu-id="f93cd-104">The `get_Jitter` method retrieves the standard deviation of time in milliseconds between each frame and the next for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="f93cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="f93cd-105">Syntax</span></span>


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a><span data-ttu-id="f93cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="f93cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f93cd-107">*piJitter*</span><span class="sxs-lookup"><span data-stu-id="f93cd-107">*piJitter*</span></span> 
</dt> <dd>

<span data-ttu-id="f93cd-108">幀出時間的標準差指標（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f93cd-108">Pointer to the standard deviation of the interframe time, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f93cd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f93cd-109">Return value</span></span>

<span data-ttu-id="f93cd-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="f93cd-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f93cd-111">備註</span><span class="sxs-lookup"><span data-stu-id="f93cd-111">Remarks</span></span>

<span data-ttu-id="f93cd-112">此成員函式會實 [**IQualProp：： get \_ 抖動**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) 方法。</span><span class="sxs-lookup"><span data-stu-id="f93cd-112">This member function implements the [**IQualProp::get\_Jitter**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f93cd-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f93cd-113">Requirements</span></span>



| <span data-ttu-id="f93cd-114">需求</span><span class="sxs-lookup"><span data-stu-id="f93cd-114">Requirement</span></span> | <span data-ttu-id="f93cd-115">值</span><span class="sxs-lookup"><span data-stu-id="f93cd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f93cd-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f93cd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f93cd-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f93cd-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f93cd-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="f93cd-118">Library</span></span><br/> | <dl> <span data-ttu-id="f93cd-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f93cd-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f93cd-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f93cd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f93cd-121">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="f93cd-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 





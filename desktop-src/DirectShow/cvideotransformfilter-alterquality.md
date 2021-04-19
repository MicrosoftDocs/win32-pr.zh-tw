---
description: AlterQuality 方法會通知篩選要求品質變更。 這個方法會覆寫 CTransformFilter：： AlterQuality 方法。
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: 'CVideoTransformFilter. AlterQuality 方法 (Vtrans .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999318"
---
# <a name="cvideotransformfilteralterquality-method"></a><span data-ttu-id="c8910-104">CVideoTransformFilter. AlterQuality 方法</span><span class="sxs-lookup"><span data-stu-id="c8910-104">CVideoTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="c8910-105">`AlterQuality`方法會通知篩選準則，要求品質變更。</span><span class="sxs-lookup"><span data-stu-id="c8910-105">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span> <span data-ttu-id="c8910-106">這個方法會覆寫 [**CTransformFilter：： AlterQuality**](ctransformfilter-alterquality.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c8910-106">This method overrides the [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8910-107">語法</span><span class="sxs-lookup"><span data-stu-id="c8910-107">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="c8910-108">參數</span><span class="sxs-lookup"><span data-stu-id="c8910-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8910-109">*問*</span><span class="sxs-lookup"><span data-stu-id="c8910-109">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="c8910-110">包含品質控制訊息的 [**品質**](/windows/win32/api/strmif/ns-strmif-quality)結構。</span><span class="sxs-lookup"><span data-stu-id="c8910-110">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8910-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8910-111">Return value</span></span>

<span data-ttu-id="c8910-112">傳回 E \_ 失敗。</span><span class="sxs-lookup"><span data-stu-id="c8910-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8910-113">備註</span><span class="sxs-lookup"><span data-stu-id="c8910-113">Remarks</span></span>

<span data-ttu-id="c8910-114">當輸出圖釘透過 [**IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 方法)  (收到品質訊息時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c8910-114">This method is called when the output pin receives a quality message (through the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method).</span></span>

<span data-ttu-id="c8910-115">*Q* 的延遲值儲存在 **m \_ itrLate** 成員變數中。</span><span class="sxs-lookup"><span data-stu-id="c8910-115">The lateness value from *q* is stored in the **m\_itrLate** member variable.</span></span> <span data-ttu-id="c8910-116">E 的傳回值表示轉譯器 \_ 應該藉由捨棄框架來趕上，雖然 **CVideoTransformFilter** 類別也會在適當的條件下卸載框架。</span><span class="sxs-lookup"><span data-stu-id="c8910-116">The return value of E\_FAIL indicates that the renderer should catch up by dropping frames, although the **CVideoTransformFilter** class will also drop frames under the right conditions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8910-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8910-117">Requirements</span></span>



| <span data-ttu-id="c8910-118">需求</span><span class="sxs-lookup"><span data-stu-id="c8910-118">Requirement</span></span> | <span data-ttu-id="c8910-119">值</span><span class="sxs-lookup"><span data-stu-id="c8910-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8910-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c8910-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c8910-121"><dt>Vtrans (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c8910-121"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c8910-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8910-122">Library</span></span><br/> | <dl> <span data-ttu-id="c8910-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c8910-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8910-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8910-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8910-125">**CVideoTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="c8910-125">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> <dt>

[<span data-ttu-id="c8910-126">**CVideoTransformFilter::ShouldSkipFrame**</span><span class="sxs-lookup"><span data-stu-id="c8910-126">**CVideoTransformFilter::ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 





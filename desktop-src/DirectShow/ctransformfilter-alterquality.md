---
description: AlterQuality 方法會通知篩選要求品質變更。
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: 'CTransformFilter. AlterQuality 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997672"
---
# <a name="ctransformfilteralterquality-method"></a><span data-ttu-id="f72c1-103">CTransformFilter. AlterQuality 方法</span><span class="sxs-lookup"><span data-stu-id="f72c1-103">CTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="f72c1-104">`AlterQuality`方法會通知篩選準則，要求品質變更。</span><span class="sxs-lookup"><span data-stu-id="f72c1-104">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72c1-105">語法</span><span class="sxs-lookup"><span data-stu-id="f72c1-105">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="f72c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="f72c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f72c1-107">*問*</span><span class="sxs-lookup"><span data-stu-id="f72c1-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="f72c1-108">包含品質控制訊息的 [**品質**](/windows/win32/api/strmif/ns-strmif-quality)結構。</span><span class="sxs-lookup"><span data-stu-id="f72c1-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f72c1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f72c1-109">Return value</span></span>

<span data-ttu-id="f72c1-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="f72c1-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f72c1-111">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="f72c1-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="f72c1-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f72c1-112">Return code</span></span>                                                                             | <span data-ttu-id="f72c1-113">Description</span><span class="sxs-lookup"><span data-stu-id="f72c1-113">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f72c1-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="f72c1-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="f72c1-115">未處理品質訊息。</span><span class="sxs-lookup"><span data-stu-id="f72c1-115">Did not handle the quality message.</span></span> <span data-ttu-id="f72c1-116">訊息應通過上游傳遞。</span><span class="sxs-lookup"><span data-stu-id="f72c1-116">The message should be passed upstream.</span></span><br/> |
| <dl> <span data-ttu-id="f72c1-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f72c1-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="f72c1-118">處理品質訊息。</span><span class="sxs-lookup"><span data-stu-id="f72c1-118">Handled the quality message.</span></span> <span data-ttu-id="f72c1-119">不需要進行其他動作。</span><span class="sxs-lookup"><span data-stu-id="f72c1-119">No further action is necessary.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="f72c1-120">備註</span><span class="sxs-lookup"><span data-stu-id="f72c1-120">Remarks</span></span>

<span data-ttu-id="f72c1-121">如果篩選準則可以執行品質控制，請覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="f72c1-121">Override this method if the filter can perform quality control.</span></span> <span data-ttu-id="f72c1-122">如需詳細資訊，請參閱 [品質控制管理](quality-control-management.md)。</span><span class="sxs-lookup"><span data-stu-id="f72c1-122">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f72c1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f72c1-123">Requirements</span></span>



| <span data-ttu-id="f72c1-124">需求</span><span class="sxs-lookup"><span data-stu-id="f72c1-124">Requirement</span></span> | <span data-ttu-id="f72c1-125">值</span><span class="sxs-lookup"><span data-stu-id="f72c1-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f72c1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f72c1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f72c1-127"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f72c1-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f72c1-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="f72c1-128">Library</span></span><br/> | <dl> <span data-ttu-id="f72c1-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f72c1-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f72c1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f72c1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72c1-131">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="f72c1-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 





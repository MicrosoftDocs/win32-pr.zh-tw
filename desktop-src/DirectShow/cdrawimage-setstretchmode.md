---
description: SetStretchMode 方法會計算影片影像是否必須伸展。
ms.assetid: ffdcaf9c-e157-4557-9193-8430c1c451bf
title: 'CDrawImage. SetStretchMode 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetStretchMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a4b3a6b104b9e2888776cc59183835f412fdcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995102"
---
# <a name="cdrawimagesetstretchmode-method"></a><span data-ttu-id="5f8a1-103">CDrawImage. SetStretchMode 方法</span><span class="sxs-lookup"><span data-stu-id="5f8a1-103">CDrawImage.SetStretchMode method</span></span>

<span data-ttu-id="5f8a1-104">`SetStretchMode`方法會計算影片影像是否必須伸展。</span><span class="sxs-lookup"><span data-stu-id="5f8a1-104">The `SetStretchMode` method calculates whether the video image must be stretched.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="5f8a1-105">Syntax</span></span>


```C++
void SetStretchMode();
```



## <a name="parameters"></a><span data-ttu-id="5f8a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="5f8a1-106">Parameters</span></span>

<span data-ttu-id="5f8a1-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5f8a1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f8a1-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f8a1-108">Return value</span></span>

<span data-ttu-id="5f8a1-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5f8a1-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f8a1-110">備註</span><span class="sxs-lookup"><span data-stu-id="5f8a1-110">Remarks</span></span>

<span data-ttu-id="5f8a1-111">每當來源或目標矩形變更時， **CDrawImage** 類別就會自動呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="5f8a1-111">The **CDrawImage** class automatically calls this method whenever the source or target rectangle changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f8a1-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f8a1-112">Requirements</span></span>



| <span data-ttu-id="5f8a1-113">需求</span><span class="sxs-lookup"><span data-stu-id="5f8a1-113">Requirement</span></span> | <span data-ttu-id="5f8a1-114">值</span><span class="sxs-lookup"><span data-stu-id="5f8a1-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8a1-115">標頭</span><span class="sxs-lookup"><span data-stu-id="5f8a1-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5f8a1-116"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5f8a1-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5f8a1-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="5f8a1-117">Library</span></span><br/> | <dl> <span data-ttu-id="5f8a1-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5f8a1-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f8a1-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f8a1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8a1-120">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="5f8a1-120">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 





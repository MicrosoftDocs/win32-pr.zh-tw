---
description: 指出執行階段錯誤是否發生的旗標。
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'CBasePin：： m_bRunTimeError 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001197"
---
# <a name="cbasepinm_bruntimeerror-member"></a><span data-ttu-id="f1def-103">CBasePin：： m \_ bRunTimeError 成員</span><span class="sxs-lookup"><span data-stu-id="f1def-103">CBasePin::m\_bRunTimeError member</span></span>

<span data-ttu-id="f1def-104">指出執行階段錯誤是否發生的旗標。</span><span class="sxs-lookup"><span data-stu-id="f1def-104">Flag that indicates whether a run-time error has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1def-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1def-105">Syntax</span></span>


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a><span data-ttu-id="f1def-106">備註</span><span class="sxs-lookup"><span data-stu-id="f1def-106">Remarks</span></span>

<span data-ttu-id="f1def-107">此旗標的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f1def-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="f1def-108">如果在串流處理期間發生執行階段錯誤，請將旗標設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f1def-108">Set the flag to **TRUE** if a run-time error occurs during streaming.</span></span> <span data-ttu-id="f1def-109">[**CBasePin：：非**](cbasepin-inactive.md)使用中方法會將旗標重設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f1def-109">The [**CBasePin::Inactive**](cbasepin-inactive.md) method resets the flag to **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1def-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1def-110">Requirements</span></span>



| <span data-ttu-id="f1def-111">需求</span><span class="sxs-lookup"><span data-stu-id="f1def-111">Requirement</span></span> | <span data-ttu-id="f1def-112">值</span><span class="sxs-lookup"><span data-stu-id="f1def-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1def-113">標頭</span><span class="sxs-lookup"><span data-stu-id="f1def-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f1def-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f1def-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f1def-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="f1def-115">Library</span></span><br/> | <dl> <span data-ttu-id="f1def-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f1def-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1def-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1def-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1def-118">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="f1def-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 





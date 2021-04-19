---
description: GetTime 方法會捕獲執行方法的時間。
ms.assetid: 40f00f21-6c35-4de6-b75a-ee6b14b0439f
title: 'CDeferredCommand. GetTime 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8673c16364f005f4169a940ddb6fee8b304fafbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998881"
---
# <a name="cdeferredcommandgettime-method"></a><span data-ttu-id="3495b-103">CDeferredCommand. GetTime 方法</span><span class="sxs-lookup"><span data-stu-id="3495b-103">CDeferredCommand.GetTime method</span></span>

<span data-ttu-id="3495b-104">`GetTime`方法會抓取方法的執行時間。</span><span class="sxs-lookup"><span data-stu-id="3495b-104">The `GetTime` method retrieves the time at which the method will be run.</span></span>

## <a name="syntax"></a><span data-ttu-id="3495b-105">語法</span><span class="sxs-lookup"><span data-stu-id="3495b-105">Syntax</span></span>


```C++
CRefTime GetTime();
```



## <a name="parameters"></a><span data-ttu-id="3495b-106">參數</span><span class="sxs-lookup"><span data-stu-id="3495b-106">Parameters</span></span>

<span data-ttu-id="3495b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3495b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3495b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3495b-108">Return value</span></span>

<span data-ttu-id="3495b-109">傳回包含參考時間的 [**CRefTime**](creftime.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3495b-109">Returns a [**CRefTime**](creftime.md) object containing a reference time.</span></span>

## <a name="requirements"></a><span data-ttu-id="3495b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="3495b-110">Requirements</span></span>



| <span data-ttu-id="3495b-111">需求</span><span class="sxs-lookup"><span data-stu-id="3495b-111">Requirement</span></span> | <span data-ttu-id="3495b-112">值</span><span class="sxs-lookup"><span data-stu-id="3495b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3495b-113">標頭</span><span class="sxs-lookup"><span data-stu-id="3495b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3495b-114"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3495b-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3495b-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="3495b-115">Library</span></span><br/> | <dl> <span data-ttu-id="3495b-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3495b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3495b-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3495b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3495b-118">**CDeferredCommand 類別**</span><span class="sxs-lookup"><span data-stu-id="3495b-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 





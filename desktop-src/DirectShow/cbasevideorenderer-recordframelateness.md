---
description: RecordFrameLateness 方法會記錄轉譯發生的及時時間，並收集屬性頁面的統計資料。
ms.assetid: 9d4b90d7-b529-40cc-a0fd-6635163fb7dd
title: 'CBaseVideoRenderer. RecordFrameLateness 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.RecordFrameLateness
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10ae7069ceedbe43f9614ea3fd1c7c901d7023cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975979"
---
# <a name="cbasevideorendererrecordframelateness-method"></a><span data-ttu-id="81306-103">CBaseVideoRenderer. RecordFrameLateness 方法</span><span class="sxs-lookup"><span data-stu-id="81306-103">CBaseVideoRenderer.RecordFrameLateness method</span></span>

<span data-ttu-id="81306-104">`RecordFrameLateness`方法會記錄轉譯發生的及時時間，並收集屬性頁的統計資料。</span><span class="sxs-lookup"><span data-stu-id="81306-104">The `RecordFrameLateness` method records how timely the rendering occurred and gathers statistics for the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="81306-105">語法</span><span class="sxs-lookup"><span data-stu-id="81306-105">Syntax</span></span>


```C++
virtual void RecordFrameLateness(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="81306-106">參數</span><span class="sxs-lookup"><span data-stu-id="81306-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81306-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="81306-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="81306-108">值，指出取樣超過其到期時間的延遲時間（以參考時間單位為單位）。</span><span class="sxs-lookup"><span data-stu-id="81306-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="81306-109">*trFrame*</span><span class="sxs-lookup"><span data-stu-id="81306-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="81306-110">在參考時間單位中的幀時間。</span><span class="sxs-lookup"><span data-stu-id="81306-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81306-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="81306-111">Return value</span></span>

<span data-ttu-id="81306-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="81306-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="81306-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="81306-113">Requirements</span></span>



| <span data-ttu-id="81306-114">需求</span><span class="sxs-lookup"><span data-stu-id="81306-114">Requirement</span></span> | <span data-ttu-id="81306-115">值</span><span class="sxs-lookup"><span data-stu-id="81306-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81306-116">標頭</span><span class="sxs-lookup"><span data-stu-id="81306-116">Header</span></span><br/>  | <dl> <span data-ttu-id="81306-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="81306-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81306-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="81306-118">Library</span></span><br/> | <dl> <span data-ttu-id="81306-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="81306-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81306-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81306-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81306-121">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="81306-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 





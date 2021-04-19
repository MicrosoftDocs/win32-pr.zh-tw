---
description: 開始位置變更時，會呼叫 ChangeStart 方法。
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: 'CSourceSeeking. ChangeStart 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987847"
---
# <a name="csourceseekingchangestart-method"></a><span data-ttu-id="fdeaa-103">CSourceSeeking. ChangeStart 方法</span><span class="sxs-lookup"><span data-stu-id="fdeaa-103">CSourceSeeking.ChangeStart method</span></span>

<span data-ttu-id="fdeaa-104">`ChangeStart`開始位置變更時，會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="fdeaa-104">The `ChangeStart` method is called when the start position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdeaa-105">語法</span><span class="sxs-lookup"><span data-stu-id="fdeaa-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a><span data-ttu-id="fdeaa-106">參數</span><span class="sxs-lookup"><span data-stu-id="fdeaa-106">Parameters</span></span>

<span data-ttu-id="fdeaa-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fdeaa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fdeaa-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdeaa-108">Return value</span></span>

<span data-ttu-id="fdeaa-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="fdeaa-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdeaa-110">備註</span><span class="sxs-lookup"><span data-stu-id="fdeaa-110">Remarks</span></span>

<span data-ttu-id="fdeaa-111">如果開始位置變更， [**CSourceSeeking：： SetPositions**](csourceseeking-setpositions.md) 方法就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="fdeaa-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the start position changes.</span></span> <span data-ttu-id="fdeaa-112">這個方法是純虛擬的;衍生的類別必須加以執行。</span><span class="sxs-lookup"><span data-stu-id="fdeaa-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="fdeaa-113">搜尋作業之後，時間戳記應從零重新開機。</span><span class="sxs-lookup"><span data-stu-id="fdeaa-113">After a seek operation, time stamps should restart from zero.</span></span> <span data-ttu-id="fdeaa-114">媒體時間應該會反映新的開始時間。</span><span class="sxs-lookup"><span data-stu-id="fdeaa-114">Media times should reflect the new start time.</span></span> <span data-ttu-id="fdeaa-115">下列範例顯示可能的實作為：</span><span class="sxs-lookup"><span data-stu-id="fdeaa-115">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="fdeaa-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdeaa-116">Requirements</span></span>



| <span data-ttu-id="fdeaa-117">需求</span><span class="sxs-lookup"><span data-stu-id="fdeaa-117">Requirement</span></span> | <span data-ttu-id="fdeaa-118">值</span><span class="sxs-lookup"><span data-stu-id="fdeaa-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdeaa-119">標頭</span><span class="sxs-lookup"><span data-stu-id="fdeaa-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fdeaa-120"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="fdeaa-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fdeaa-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="fdeaa-121">Library</span></span><br/> | <dl> <span data-ttu-id="fdeaa-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="fdeaa-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdeaa-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdeaa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdeaa-124">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="fdeaa-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 





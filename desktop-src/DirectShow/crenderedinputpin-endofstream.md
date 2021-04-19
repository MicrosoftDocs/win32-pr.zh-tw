---
description: 在將新的 run 命令發出至篩選器之前，EndOfStream 方法會通知 pin 不需要其他資料。 這個方法會實 IPin：： EndOfStream 方法。
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: 'CRenderedInputPin. EndOfStream 方法 (Amextra .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978759"
---
# <a name="crenderedinputpinendofstream-method"></a><span data-ttu-id="b7ab4-104">CRenderedInputPin. EndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="b7ab4-104">CRenderedInputPin.EndOfStream method</span></span>

<span data-ttu-id="b7ab4-105">在將 `EndOfStream` 新的 run 命令發出至篩選器之前，方法會通知 pin 不需要其他資料。</span><span class="sxs-lookup"><span data-stu-id="b7ab4-105">The `EndOfStream` method notifies the pin that no additional data is expected, until a new run command is issued to the filter.</span></span> <span data-ttu-id="b7ab4-106">這個方法會實 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。</span><span class="sxs-lookup"><span data-stu-id="b7ab4-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7ab4-107">語法</span><span class="sxs-lookup"><span data-stu-id="b7ab4-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="b7ab4-108">參數</span><span class="sxs-lookup"><span data-stu-id="b7ab4-108">Parameters</span></span>

<span data-ttu-id="b7ab4-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b7ab4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7ab4-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7ab4-110">Return value</span></span>

<span data-ttu-id="b7ab4-111">\_如果成功，則傳回，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b7ab4-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7ab4-112">備註</span><span class="sxs-lookup"><span data-stu-id="b7ab4-112">Remarks</span></span>

<span data-ttu-id="b7ab4-113">如果篩選器正在執行，這個方法會將 [**EC \_ 完成**](ec-complete.md) 事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="b7ab4-113">If the filter is running, this method sends an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> <span data-ttu-id="b7ab4-114">否則，會設定旗標，以便在 \_ 下次執行篩選時傳送 EC 完成事件。</span><span class="sxs-lookup"><span data-stu-id="b7ab4-114">Otherwise, is sets a flag so that the EC\_COMPLETE event is sent when the filter next runs.</span></span> <span data-ttu-id="b7ab4-115">清除篩選器會清除旗標。</span><span class="sxs-lookup"><span data-stu-id="b7ab4-115">Flushing the filter clears the flag.</span></span>

<span data-ttu-id="b7ab4-116">您應覆寫此方法以保存釘選的串流鎖定：</span><span class="sxs-lookup"><span data-stu-id="b7ab4-116">You should override this method to hold the pin's streaming lock:</span></span>


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



<span data-ttu-id="b7ab4-117">此外，如果篩選器以非同步方式處理 **接收** 呼叫，則在 \_ 篩選處理所有暫止的範例之前，釘選應該等候傳送 EC 完成事件。</span><span class="sxs-lookup"><span data-stu-id="b7ab4-117">Also, if the filter processes **Receive** calls asynchronously, the pin should wait to send the EC\_COMPLETE event until the filter has processed all pending samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7ab4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7ab4-118">Requirements</span></span>



| <span data-ttu-id="b7ab4-119">需求</span><span class="sxs-lookup"><span data-stu-id="b7ab4-119">Requirement</span></span> | <span data-ttu-id="b7ab4-120">值</span><span class="sxs-lookup"><span data-stu-id="b7ab4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ab4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b7ab4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b7ab4-122"><dt>Amextra (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b7ab4-122"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b7ab4-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7ab4-123">Library</span></span><br/> | <dl> <span data-ttu-id="b7ab4-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b7ab4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7ab4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7ab4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ab4-126">**CRenderedInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="b7ab4-126">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 





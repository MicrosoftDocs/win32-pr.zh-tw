---
description: '\_每當 tapi 未產生的新呼叫抵達 tapi 開啟的行時，就會將 TSPI LINE NEWCALL 訊息傳送至 LINEEVENT 回呼函式。'
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: 'LINE_NEWCALL 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979433"
---
# <a name="line_newcall-message"></a><span data-ttu-id="ad158-103">行 \_ NEWCALL 訊息</span><span class="sxs-lookup"><span data-stu-id="ad158-103">LINE\_NEWCALL message</span></span>

<span data-ttu-id="ad158-104">每當 tapi 未產生的新呼叫抵達 TAPI 開啟的行時，就會將 TSPI **LINE \_ NEWCALL** 訊息傳送至 [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) 回呼函式。</span><span class="sxs-lookup"><span data-stu-id="ad158-104">The TSPI **LINE\_NEWCALL** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function whenever a new call that TAPI has not originated arrives on a line that TAPI has open.</span></span> <span data-ttu-id="ad158-105">這必須是第一個針對該呼叫傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="ad158-105">This must be the first message sent regarding that call.</span></span> <span data-ttu-id="ad158-106">TAPI 會將 *htCall* 的不透明控制碼寫入服務提供者以 *dwParam2* 形式傳遞的位置。</span><span class="sxs-lookup"><span data-stu-id="ad158-106">TAPI writes the *htCall* opaque handle to the location passed by the service provider as *dwParam2*.</span></span> <span data-ttu-id="ad158-107">這會提供服務提供者要在後續訊息中使用的 *htCall* 值。</span><span class="sxs-lookup"><span data-stu-id="ad158-107">This gives the service provider the *htCall* value to be used in subsequent messages.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="ad158-108">參數</span><span class="sxs-lookup"><span data-stu-id="ad158-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad158-109">*htLine*</span><span class="sxs-lookup"><span data-stu-id="ad158-109">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="ad158-110">線路裝置的 TAPI 不透明物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="ad158-110">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="ad158-111">*htCall*</span><span class="sxs-lookup"><span data-stu-id="ad158-111">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="ad158-112">未使用的。</span><span class="sxs-lookup"><span data-stu-id="ad158-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="ad158-113">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="ad158-113">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="ad158-114">值行 \_ NEWCALL。</span><span class="sxs-lookup"><span data-stu-id="ad158-114">The value LINE\_NEWCALL.</span></span>

</dd> <dt>

<span data-ttu-id="ad158-115">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ad158-115">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="ad158-116">服務提供者的呼叫不透明控制碼，屬於 [**HDRVCALL**](hdrvline.md)型別。</span><span class="sxs-lookup"><span data-stu-id="ad158-116">The service provider's opaque handle for the call, of type [**HDRVCALL**](hdrvline.md).</span></span> <span data-ttu-id="ad158-117">TAPI 會將此值傳遞為 *hdCall* 參數，以識別在後續程式中叫用以在呼叫上操作的呼叫。</span><span class="sxs-lookup"><span data-stu-id="ad158-117">TAPI passes this value as the *hdCall* parameter to identify the call in subsequent procedures it invokes to operate on the call.</span></span>

</dd> <dt>

<span data-ttu-id="ad158-118">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ad158-118">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="ad158-119">指向 LPHTAPICALL 的類型指標，指向 [**HTAPICALL**](htapicall.md)。</span><span class="sxs-lookup"><span data-stu-id="ad158-119">A pointer of type LPHTAPICALL pointing to a [**HTAPICALL**](htapicall.md).</span></span> <span data-ttu-id="ad158-120">TAPI 會針對指定位置的呼叫，寫入 TAPI 不透明控制碼。</span><span class="sxs-lookup"><span data-stu-id="ad158-120">TAPI writes the TAPI opaque handle for the call to the indicated location.</span></span> <span data-ttu-id="ad158-121">服務提供者必須儲存此值，並將其傳遞為 *htCall* 參數，以識別在其回報給呼叫的後續事件中的呼叫。</span><span class="sxs-lookup"><span data-stu-id="ad158-121">The service provider must save this value and pass it as the *htCall* parameter to identify the call in subsequent events it reports for the call.</span></span>

<span data-ttu-id="ad158-122">此參數也可以取得 **Null** 值 (請參閱) 的下列備註區段。</span><span class="sxs-lookup"><span data-stu-id="ad158-122">This parameter can also acquire a value of **NULL** (see the following Remarks section).</span></span>

</dd> <dt>

<span data-ttu-id="ad158-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="ad158-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="ad158-124">未使用的。</span><span class="sxs-lookup"><span data-stu-id="ad158-124">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad158-125">備註</span><span class="sxs-lookup"><span data-stu-id="ad158-125">Remarks</span></span>

<span data-ttu-id="ad158-126">服務提供者應該傳送 [**該行 \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) 訊息作為此呼叫的下一則訊息。</span><span class="sxs-lookup"><span data-stu-id="ad158-126">The service provider should send the [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) message as the next message for this call.</span></span> <span data-ttu-id="ad158-127">**LINE \_ NEWCALL** 事件不尋常，因為它也會傳回值給服務提供者。</span><span class="sxs-lookup"><span data-stu-id="ad158-127">The **LINE\_NEWCALL** event is unusual in that it also passes a value back to the service provider.</span></span>

<span data-ttu-id="ad158-128">此函式會報告源自服務提供者的任何新呼叫， (輸入、輸出、在電話上起始，以及在 TAPI 和服務提供者尚未交換不透明控制碼的) 上。</span><span class="sxs-lookup"><span data-stu-id="ad158-128">This function reports any new calls that originate in the service provider (inbound, outbound, initiated at the phone, and so on) for which TAPI and the service provider have not yet exchanged opaque handles.</span></span> <span data-ttu-id="ad158-129">系統會交換這些控制碼，讓 TAPI 和服務提供者可以接著提出要求，並報告與呼叫相關的事件。</span><span class="sxs-lookup"><span data-stu-id="ad158-129">The handles are exchanged so that TAPI and the service provider can subsequently make requests and report events involving the call.</span></span> <span data-ttu-id="ad158-130">由於這些新的呼叫不一定是輸入，因此呼叫一開始可能會處於任何狀態，而不一定是 *提供* 狀態。</span><span class="sxs-lookup"><span data-stu-id="ad158-130">Because these new calls are not necessarily inbound, the calls can initially be in any state, not necessarily the *offering* state.</span></span> <span data-ttu-id="ad158-131">如果服務提供者啟動，併發現該行有一或多個呼叫已在使用中，它就會使用 **行 \_ NEWCALL** 訊息來通知 TAPI，然後以 [**行 \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) 訊息指出目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="ad158-131">If the service provider starts and discovers that one or more calls are already active on the line, it informs TAPI of them with **LINE\_NEWCALL** messages followed by [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages indicating the current state.</span></span> <span data-ttu-id="ad158-132">由使用者在電話上起始的新撥出電話，將會以 **行 \_ NEWCALL** 訊息來回報，而初始 **行 \_ CALLSTATE** 訊息會指出通話處於 **撥號撥號** 狀態 (然後繼續進行) 。</span><span class="sxs-lookup"><span data-stu-id="ad158-132">A new outgoing call, initiated on the phone by the user, would be reported with a **LINE\_NEWCALL** message, and the initial **LINE\_CALLSTATE** message would indicate that the call was in **DIALTONE** state (and then continuing on from there).</span></span>

<span data-ttu-id="ad158-133">如果服務提供者在很短的時間內將大量呼叫傳遞給 TAPI (在相同的插斷週期) 期間，TAPI 可能會在處理這些呼叫時累積。</span><span class="sxs-lookup"><span data-stu-id="ad158-133">If the service provider passes a large number of calls to TAPI in a very short amount of time (during the same interrupt cycle), TAPI can become backlogged in processing those calls.</span></span> <span data-ttu-id="ad158-134">當發生這種情況時，TAPI 會向服務提供者指出在傳送任何其他呼叫之前，會先等候一小段時間。</span><span class="sxs-lookup"><span data-stu-id="ad158-134">When this happens, TAPI signals to the service provider to wait a short time before sending any more calls.</span></span> <span data-ttu-id="ad158-135">它會藉由將 **Null** 值（而不是有效的 [**HTAPICALL**](htapicall.md)）寫入至 **\_ NEWCALL 行** *dwParam2* 參數所指向的位置來發出信號。</span><span class="sxs-lookup"><span data-stu-id="ad158-135">It signals this by writing a value of **NULL**, instead of a valid [**HTAPICALL**](htapicall.md), into the location pointed to by the *dwParam2* parameter of **LINE\_NEWCALL**.</span></span> <span data-ttu-id="ad158-136">這表示嘗試處理新提供的呼叫控制碼失敗，最有可能是因為暫時無法配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="ad158-136">This indicates that the attempt to process the newly offered call handle was not successful, most likely due to a temporary inability to allocate memory.</span></span> <span data-ttu-id="ad158-137">服務提供者可以藉由卸載呼叫來回應，或是在排程延遲之後重新傳送 **行 \_ NEWCALL** 訊息來回應 (在這段期間，服務提供者應該產生處理器以允許 TAPI 處理其他擱置中的動作) 。</span><span class="sxs-lookup"><span data-stu-id="ad158-137">The service provider can respond by dropping the call or by resending the **LINE\_NEWCALL** message after a scheduling delay (during which time the service provider should yield the processor to allow TAPI to process other pending actions).</span></span> <span data-ttu-id="ad158-138">在任何情況下，您可以將新呼叫的相關訊息傳遞給 TAPI，直到控制碼交換成功為止。</span><span class="sxs-lookup"><span data-stu-id="ad158-138">In any case, no further messages regarding the new call can be passed to TAPI until the handle exchange succeeds.</span></span> <span data-ttu-id="ad158-139">當 *dwParam2* 所指向的位置取得非 **Null** 值時，服務提供者會知道此值是對呼叫的有效 [**HTAPICALL**](htapicall.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="ad158-139">When the location pointed to by *dwParam2* acquires a non-**NULL** value, the service provider knows that this value is a valid [**HTAPICALL**](htapicall.md) handle to the call.</span></span>

<span data-ttu-id="ad158-140">TAPI 層級沒有直接對應的訊息。</span><span class="sxs-lookup"><span data-stu-id="ad158-140">There is no directly corresponding message at the TAPI level.</span></span> <span data-ttu-id="ad158-141">此訊息是在 TSPI 層級上使用，以獨特且明確的方式引入新的 TAPI 來電，並取得 TAPI 不透明識別碼進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="ad158-141">This message is used at the TSPI level to uniquely and unambiguously introduce a new incoming call to TAPI and retrieve the TAPI opaque identifier for the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad158-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad158-142">Requirements</span></span>



| <span data-ttu-id="ad158-143">需求</span><span class="sxs-lookup"><span data-stu-id="ad158-143">Requirement</span></span> | <span data-ttu-id="ad158-144">值</span><span class="sxs-lookup"><span data-stu-id="ad158-144">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ad158-145">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ad158-145">TAPI version</span></span><br/> | <span data-ttu-id="ad158-146">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ad158-146">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ad158-147">標頭</span><span class="sxs-lookup"><span data-stu-id="ad158-147">Header</span></span><br/>       | <dl> <span data-ttu-id="ad158-148"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad158-148"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad158-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad158-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad158-150">[**行 \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad158-150">[**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ad158-151">**LINEEVENT**</span><span class="sxs-lookup"><span data-stu-id="ad158-151">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 


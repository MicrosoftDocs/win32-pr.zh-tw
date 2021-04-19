---
description: 同步處理 DVD 命令
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: 同步處理 DVD 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d677c38363a0ab80f90f58498eeef24bdc29eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990449"
---
# <a name="synchronizing-dvd-commands"></a><span data-ttu-id="467c7-103">同步處理 DVD 命令</span><span class="sxs-lookup"><span data-stu-id="467c7-103">Synchronizing DVD Commands</span></span>

<span data-ttu-id="467c7-104">DVD 命令不一定會立即完成。</span><span class="sxs-lookup"><span data-stu-id="467c7-104">DVD commands do not always complete instantly.</span></span> <span data-ttu-id="467c7-105">基於這個理由， [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 中的某些方法是非同步。</span><span class="sxs-lookup"><span data-stu-id="467c7-105">For this reason, some of the methods in [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) are asynchronous.</span></span> <span data-ttu-id="467c7-106">這些包括播放方法（例如 **PlayTitle**）和功能表導覽方法（例如 **ShowMenu** 和 **ReturnFromSubmenu**）。</span><span class="sxs-lookup"><span data-stu-id="467c7-106">These include playback methods, such as **PlayTitle**, and menu navigation methods, such as **ShowMenu** and **ReturnFromSubmenu**.</span></span> <span data-ttu-id="467c7-107">非同步方法會立即傳回，而不會等候命令完成。</span><span class="sxs-lookup"><span data-stu-id="467c7-107">An asynchronous method returns immediately, without waiting for the command to complete.</span></span> <span data-ttu-id="467c7-108">在方法傳回之後，即使方法成功，其他事件也可能會導致命令無法完成。</span><span class="sxs-lookup"><span data-stu-id="467c7-108">After the method returns, other events may prevent the command from completing, even if the method succeeded.</span></span> <span data-ttu-id="467c7-109">DirectShow 提供數個選項來同步處理命令，範圍從無同步處理到使用篩選圖形事件的完整同步處理。</span><span class="sxs-lookup"><span data-stu-id="467c7-109">DirectShow provides several options for synchronizing commands, ranging from no synchronization to full synchronization using filter graph events.</span></span>

<span data-ttu-id="467c7-110">所有的非同步方法都有 *dwFlags* 參數和 *ppCmd* 參數。</span><span class="sxs-lookup"><span data-stu-id="467c7-110">All of the asynchronous methods have a *dwFlags* parameter and a *ppCmd* parameter.</span></span> <span data-ttu-id="467c7-111">*DwFlags* 參數會指定同步處理行為，而 *ppCmd* 參數會傳回選擇性同步處理物件的指標。</span><span class="sxs-lookup"><span data-stu-id="467c7-111">The *dwFlags* parameter specifies the synchronization behavior, and the *ppCmd* parameter returns a pointer to an optional synchronization object.</span></span> <span data-ttu-id="467c7-112">根據您提供給這些參數的值而定，會有不同的行為結果。</span><span class="sxs-lookup"><span data-stu-id="467c7-112">Different behaviors result depending on what values you give for these parameters.</span></span>

<span data-ttu-id="467c7-113">**無同步處理**</span><span class="sxs-lookup"><span data-stu-id="467c7-113">**No Synchronization**</span></span>

<span data-ttu-id="467c7-114">若是基本的 DVD 播放應用程式，最好的選擇就是忽略同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="467c7-114">For a basic DVD playback application, the best option may be simply to ignore synchronization issues.</span></span> <span data-ttu-id="467c7-115">有時命令可能會失敗，或 UI 在更新時可能會稍微延遲一點，但這些錯誤會依秒數的順序排列。</span><span class="sxs-lookup"><span data-stu-id="467c7-115">Occasionally a command may fail or the UI might lag slightly when it updates, but these errors will be on the order of fractions of seconds.</span></span>

<span data-ttu-id="467c7-116">若要發出無同步處理的命令，請 \_ \_ 在 dwFlags 參數中設定 DVD CMD 旗標 \_ None 旗標，並將 *PpCmd* 參數設定為 **Null**：</span><span class="sxs-lookup"><span data-stu-id="467c7-116">To issue a command with no synchronization, set the DVD\_CMD\_FLAG\_None flag in the *dwFlags* parameter and set the *ppCmd* parameter to **NULL**:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



<span data-ttu-id="467c7-117">**封鎖**</span><span class="sxs-lookup"><span data-stu-id="467c7-117">**Blocking**</span></span>

<span data-ttu-id="467c7-118">如果您 \_ \_ \_ 在 dwFlags 參數中設定 EC DVD CMD 旗標 \_ 封鎖旗標，方法會封鎖，直到命令完成為止： </span><span class="sxs-lookup"><span data-stu-id="467c7-118">If you set the EC\_DVD\_CMD\_FLAG\_Block flag in the *dwFlags* parameter, the method blocks until the command completes:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



<span data-ttu-id="467c7-119">實際上，這個旗標會將非同步方法變成同步方法。</span><span class="sxs-lookup"><span data-stu-id="467c7-119">In effect, this flag turns an asynchronous method into a synchronous method.</span></span> <span data-ttu-id="467c7-120">缺點是當您從應用程式執行緒呼叫方法時，您的 UI 會封鎖。</span><span class="sxs-lookup"><span data-stu-id="467c7-120">The drawback is that your UI blocks if you call the method from the application thread.</span></span>

<span data-ttu-id="467c7-121">**同步處理物件**</span><span class="sxs-lookup"><span data-stu-id="467c7-121">**Synchronization Object**</span></span>

<span data-ttu-id="467c7-122">所有的非同步方法都可以傳回同步處理物件，您可以用它來等候命令開始或結束。</span><span class="sxs-lookup"><span data-stu-id="467c7-122">All of the asynchronous methods can return a synchronization object, which you can use to wait for the command to start or end.</span></span> <span data-ttu-id="467c7-123">若要取得此物件，請在 *ppCmd* 參數中傳遞 [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd)指標的位址：</span><span class="sxs-lookup"><span data-stu-id="467c7-123">To get this object, pass the address of an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) pointer in the *ppCmd* parameter:</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



<span data-ttu-id="467c7-124">如果方法成功，它會傳回新的 **IDvdCmd** 物件。</span><span class="sxs-lookup"><span data-stu-id="467c7-124">If the method succeeds, it returns a new **IDvdCmd** object.</span></span> <span data-ttu-id="467c7-125">[**IDvdCmd：： WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart)方法會封鎖，直到命令開始，而 [**IDvdCmd：： WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend)方法會封鎖，直到命令結束為止。</span><span class="sxs-lookup"><span data-stu-id="467c7-125">The [**IDvdCmd::WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) method blocks until the command begins, and the [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) method blocks until the command ends.</span></span> <span data-ttu-id="467c7-126">傳回值指出命令的狀態。</span><span class="sxs-lookup"><span data-stu-id="467c7-126">The return value indicates the status of the command.</span></span>

<span data-ttu-id="467c7-127">下列程式碼在功能上等同于設定 EC \_ DVD \_ CMD \_ 旗標 \_ 封鎖旗標，如先前所示。</span><span class="sxs-lookup"><span data-stu-id="467c7-127">The following code is functionally equivalent to setting the EC\_DVD\_CMD\_FLAG\_Block flag, shown previously.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



<span data-ttu-id="467c7-128">在此情況下， **PlayTitle** 方法不會封鎖，而是藉由呼叫 **WaitForEnd** 來封鎖應用程式。</span><span class="sxs-lookup"><span data-stu-id="467c7-128">In this case, the **PlayTitle** method does not block, but the application blocks by calling **WaitForEnd**.</span></span>

<span data-ttu-id="467c7-129">**命令狀態事件**</span><span class="sxs-lookup"><span data-stu-id="467c7-129">**Command Status Events**</span></span>

<span data-ttu-id="467c7-130">如果您 \_ \_ 在 dwFlags 參數中設定 dvd cmd 旗標 \_ SendEvents 旗標，則當命令開始時，dvd 瀏覽器會傳送 [**ec \_ dvd \_ cmd \_ START**](ec-dvd-cmd-start.md)事件，而當命令結束時，則會傳送 [**ec \_ dvd \_ cmd \_ END**](ec-dvd-cmd-end.md)事件。 </span><span class="sxs-lookup"><span data-stu-id="467c7-130">If you set the DVD\_CMD\_FLAG\_SendEvents flag in the *dwFlags* parameter, the DVD Navigator sends an [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) event when the command begins and an [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event when the command ends.</span></span>

<span data-ttu-id="467c7-131">事件的 *lParam2* 參數是命令的 HRESULT 傳回值。</span><span class="sxs-lookup"><span data-stu-id="467c7-131">The event's *lParam2* parameter is the HRESULT return value for the command.</span></span> <span data-ttu-id="467c7-132">事件的 *lParam1* 參數提供取得命令之同步處理物件的方式。</span><span class="sxs-lookup"><span data-stu-id="467c7-132">The event's *lParam1* parameter provides a way get the synchronization object for the command.</span></span> <span data-ttu-id="467c7-133">如果您將 *lParam1* 傳遞至 [**IDvdInfo2：： GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) 方法，則方法會傳回同步處理物件 **IDvdCmd** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="467c7-133">If you pass *lParam1* to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method, the method returns a pointer to the synchronization object's **IDvdCmd** interface.</span></span> <span data-ttu-id="467c7-134">您可以使用此介面來等候命令完成（如先前所述）。</span><span class="sxs-lookup"><span data-stu-id="467c7-134">You can use this interface to wait for completion of the command, as described earlier.</span></span> <span data-ttu-id="467c7-135">但是，如果您針對原始 **IDvdControl2** 方法中的 *PpCmd* 參數傳遞 **Null** ，則 DVD 導覽器不會建立同步處理物件，且 **GetCmdFromEvent** 會傳回 E \_ FAIL。</span><span class="sxs-lookup"><span data-stu-id="467c7-135">However, if you passed **NULL** for the *ppCmd* parameter in the original **IDvdControl2** method, the DVD Navigator does not create a synchronization object, and **GetCmdFromEvent** returns E\_FAIL.</span></span>

<span data-ttu-id="467c7-136">下列程式碼顯示如何使用沒有同步處理物件的命令狀態事件。</span><span class="sxs-lookup"><span data-stu-id="467c7-136">The following code shows how to use command status events with no synchronization object.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



<span data-ttu-id="467c7-137">請注意，如果沒有同步處理物件，您就無法分辨哪一個命令與事件相關聯。</span><span class="sxs-lookup"><span data-stu-id="467c7-137">Note that without a synchronization object, you cannot tell which command is associated with the event.</span></span> <span data-ttu-id="467c7-138">下列程式碼示範如何使用事件與同步處理物件。</span><span class="sxs-lookup"><span data-stu-id="467c7-138">The following code shows how to use events with the synchronization object.</span></span> <span data-ttu-id="467c7-139">其概念是將同步處理物件儲存在清單中，然後在您取得 [**EC \_ dvd \_ Cmd \_ START**](ec-dvd-cmd-start.md) 或 [**EC \_ dvd \_ cmd \_ 結束**](ec-dvd-cmd-end.md) 事件時比較物件指標。</span><span class="sxs-lookup"><span data-stu-id="467c7-139">The idea is to store the synchronization objects in a list and then compare object pointers when you get the [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) or [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



<span data-ttu-id="467c7-140">**清除 DVD Navigator 的緩衝區**</span><span class="sxs-lookup"><span data-stu-id="467c7-140">**Flushing the DVD Navigator's Buffers**</span></span>

<span data-ttu-id="467c7-141">在播放期間，DVD 導覽器會緩衝影片資料。</span><span class="sxs-lookup"><span data-stu-id="467c7-141">During playback, the DVD Navigator buffers video data.</span></span> <span data-ttu-id="467c7-142">緩衝的資料量會有所不同。</span><span class="sxs-lookup"><span data-stu-id="467c7-142">The amount of buffered data varies.</span></span> <span data-ttu-id="467c7-143">當 DVD 導覽器切換至新的影片時，已在管線中的資料不會遺失，因此轉換會順暢。</span><span class="sxs-lookup"><span data-stu-id="467c7-143">When the DVD Navigator switches to a new piece of video, data already in the pipeline is not lost, so the transition is seamless.</span></span> <span data-ttu-id="467c7-144">根據預設，當 DVD 導覽器發出命令時，它不會排清已在管線中的資料。</span><span class="sxs-lookup"><span data-stu-id="467c7-144">By default, when the DVD Navigator issues a command, it does not flush data already in the pipeline.</span></span> <span data-ttu-id="467c7-145">如此一來，可能會有一些延遲，您才能看到命令的效果，視緩衝的資料量而定。</span><span class="sxs-lookup"><span data-stu-id="467c7-145">As a result, there may be some latency before you can see the effect of the command, depending on how much data is buffered.</span></span> <span data-ttu-id="467c7-146">若要增加回應能力，您可以設定 DVD CMD 旗標排清旗標來強制讓 DVD Navigator 排清 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="467c7-146">To increase the responsiveness, you can force the DVD Navigator to flush by setting the DVD\_CMD\_FLAG\_Flush flag.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



<span data-ttu-id="467c7-147">此旗標可以與先前所述的任何旗標結合使用位 OR。</span><span class="sxs-lookup"><span data-stu-id="467c7-147">This flag can be combined with any of the flags described previously, using a bitwise OR.</span></span> <span data-ttu-id="467c7-148">清除的副作用是某些影片可能會遺失，因此，如果您需要保證影片中沒有間距，請不要使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="467c7-148">A side effect of flushing is that some video may be lost, so do not use this flag if you need to guarantee there are no gaps in the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="467c7-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="467c7-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="467c7-150">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="467c7-150">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 




---
title: 'WM_DDE_ACK 訊息 (的) '
description: WM \_ dde \_ 通知訊息會通知動態資料交換 (DDE) 應用程式的接收和處理下列訊息： wm dde 傳送 \_ \_ 、WM \_ dde \_ 執行、wm \_ DDE \_ 資料、WM \_ dde \_ 建議、wm \_ dde \_ UNADVISE、wm dde \_ \_ 初始，或 wm \_ dde \_ 要求 (在某些情況下) 。 若要張貼此訊息，請使用下列參數呼叫 PostMessage 函數。
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- WM_DDE_ACK 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025016"
---
# <a name="wm_dde_ack-message"></a><span data-ttu-id="a4ab5-105">WM \_ DDE \_ ACK 訊息</span><span class="sxs-lookup"><span data-stu-id="a4ab5-105">WM\_DDE\_ACK message</span></span>

<span data-ttu-id="a4ab5-106">**Wm \_ dde \_** 通知訊息會通知動態資料交換 (DDE) 應用程式接收和處理下列訊息： [**wm \_ dde \_**](wm-dde-poke.md)傳送、 [**wm \_ dde \_ 執行**](wm-dde-execute.md)、 [**wm \_ dde \_ 資料**](wm-dde-data.md)、 [**wm \_ dde \_ 建議**](wm-dde-advise.md)、 [**wm \_ dde \_ UNADVISE**](wm-dde-unadvise.md)、 [**wm dde \_ \_ 起始**](wm-dde-initiate.md)或 [**wm \_ dde \_ 要求**](wm-dde-request.md) (在某些情況下) 。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-106">The **WM\_DDE\_ACK** message notifies a Dynamic Data Exchange (DDE) application of the receipt and processing of the following messages: [**WM\_DDE\_POKE**](wm-dde-poke.md), [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_ADVISE**](wm-dde-advise.md), [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md), [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), or [**WM\_DDE\_REQUEST**](wm-dde-request.md) (in some cases).</span></span>

<span data-ttu-id="a4ab5-107">若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a><span data-ttu-id="a4ab5-108">參數</span><span class="sxs-lookup"><span data-stu-id="a4ab5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4ab5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a4ab5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4ab5-110">當回應 [**WM \_ DDE 的 \_ 起始**](wm-dde-initiate.md)時，此參數是傳送訊息之伺服器視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-110">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), this parameter is a handle to the server window sending the message.</span></span>

<span data-ttu-id="a4ab5-111">當回應 [**WM \_ DDE 的 \_ 執行**](wm-dde-execute.md)時，此參數是伺服器視窗張貼訊息的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-111">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), this parameter is a handle to the server window posting the message.</span></span>

<span data-ttu-id="a4ab5-112">當您回復所有其他訊息時，此參數是用戶端或伺服器視窗張貼訊息的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-112">When replying to all other messages, this parameter is a handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="a4ab5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4ab5-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4ab5-114">當回應 [**WM \_ DDE 的 \_ 起始**](wm-dde-initiate.md)時，低序位單字包含識別回復應用程式的 atom。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-114">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), the low-order word contains an atom that identifies the replying application.</span></span> <span data-ttu-id="a4ab5-115">高序位單字包含一個 atom，可識別正在建立交談的主題。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-115">The high-order word contains an atom that identifies the topic for which a conversation is being established.</span></span>

<span data-ttu-id="a4ab5-116">當回應 [**WM \_ DDE 的 \_ 執行**](wm-dde-execute.md)時，低序位單字會指定包含一連串旗標的 [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) 結構，這些旗標表示回應的狀態。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-116">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="a4ab5-117">高序位單字是全域記憶體物件的控制碼，其中包含在 **WM \_ DDE \_ 執行** 訊息中收到的命令字串。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-117">The high-order word is a handle to a global memory object that contains the command string that was received in the **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="a4ab5-118">當您回復所有其他訊息時，低序位單字會指定 [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) 結構，其中包含一系列指出回應狀態的旗標。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-118">When replying to all other messages, the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="a4ab5-119">高序位字組包含全域 atom，可識別回應傳送的資料項目名稱。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-119">The high-order word contains a global atom that identifies the name of the data item for which the response is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4ab5-120">備註</span><span class="sxs-lookup"><span data-stu-id="a4ab5-120">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="a4ab5-121">張貼</span><span class="sxs-lookup"><span data-stu-id="a4ab5-121">Posting</span></span>

<span data-ttu-id="a4ab5-122">除了回應 [**WM \_ dde \_ 起始**](wm-dde-initiate.md)訊息之外，應用程式也會呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)函式，而不是透過呼叫 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)函式，以張貼 **wm \_ dde \_** 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-122">Except in response to the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message, the application posts the **WM\_DDE\_ACK** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not by calling the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="a4ab5-123">當回應 **WM \_ dde 的 \_ 起始** 時，應用程式會呼叫 **SendMessage** 來傳送 **WM \_ dde \_ ACK** 訊息。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-123">When responding to **WM\_DDE\_INITIATE**, the application sends the **WM\_DDE\_ACK** message by calling **SendMessage**.</span></span> <span data-ttu-id="a4ab5-124">在此情況下，應用程式名稱 atom 和主題名稱 atom 都不應為 **null** (即使是由 **WM \_ DDE \_ 初始化** 訊息指定的 **null** 原子) 。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-124">In this case, neither the application-name atom nor the topic-name atom should be **NULL** (even if the **WM\_DDE\_INITIATE** message specified **NULL** atoms).</span></span>

<span data-ttu-id="a4ab5-125">當您使用隨附的 atom 來確認任何訊息時，應用程式張貼了 **WM \_ DDE \_** 通知可以重複使用伴隨原始訊息的 atom，或是將它刪除並建立新訊息。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-125">When acknowledging any message with an accompanying atom, the application posting **WM\_DDE\_ACK** can either reuse the atom that accompanied the original message, or it can delete it and create a new one.</span></span>

<span data-ttu-id="a4ab5-126">當您在確認 [**\_ \_ 執行 wm dde dde**](wm-dde-execute.md)時，張貼了 **wm \_ dde \_** 通知的應用程式應該重複使用原始 **wm \_ dde \_ 執行** 訊息中識別的全域記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-126">When acknowledging [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the application that posts **WM\_DDE\_ACK** should reuse the global memory object identified in the original **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="a4ab5-127">所有張貼 **的 \_ WM \_ DDE** 通知訊息都必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數來建立或重複使用 *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-127">All posted **WM\_DDE\_ACK** messages must create or reuse the *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="a4ab5-128">如果應用程式已透過張貼 [**WM \_ DDE DDE \_ 終止**](wm-dde-terminate.md) 並等候確認來起始交談的終止，則等待應用程式應該不會認可 (的正面或負面) 其他應用程式傳送的任何後續訊息。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-128">If an application has initiated the termination of a conversation by posting [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) and is awaiting confirmation, the waiting application should not acknowledge (positively or negatively) any subsequent messages sent by the other application.</span></span> <span data-ttu-id="a4ab5-129">等候中的應用程式應該刪除這些中間訊息中收到的任何原子或共用記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-129">The waiting application should delete any atoms or shared memory objects received in these intervening messages.</span></span> <span data-ttu-id="a4ab5-130">如果在 [**wm \_ dde \_**](wm-dde-poke.md)郵件和 [**wm \_ dde \_ 資料**](wm-dde-data.md)訊息中， **fRelease** 旗標設定為 **FALSE** ，則不應釋放記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-130">Memory objects should not be freed if the **fRelease** flag is set to **FALSE** in [**WM\_DDE\_POKE**](wm-dde-poke.md) and [**WM\_DDE\_DATA**](wm-dde-data.md) messages.</span></span>

### <a name="receiving"></a><span data-ttu-id="a4ab5-131">接收</span><span class="sxs-lookup"><span data-stu-id="a4ab5-131">Receiving</span></span>

<span data-ttu-id="a4ab5-132">接收 **WM \_ DDE \_** 通知訊息的應用程式應該刪除訊息隨附的所有原子。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-132">The application that receives a **WM\_DDE\_ACK** message should delete all atoms accompanying the message.</span></span> <span data-ttu-id="a4ab5-133">如果應用程式接收了 **WM \_ DDE \_** 通知，以回應具有伴隨全域記憶體物件的訊息，而且物件是以 **FRelease** 旗標設定為 **FALSE** 來傳送，則應用程式會負責刪除物件。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-133">If the application receives a **WM\_DDE\_ACK** in response to a message with an accompanying global memory object, and the object was sent with the **fRelease** flags set to **FALSE**, the application is responsible for deleting the object.</span></span>

<span data-ttu-id="a4ab5-134">如果應用程式收到回傳至 [**wm \_ dde \_ 建議**](wm-dde-advise.md)訊息的負 **wm \_ dde dde \_ ACK** 訊息，應用程式應該刪除以原始的 **wm \_ dde \_ 建議** 訊息張貼的全域記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-134">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_ADVISE** message.</span></span> <span data-ttu-id="a4ab5-135">如果應用程式收到回傳至 [**wm \_ dde \_ 資料**](wm-dde-data.md)、 [**wm \_ dde \_**](wm-dde-poke.md)傳送或 [**wm \_ dde \_ 執行**](wm-dde-execute.md)訊息的負 **WM \_ dde \_** 通知訊息，應用程式應該刪除以原始 **WM \_ dde \_ 資料**、 **wm \_ dde \_** 傳送或 **wm dde \_ \_ 執行** 訊息張貼的全域記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-135">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_POKE**](wm-dde-poke.md), or [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_DATA**, **WM\_DDE\_POKE**, or **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="a4ab5-136">接收已張貼之 **WM \_ DDE \_ ACK** 訊息的應用程式，必須使用 [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)函數釋放 *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="a4ab5-136">The application that receives a posted **WM\_DDE\_ACK** message must free the *lParam* parameter by using the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4ab5-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4ab5-137">Requirements</span></span>



| <span data-ttu-id="a4ab5-138">需求</span><span class="sxs-lookup"><span data-stu-id="a4ab5-138">Requirement</span></span> | <span data-ttu-id="a4ab5-139">值</span><span class="sxs-lookup"><span data-stu-id="a4ab5-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4ab5-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4ab5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a4ab5-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4ab5-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a4ab5-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4ab5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a4ab5-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4ab5-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a4ab5-144">標頭</span><span class="sxs-lookup"><span data-stu-id="a4ab5-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4ab5-145"><dt> (包含 Windows. h) </dt></span><span class="sxs-lookup"><span data-stu-id="a4ab5-145"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4ab5-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4ab5-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="a4ab5-147">**參考**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a4ab5-148">**DDEACK**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-148">**DDEACK**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[<span data-ttu-id="a4ab5-149">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-149">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="a4ab5-150">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-150">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="a4ab5-151">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-151">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="a4ab5-152">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-152">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="a4ab5-153">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-153">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="a4ab5-154">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-154">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="a4ab5-155">**WM \_ DDE \_ 建議**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-155">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="a4ab5-156">**WM \_ DDE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-156">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="a4ab5-157">**WM \_ DDE \_ 執行**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-157">**WM\_DDE\_EXECUTE**</span></span>](wm-dde-execute.md)
</dt> <dt>

[<span data-ttu-id="a4ab5-158">**WM \_ DDE \_ 起始**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-158">**WM\_DDE\_INITIATE**</span></span>](wm-dde-initiate.md)
</dt> <dt>

[<span data-ttu-id="a4ab5-159">**WM \_ DDE 的進行 \_**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-159">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="a4ab5-160">**WM \_ DDE \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-160">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

[<span data-ttu-id="a4ab5-161">**WM \_ DDE \_ 終止**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-161">**WM\_DDE\_TERMINATE**</span></span>](wm-dde-terminate.md)
</dt> <dt>

[<span data-ttu-id="a4ab5-162">**WM \_ DDE \_ UNADVISE**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-162">**WM\_DDE\_UNADVISE**</span></span>](wm-dde-unadvise.md)
</dt> <dt>

<span data-ttu-id="a4ab5-163">**概念**</span><span class="sxs-lookup"><span data-stu-id="a4ab5-163">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a4ab5-164">關於動態資料交換</span><span class="sxs-lookup"><span data-stu-id="a4ab5-164">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


---
title: 'WM_DDE_ADVISE 訊息 (的) '
description: 動態資料交換 (DDE) 用戶端應用程式會將 WM \_ DDE \_ 建議訊息張貼至 dde 伺服器應用程式，要求伺服器在專案變更時，提供資料項目的更新。
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- WM_DDE_ADVISE 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094467"
---
# <a name="wm_dde_advise-message"></a><span data-ttu-id="c93e9-104">WM \_ DDE \_ 建議訊息</span><span class="sxs-lookup"><span data-stu-id="c93e9-104">WM\_DDE\_ADVISE message</span></span>

<span data-ttu-id="c93e9-105">動態資料交換 (DDE) 用戶端應用程式會將 **WM \_ DDE \_ 建議** 訊息張貼至 dde 伺服器應用程式，要求伺服器在專案變更時，提供資料項目的更新。</span><span class="sxs-lookup"><span data-stu-id="c93e9-105">A Dynamic Data Exchange (DDE) client application posts the **WM\_DDE\_ADVISE** message to a DDE server application to request the server to supply an update for a data item whenever the item changes.</span></span>

<span data-ttu-id="c93e9-106">若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。</span><span class="sxs-lookup"><span data-stu-id="c93e9-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a><span data-ttu-id="c93e9-107">參數</span><span class="sxs-lookup"><span data-stu-id="c93e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c93e9-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c93e9-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c93e9-109">張貼訊息之用戶端視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c93e9-109">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="c93e9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c93e9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c93e9-111">低序位單字是全域記憶體物件的控制碼，其中包含指定如何傳送資料的 [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) 結構。</span><span class="sxs-lookup"><span data-stu-id="c93e9-111">The low-order word is a handle to a global memory object containing a [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) structure that specifies how the data is to be sent.</span></span>

<span data-ttu-id="c93e9-112">高序位字包含識別所要求資料項目的 atom。</span><span class="sxs-lookup"><span data-stu-id="c93e9-112">The high-order word contains an atom that identifies the requested data item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c93e9-113">備註</span><span class="sxs-lookup"><span data-stu-id="c93e9-113">Remarks</span></span>

<span data-ttu-id="c93e9-114">如果用戶端應用程式支援單一主題和專案的多個剪貼簿格式，它可以張貼主題和專案的多個 **WM \_ DDE \_ 建議** 訊息，並指定每個訊息的不同剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="c93e9-114">If a client application supports more than one clipboard format for a single topic and item, it can post multiple **WM\_DDE\_ADVISE** messages for the topic and item, specifying a different clipboard format with each message.</span></span> <span data-ttu-id="c93e9-115">請注意，伺服器只能針對經常性存取資料連結支援多種格式，而不支援暖資料連結。</span><span class="sxs-lookup"><span data-stu-id="c93e9-115">Note that a server can support multiple formats only for hot data links, not warm data links.</span></span>

### <a name="posting"></a><span data-ttu-id="c93e9-116">張貼</span><span class="sxs-lookup"><span data-stu-id="c93e9-116">Posting</span></span>

<span data-ttu-id="c93e9-117">用戶端應用程式會呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)函式，而不是 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)函式，以張貼 **WM \_ DDE \_ 建議** 訊息。</span><span class="sxs-lookup"><span data-stu-id="c93e9-117">The client application posts the **WM\_DDE\_ADVISE** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="c93e9-118">用戶端應用程式會使用 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) 函數來配置全域記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="c93e9-118">The client application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="c93e9-119">它會使用 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 函數來配置 atom。</span><span class="sxs-lookup"><span data-stu-id="c93e9-119">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="c93e9-120">用戶端應用程式必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數，來建立或重複使用 **WM \_ DDE \_ 建議** *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="c93e9-120">The client application must create or reuse the **WM\_DDE\_ADVISE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="c93e9-121">如果接收 (伺服器) 應用程式以負的 [**WM \_ DDE \_ 確認**](wm-dde-ack.md) 訊息回應，則張貼應用程式必須刪除物件。</span><span class="sxs-lookup"><span data-stu-id="c93e9-121">If the receiving (server) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting application must delete the object.</span></span>

<span data-ttu-id="c93e9-122">**FRelease** 旗標不會用於 **wm \_ dde \_ 建議** 訊息中，但其資料釋出行為類似于 [**wm \_ Dde \_ 資料**](wm-dde-data.md)和 [**wm \_ dde \_**](wm-dde-poke.md)訊息（其中 **fRelease** 為 **TRUE**）。</span><span class="sxs-lookup"><span data-stu-id="c93e9-122">The **fRelease** flag is not used in **WM\_DDE\_ADVISE** messages, but their data-freeing behavior is similar to that of [**WM\_DDE\_DATA**](wm-dde-data.md) and [**WM\_DDE\_POKE**](wm-dde-poke.md) messages where **fRelease** is **TRUE**.</span></span>

### <a name="receiving"></a><span data-ttu-id="c93e9-123">接收</span><span class="sxs-lookup"><span data-stu-id="c93e9-123">Receiving</span></span>

<span data-ttu-id="c93e9-124">伺服器應用程式會張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，以回應正面或負面。</span><span class="sxs-lookup"><span data-stu-id="c93e9-124">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="c93e9-125">張貼 **WM \_ DDE \_** 通知時，應用程式可以重複使用 atom 或將它刪除，然後建立一個新的。</span><span class="sxs-lookup"><span data-stu-id="c93e9-125">When posting **WM\_DDE\_ACK**, the application can reuse the atom or delete it and create a new one.</span></span> <span data-ttu-id="c93e9-126">如果 **WM \_ DDE \_** 通知訊息是正數，則應用程式應該刪除全域記憶體物件，否則應用程式不應該刪除物件。</span><span class="sxs-lookup"><span data-stu-id="c93e9-126">If the **WM\_DDE\_ACK** message is positive, the application should delete the global memory object; otherwise, the application should not delete the object.</span></span>

<span data-ttu-id="c93e9-127">伺服器必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數，來建立或重複使用 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="c93e9-127">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c93e9-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c93e9-128">Requirements</span></span>



| <span data-ttu-id="c93e9-129">需求</span><span class="sxs-lookup"><span data-stu-id="c93e9-129">Requirement</span></span> | <span data-ttu-id="c93e9-130">值</span><span class="sxs-lookup"><span data-stu-id="c93e9-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c93e9-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c93e9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c93e9-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c93e9-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c93e9-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c93e9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c93e9-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c93e9-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c93e9-135">標頭</span><span class="sxs-lookup"><span data-stu-id="c93e9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c93e9-136"><dt> (包含 Windows. h) </dt></span><span class="sxs-lookup"><span data-stu-id="c93e9-136"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93e9-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c93e9-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="c93e9-138">**參考**</span><span class="sxs-lookup"><span data-stu-id="c93e9-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c93e9-139">**DDEADVISE**</span><span class="sxs-lookup"><span data-stu-id="c93e9-139">**DDEADVISE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[<span data-ttu-id="c93e9-140">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="c93e9-140">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="c93e9-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="c93e9-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="c93e9-142">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="c93e9-142">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="c93e9-143">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="c93e9-143">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="c93e9-144">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="c93e9-144">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="c93e9-145">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="c93e9-145">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="c93e9-146">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="c93e9-146">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="c93e9-147">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="c93e9-147">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="c93e9-148">**WM \_ DDE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c93e9-148">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="c93e9-149">**WM \_ DDE 的進行 \_**</span><span class="sxs-lookup"><span data-stu-id="c93e9-149">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="c93e9-150">**WM \_ DDE \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="c93e9-150">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="c93e9-151">**概念**</span><span class="sxs-lookup"><span data-stu-id="c93e9-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c93e9-152">關於動態資料交換</span><span class="sxs-lookup"><span data-stu-id="c93e9-152">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


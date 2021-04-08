---
title: 'WM_DDE_POKE 訊息 (的) '
description: 動態資料交換 (的 DDE) 用戶端應用程式會將 WM \_ DDE \_ 郵件訊息張貼至 DDE 伺服器應用程式。
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- WM_DDE_POKE 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686524"
---
# <a name="wm_dde_poke-message"></a><span data-ttu-id="441df-104">WM \_ DDE \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="441df-104">WM\_DDE\_POKE message</span></span>

<span data-ttu-id="441df-105">動態資料交換 (的 DDE) 用戶端應用程式會將 **WM \_ DDE \_** 郵件訊息張貼至 DDE 伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="441df-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_POKE** message to a DDE server application.</span></span> <span data-ttu-id="441df-106">用戶端會使用此訊息要求伺服器接受未請求的資料項目。</span><span class="sxs-lookup"><span data-stu-id="441df-106">A client uses this message to request the server to accept an unsolicited data item.</span></span> <span data-ttu-id="441df-107">伺服器預期會以 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息來回複，指出它是否接受該資料項目。</span><span class="sxs-lookup"><span data-stu-id="441df-107">The server is expected to reply with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message indicating whether it accepted the data item.</span></span>

<span data-ttu-id="441df-108">若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。</span><span class="sxs-lookup"><span data-stu-id="441df-108">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a><span data-ttu-id="441df-109">參數</span><span class="sxs-lookup"><span data-stu-id="441df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="441df-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="441df-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="441df-111">張貼訊息之用戶端視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="441df-111">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="441df-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="441df-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="441df-113">低序位單字是全域記憶體物件的控制碼，其中包含具有資料和其他資訊的 [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) 結構。</span><span class="sxs-lookup"><span data-stu-id="441df-113">The low-order word is a handle to a global memory object containing a [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) structure with the data and additional information.</span></span>

<span data-ttu-id="441df-114">高序位單字包含全域 atom，可識別要傳送資料或通知的資料項目。</span><span class="sxs-lookup"><span data-stu-id="441df-114">The high-order word contains a global atom that identifies the data item for which the data or notification is being sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="441df-115">備註</span><span class="sxs-lookup"><span data-stu-id="441df-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="441df-116">張貼</span><span class="sxs-lookup"><span data-stu-id="441df-116">Posting</span></span>

<span data-ttu-id="441df-117">用戶端應用程式必須使用 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) 函式來配置全域記憶體物件的記憶體。</span><span class="sxs-lookup"><span data-stu-id="441df-117">The client application must allocate memory for the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="441df-118">如果下列任一條件成立，用戶端應用程式必須刪除物件：</span><span class="sxs-lookup"><span data-stu-id="441df-118">The client application must delete the object if either of the following conditions is true:</span></span>

-   <span data-ttu-id="441df-119">伺服器應用程式會以負的 [**WM \_ DDE \_ 確認**](wm-dde-ack.md) 訊息來回應。</span><span class="sxs-lookup"><span data-stu-id="441df-119">The server application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>
-   <span data-ttu-id="441df-120">**FRelease** 成員為 **FALSE**，但伺服器應用程式會以正面或負的 WM 的 [**WM \_ DDE \_ ACK**](wm-dde-ack.md)來回應。</span><span class="sxs-lookup"><span data-stu-id="441df-120">The **fRelease** member is **FALSE**, but the server application responds with either a positive or negative [**WM\_DDE\_ACK**](wm-dde-ack.md).</span></span>

<span data-ttu-id="441df-121">用戶端應用程式必須使用 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 函數來建立 atom。</span><span class="sxs-lookup"><span data-stu-id="441df-121">The client application must create the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="441df-122">用戶端應用程式必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函式，來建立或重複使用 **WM \_ \_ DDE** 的 *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="441df-122">The client application must create or reuse the **WM\_DDE\_POKE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="441df-123">接收</span><span class="sxs-lookup"><span data-stu-id="441df-123">Receiving</span></span>

<span data-ttu-id="441df-124">伺服器應用程式應該張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，以回應正面或負面。</span><span class="sxs-lookup"><span data-stu-id="441df-124">The server application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="441df-125">在張貼 **WM \_ DDE \_** 通知時，伺服器可以重複使用 atom，也可以將它刪除並建立一個新的。</span><span class="sxs-lookup"><span data-stu-id="441df-125">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="441df-126">伺服器必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數，來建立或重複使用 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="441df-126">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="441df-127">若要釋放全域記憶體物件，伺服器應該呼叫 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函數。</span><span class="sxs-lookup"><span data-stu-id="441df-127">To free the global memory object, the server should call the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="441df-128">此外，如果資料格式為 [**cf \_ DSPMETAFILEPICT**](clipboard-formats.md) 或 **cf \_ METAFILEPICT**，則伺服器也必須使用內嵌的中繼檔控制碼來呼叫 [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) 。</span><span class="sxs-lookup"><span data-stu-id="441df-128">Also, if the data format is either [**CF\_DSPMETAFILEPICT**](clipboard-formats.md) or **CF\_METAFILEPICT**, the server must also call [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) with the embedded metafile handle.</span></span> <span data-ttu-id="441df-129">這兩種格式具有額外的間接取值層級;亦即，應用程式必須鎖定物件以取得控制碼的指標，然後鎖定該控制碼以取得 [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict)結構的指標，最後使用 **METAFILEPICT** 結構 **hMF** 成員的控制碼來呼叫 **DeleteMetaFile** 。</span><span class="sxs-lookup"><span data-stu-id="441df-129">These two formats have an extra level of indirection; that is, an application must lock the object to get a pointer to a handle, then lock that handle to get a pointer to a [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) structure, and finally call **DeleteMetaFile** with the handle from the **hMF** member of the **METAFILEPICT** structure.</span></span>

<span data-ttu-id="441df-130">若要釋放物件，伺服器應該呼叫 [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) 函數。</span><span class="sxs-lookup"><span data-stu-id="441df-130">To free the object, the server should call the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="441df-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="441df-131">Requirements</span></span>



| <span data-ttu-id="441df-132">需求</span><span class="sxs-lookup"><span data-stu-id="441df-132">Requirement</span></span> | <span data-ttu-id="441df-133">值</span><span class="sxs-lookup"><span data-stu-id="441df-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="441df-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="441df-134">Minimum supported client</span></span><br/> | <span data-ttu-id="441df-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="441df-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="441df-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="441df-136">Minimum supported server</span></span><br/> | <span data-ttu-id="441df-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="441df-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="441df-138">標頭</span><span class="sxs-lookup"><span data-stu-id="441df-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="441df-139"><dt> (包含 Windows. h) </dt></span><span class="sxs-lookup"><span data-stu-id="441df-139"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="441df-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="441df-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="441df-141">**參考**</span><span class="sxs-lookup"><span data-stu-id="441df-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="441df-142">**DDEPOKE**</span><span class="sxs-lookup"><span data-stu-id="441df-142">**DDEPOKE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[<span data-ttu-id="441df-143">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="441df-143">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="441df-144">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="441df-144">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="441df-145">**METAFILEPICT**</span><span class="sxs-lookup"><span data-stu-id="441df-145">**METAFILEPICT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
</dt> <dt>

[<span data-ttu-id="441df-146">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="441df-146">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="441df-147">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="441df-147">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="441df-148">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="441df-148">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="441df-149">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="441df-149">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="441df-150">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="441df-150">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="441df-151">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="441df-151">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="441df-152">**概念**</span><span class="sxs-lookup"><span data-stu-id="441df-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="441df-153">關於動態資料交換</span><span class="sxs-lookup"><span data-stu-id="441df-153">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


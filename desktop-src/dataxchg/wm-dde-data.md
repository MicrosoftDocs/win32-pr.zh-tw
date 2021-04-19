---
title: 'WM_DDE_DATA 訊息 (的) '
description: 動態資料交換 (DDE) server 應用程式將 WM \_ DDE 的 \_ 資料訊息張貼至 dde 用戶端應用程式，以將資料項目傳遞給用戶端，或通知用戶端資料項目目的可用性。
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- WM_DDE_DATA 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966307"
---
# <a name="wm_dde_data-message"></a><span data-ttu-id="aaa10-104">WM \_ DDE \_ 資料訊息</span><span class="sxs-lookup"><span data-stu-id="aaa10-104">WM\_DDE\_DATA message</span></span>

<span data-ttu-id="aaa10-105">動態資料交換 (DDE) server 應用程式將 **WM \_ DDE 的 \_ 資料** 訊息張貼至 dde 用戶端應用程式，以將資料項目傳遞給用戶端，或通知用戶端資料項目目的可用性。</span><span class="sxs-lookup"><span data-stu-id="aaa10-105">A Dynamic Data Exchange (DDE) server application posts a **WM\_DDE\_DATA** message to a DDE client application to pass a data item to the client or to notify the client of the availability of a data item.</span></span>

<span data-ttu-id="aaa10-106">若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。</span><span class="sxs-lookup"><span data-stu-id="aaa10-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a><span data-ttu-id="aaa10-107">參數</span><span class="sxs-lookup"><span data-stu-id="aaa10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa10-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aaa10-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaa10-109">張貼訊息之伺服器視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="aaa10-109">A handle to the server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="aaa10-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aaa10-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaa10-111">低序位單字是全域記憶體物件的控制碼，其中包含具有資料和其他資訊的 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) 結構。</span><span class="sxs-lookup"><span data-stu-id="aaa10-111">The low-order word is a handle to a global memory object containing a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure with the data and additional information.</span></span> <span data-ttu-id="aaa10-112">如果伺服器通知用戶端資料項目目值在暖資料連結期間已變更，則此控制碼應該設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="aaa10-112">The handle should be set to **NULL** if the server is notifying the client that the data-item value has changed during a warm data link.</span></span> <span data-ttu-id="aaa10-113">用戶端會建立一個暖連結，而用戶端會使用 **fDeferUpd** 位組來傳送 [**WM \_ DDE \_ 建議**](wm-dde-advise.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="aaa10-113">A warm link is established by the client sending a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message with the **fDeferUpd** bit set.</span></span>

<span data-ttu-id="aaa10-114">高序位字組包含 atom，可識別資料或通知傳送至的資料項目。</span><span class="sxs-lookup"><span data-stu-id="aaa10-114">The high-order word contains an atom that identifies the data item for which the data or notification is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aaa10-115">備註</span><span class="sxs-lookup"><span data-stu-id="aaa10-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="aaa10-116">張貼</span><span class="sxs-lookup"><span data-stu-id="aaa10-116">Posting</span></span>

<span data-ttu-id="aaa10-117">伺服器應用程式會使用 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) 函數來配置全域記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="aaa10-117">The server application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="aaa10-118">它會使用 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 函數來配置 atom。</span><span class="sxs-lookup"><span data-stu-id="aaa10-118">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="aaa10-119">伺服器必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數，來建立或重複使用 **WM \_ DDE \_ DATA** *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="aaa10-119">The server must create or reuse the **WM\_DDE\_DATA** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="aaa10-120">如果接收 (用戶端) 應用程式以負的 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息回應，則張貼 (伺服器) 應用程式必須刪除全域記憶體物件; 否則，用戶端必須藉由呼叫 [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) 函式來將物件解壓縮之後，才能刪除該物件。</span><span class="sxs-lookup"><span data-stu-id="aaa10-120">If the receiving (client) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting (server) application must delete the global memory object; otherwise, the client must delete the object after extracting its contents by calling the [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) function.</span></span>

<span data-ttu-id="aaa10-121">如果伺服器應用程式將 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)結構的 **fRelease** 成員設定為 **FALSE**，則伺服器會負責在接收正面或負認可時刪除物件。</span><span class="sxs-lookup"><span data-stu-id="aaa10-121">If the server application sets the **fRelease** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**, the server is responsible for deleting the object upon receiving either a positive or negative acknowledgment.</span></span>

<span data-ttu-id="aaa10-122">伺服器應用程式不應該將 [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)結構的 **fAckReq** 和 **FRelease** 成員都設為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="aaa10-122">The server application should not set both the **fAckReq** and **fRelease** members of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**.</span></span> <span data-ttu-id="aaa10-123">如果這兩個成員都設定為 **FALSE**，則伺服器無法判斷何時刪除該物件。</span><span class="sxs-lookup"><span data-stu-id="aaa10-123">If both members are set to **FALSE**, it is impossible for the server to determine when to delete the object.</span></span>

### <a name="receiving"></a><span data-ttu-id="aaa10-124">接收</span><span class="sxs-lookup"><span data-stu-id="aaa10-124">Receiving</span></span>

<span data-ttu-id="aaa10-125">如果 **fAckReq** 為 **TRUE**，用戶端應用程式應該張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，以回應正面或負面。</span><span class="sxs-lookup"><span data-stu-id="aaa10-125">If **fAckReq** is **TRUE**, the client application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="aaa10-126">張貼 **WM \_ DDE DDE \_ ACK** 時，用戶端可以重複使用 atom，也可以刪除它並建立新的。</span><span class="sxs-lookup"><span data-stu-id="aaa10-126">When posting **WM\_DDE\_ACK**, the client can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="aaa10-127">用戶端必須藉由呼叫 [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)函數或 [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)函數來建立或重複使用 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="aaa10-127">The client must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="aaa10-128">如果 **fAckReq** 為 **FALSE**，用戶端應用程式應該刪除 atom。</span><span class="sxs-lookup"><span data-stu-id="aaa10-128">If **fAckReq** is **FALSE**, the client application should delete the atom.</span></span>

<span data-ttu-id="aaa10-129">如果張貼應用程式將全域記憶體物件指定為 **Null**，則接收應用程式可以藉由張貼 [**WM \_ DDE \_ 要求**](wm-dde-request.md) 訊息來要求伺服器傳送資料。</span><span class="sxs-lookup"><span data-stu-id="aaa10-129">If the posting application specified global memory object as **NULL**, the receiving application can request the server to send the data by posting a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message.</span></span>

<span data-ttu-id="aaa10-130">處理在全域記憶體物件不是 **Null** 的 **WM \_ DDE \_ 資料** 訊息之後，除非下列其中一個條件成立，否則用戶端應該釋放物件：</span><span class="sxs-lookup"><span data-stu-id="aaa10-130">After processing a **WM\_DDE\_DATA** message in which the global memory object is not **NULL**, the client should free the object, unless one of the following conditions is true:</span></span>

-   <span data-ttu-id="aaa10-131">**FRelease** 成員為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="aaa10-131">The **fRelease** member is **FALSE**.</span></span>
-   <span data-ttu-id="aaa10-132">**FRelease** 成員是 **TRUE**，但用戶端應用程式會以負的 [**WM \_ DDE \_**](wm-dde-ack.md)通知訊息來回應。</span><span class="sxs-lookup"><span data-stu-id="aaa10-132">The **fRelease** member is **TRUE**, but the client application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa10-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="aaa10-133">Requirements</span></span>



| <span data-ttu-id="aaa10-134">需求</span><span class="sxs-lookup"><span data-stu-id="aaa10-134">Requirement</span></span> | <span data-ttu-id="aaa10-135">值</span><span class="sxs-lookup"><span data-stu-id="aaa10-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa10-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aaa10-136">Minimum supported client</span></span><br/> | <span data-ttu-id="aaa10-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aaa10-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aaa10-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aaa10-138">Minimum supported server</span></span><br/> | <span data-ttu-id="aaa10-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aaa10-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aaa10-140">標頭</span><span class="sxs-lookup"><span data-stu-id="aaa10-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaa10-141"><dt> (包含 Windows. h) </dt></span><span class="sxs-lookup"><span data-stu-id="aaa10-141"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaa10-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aaa10-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="aaa10-143">**參考**</span><span class="sxs-lookup"><span data-stu-id="aaa10-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aaa10-144">**DDEDATA**</span><span class="sxs-lookup"><span data-stu-id="aaa10-144">**DDEDATA**</span></span>](/windows/desktop/api/Dde/ns-dde-ddedata)
</dt> <dt>

[<span data-ttu-id="aaa10-145">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="aaa10-145">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="aaa10-146">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="aaa10-146">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="aaa10-147">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="aaa10-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="aaa10-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="aaa10-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="aaa10-149">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="aaa10-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="aaa10-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="aaa10-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="aaa10-151">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="aaa10-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="aaa10-152">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="aaa10-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="aaa10-153">**WM \_ DDE \_ 建議**</span><span class="sxs-lookup"><span data-stu-id="aaa10-153">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="aaa10-154">**WM \_ DDE 的進行 \_**</span><span class="sxs-lookup"><span data-stu-id="aaa10-154">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="aaa10-155">**WM \_ DDE \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="aaa10-155">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="aaa10-156">**概念**</span><span class="sxs-lookup"><span data-stu-id="aaa10-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aaa10-157">關於動態資料交換</span><span class="sxs-lookup"><span data-stu-id="aaa10-157">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


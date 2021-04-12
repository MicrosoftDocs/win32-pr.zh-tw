---
title: 'WM_DDE_INITIATE 訊息 (的) '
description: 動態資料交換 (DDE) 用戶端應用程式傳送 WM \_ dde \_ 的初始訊息，以起始與伺服器應用程式的交談，回應指定的應用程式和主題名稱。
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36485db262c46d5364ee0ee26e7e6f39ccf0e677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384518"
---
# <a name="wm_dde_initiate-message"></a><span data-ttu-id="4d439-104">WM \_ DDE \_ 起始訊息</span><span class="sxs-lookup"><span data-stu-id="4d439-104">WM\_DDE\_INITIATE message</span></span>

<span data-ttu-id="4d439-105">動態資料交換 (DDE) 用戶端應用程式傳送 **WM \_ dde 的 \_ 初始** 訊息，以起始與伺服器應用程式的交談，回應指定的應用程式和主題名稱。</span><span class="sxs-lookup"><span data-stu-id="4d439-105">A Dynamic Data Exchange (DDE) client application sends a **WM\_DDE\_INITIATE** message to initiate a conversation with a server application responding to the specified application and topic names.</span></span> <span data-ttu-id="4d439-106">收到此訊息時，所有名稱符合指定之應用程式且支援指定主題的伺服器應用程式，都應該要知道它。</span><span class="sxs-lookup"><span data-stu-id="4d439-106">Upon receiving this message, all server applications with names that match the specified application and that support the specified topic are expected to acknowledge it.</span></span> <span data-ttu-id="4d439-107"> (需詳細資訊，請參閱 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) 訊息。 ) </span><span class="sxs-lookup"><span data-stu-id="4d439-107">(For more information, see the [**WM\_DDE\_ACK**](wm-dde-ack.md) message.)</span></span>


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a><span data-ttu-id="4d439-108">參數</span><span class="sxs-lookup"><span data-stu-id="4d439-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d439-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d439-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d439-110">傳送訊息之用戶端視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4d439-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="4d439-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d439-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d439-112">低序位字組包含 atom，用來識別要求交談的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4d439-112">The low-order word contains an atom that identifies the application with which a conversation is requested.</span></span> <span data-ttu-id="4d439-113">應用程式名稱不能包含斜線 (/) 或反斜線 (\) 。</span><span class="sxs-lookup"><span data-stu-id="4d439-113">The application name cannot contain slashes (/) or backslashes (\).</span></span> <span data-ttu-id="4d439-114">這些字元會保留給網路執行。</span><span class="sxs-lookup"><span data-stu-id="4d439-114">These characters are reserved for network implementations.</span></span> <span data-ttu-id="4d439-115">如果此參數為 **Null**，則會要求與所有應用程式的交談。</span><span class="sxs-lookup"><span data-stu-id="4d439-115">If this parameter is **NULL**, a conversation with all applications is requested.</span></span>

<span data-ttu-id="4d439-116">高序位單字包含的 atom 會識別要求交談的主題。</span><span class="sxs-lookup"><span data-stu-id="4d439-116">The high-order word contains an atom that identifies the topic for which a conversation is requested.</span></span> <span data-ttu-id="4d439-117">如果主題為 **Null**，則會要求所有可用主題的交談。</span><span class="sxs-lookup"><span data-stu-id="4d439-117">If the topic is **NULL**, conversations for all available topics are requested.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d439-118">備註</span><span class="sxs-lookup"><span data-stu-id="4d439-118">Remarks</span></span>

<span data-ttu-id="4d439-119">如果 *lParam* 的低序位字是 **Null**，任何伺服器應用程式都可以回應。</span><span class="sxs-lookup"><span data-stu-id="4d439-119">If the low-order word of *lParam* is **NULL**, any server application can respond.</span></span> <span data-ttu-id="4d439-120">如果 *lParam* 的高序位字是 **Null**，則任何主題都有效。</span><span class="sxs-lookup"><span data-stu-id="4d439-120">If the high-order word of *lParam* is **NULL**, any topic is valid.</span></span> <span data-ttu-id="4d439-121">在收到具有 *lParam* 參數高序位字組的 **wm \_ dde \_ 起始** 要求 **時，伺服器** 必須針對它所支援的每個主題傳送 [**wm \_ dde \_ ACK**](wm-dde-ack.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="4d439-121">Upon receiving a **WM\_DDE\_INITIATE** request with the high-order word of the *lParam* parameter set to **NULL**, a server must send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each of the topics it supports.</span></span>

### <a name="sending"></a><span data-ttu-id="4d439-122">傳送</span><span class="sxs-lookup"><span data-stu-id="4d439-122">Sending</span></span>

<span data-ttu-id="4d439-123">用戶端會將 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 的第一個參數設定為 **HWND \_ 廣播**，以將訊息廣播到所有最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="4d439-123">The client broadcasts the message to all top-level windows by setting the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="4d439-124">如果用戶端應用程式已經取得所需伺服器的視窗控制碼，它可以將伺服器的視窗控制碼傳遞為 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)的第一個參數，以將該伺服器的視窗控制碼直接傳送到伺服器視窗。 **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="4d439-124">If the client application has already obtained the window handle of the desired server, it can send **WM\_DDE\_INITIATE** directly to the server window by passing the server's window handle as the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span>

<span data-ttu-id="4d439-125">用戶端應用程式會藉由呼叫 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) 函數來配置原子。</span><span class="sxs-lookup"><span data-stu-id="4d439-125">The client application allocates atoms by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="4d439-126">當 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 傳回時，用戶端應用程式必須刪除原子。</span><span class="sxs-lookup"><span data-stu-id="4d439-126">When [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application must delete the atoms.</span></span>

### <a name="receiving"></a><span data-ttu-id="4d439-127">接收</span><span class="sxs-lookup"><span data-stu-id="4d439-127">Receiving</span></span>

<span data-ttu-id="4d439-128">若要完成對話的起始，伺服器應用程式必須回應一或多個 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，其中每個訊息都是針對個別的主題。</span><span class="sxs-lookup"><span data-stu-id="4d439-128">To complete the initiation of a conversation, the server application must respond with one or more [**WM\_DDE\_ACK**](wm-dde-ack.md) messages, where each message is for a separate topic.</span></span> <span data-ttu-id="4d439-129">傳送 **wm \_ dde \_** 通知訊息時，伺服器應該建立新的原子，不應重複使用與 **WM \_ DDE \_ 起始** 一起傳送的原子。</span><span class="sxs-lookup"><span data-stu-id="4d439-129">When sending **WM\_DDE\_ACK** message, the server should create new atoms; it should not reuse the atoms sent with **WM\_DDE\_INITIATE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d439-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d439-130">Requirements</span></span>



| <span data-ttu-id="4d439-131">需求</span><span class="sxs-lookup"><span data-stu-id="4d439-131">Requirement</span></span> | <span data-ttu-id="4d439-132">值</span><span class="sxs-lookup"><span data-stu-id="4d439-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d439-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d439-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4d439-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d439-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4d439-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d439-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4d439-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d439-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4d439-137">標頭</span><span class="sxs-lookup"><span data-stu-id="4d439-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d439-138"><dt> (包含 Windows. h) </dt></span><span class="sxs-lookup"><span data-stu-id="4d439-138"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d439-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d439-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="4d439-140">**參考**</span><span class="sxs-lookup"><span data-stu-id="4d439-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4d439-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="4d439-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="4d439-142">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="4d439-142">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="4d439-143">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="4d439-143">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="4d439-144">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="4d439-144">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="4d439-145">**概念**</span><span class="sxs-lookup"><span data-stu-id="4d439-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4d439-146">關於動態資料交換</span><span class="sxs-lookup"><span data-stu-id="4d439-146">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


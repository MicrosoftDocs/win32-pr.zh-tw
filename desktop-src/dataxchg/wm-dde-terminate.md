---
title: 'WM_DDE_TERMINATE 訊息 (的) '
description: 動態資料交換 (DDE) 應用程式 (用戶端或伺服器) 張貼 WM \_ DDE \_ 終止訊息以終止交談。 若要張貼此訊息，請使用下列參數呼叫 PostMessage 函數。
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094363"
---
# <a name="wm_dde_terminate-message"></a><span data-ttu-id="8aa60-105">WM \_ DDE \_ 終止訊息</span><span class="sxs-lookup"><span data-stu-id="8aa60-105">WM\_DDE\_TERMINATE message</span></span>

<span data-ttu-id="8aa60-106">動態資料交換 (DDE) 應用程式 (用戶端或伺服器) 張貼 **WM \_ DDE \_ 終止** 訊息以終止交談。</span><span class="sxs-lookup"><span data-stu-id="8aa60-106">A Dynamic Data Exchange (DDE) application (client or server) posts a **WM\_DDE\_TERMINATE** message to terminate a conversation.</span></span>

<span data-ttu-id="8aa60-107">若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。</span><span class="sxs-lookup"><span data-stu-id="8aa60-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a><span data-ttu-id="8aa60-108">參數</span><span class="sxs-lookup"><span data-stu-id="8aa60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aa60-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8aa60-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8aa60-110">張貼訊息之用戶端或伺服器視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8aa60-110">A handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="8aa60-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8aa60-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8aa60-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="8aa60-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8aa60-113">備註</span><span class="sxs-lookup"><span data-stu-id="8aa60-113">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="8aa60-114">張貼</span><span class="sxs-lookup"><span data-stu-id="8aa60-114">Posting</span></span>

<span data-ttu-id="8aa60-115">在等候確認終止時，張貼應用程式不應該將任何其他訊息張貼至接收應用程式。</span><span class="sxs-lookup"><span data-stu-id="8aa60-115">While waiting for confirmation of the termination, the posting application should not post any other messages to the receiving application.</span></span> <span data-ttu-id="8aa60-116">如果傳送的應用程式接收到來自接收應用程式的 (**WM \_ DDE \_ TERMINATE**) 以外的訊息，則應該刪除伴隨于訊息的任何原子或共用記憶體物件，但不包括與未設定 **fRelease** 成員之 [**wm \_ dde \_**](wm-dde-poke.md)郵件或 [**wm \_ dde \_ 資料**](wm-dde-data.md)訊息相關聯的全域記憶體物件。</span><span class="sxs-lookup"><span data-stu-id="8aa60-116">If the sending application receives messages (other than **WM\_DDE\_TERMINATE**) from the receiving application, it should delete any atoms or shared memory objects accompanying the messages, except global memory objects associated with [**WM\_DDE\_POKE**](wm-dde-poke.md) or [**WM\_DDE\_DATA**](wm-dde-data.md) messages that do not have the **fRelease** member set.</span></span>

### <a name="receiving"></a><span data-ttu-id="8aa60-117">接收</span><span class="sxs-lookup"><span data-stu-id="8aa60-117">Receiving</span></span>

<span data-ttu-id="8aa60-118">用戶端或伺服器應用程式應藉由公佈 **WM \_ DDE \_ 終止** 訊息來回應。</span><span class="sxs-lookup"><span data-stu-id="8aa60-118">The client or server application should respond by posting a **WM\_DDE\_TERMINATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa60-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8aa60-119">Requirements</span></span>



| <span data-ttu-id="8aa60-120">需求</span><span class="sxs-lookup"><span data-stu-id="8aa60-120">Requirement</span></span> | <span data-ttu-id="8aa60-121">值</span><span class="sxs-lookup"><span data-stu-id="8aa60-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa60-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8aa60-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8aa60-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8aa60-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8aa60-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8aa60-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8aa60-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8aa60-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8aa60-126">標頭</span><span class="sxs-lookup"><span data-stu-id="8aa60-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aa60-127"><dt> (包含 Windows. h) </dt></span><span class="sxs-lookup"><span data-stu-id="8aa60-127"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa60-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8aa60-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="8aa60-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="8aa60-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8aa60-130">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="8aa60-130">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="8aa60-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="8aa60-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="8aa60-132">**WM \_ DDE \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="8aa60-132">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="8aa60-133">**WM \_ DDE 的進行 \_**</span><span class="sxs-lookup"><span data-stu-id="8aa60-133">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

<span data-ttu-id="8aa60-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="8aa60-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8aa60-135">關於動態資料交換</span><span class="sxs-lookup"><span data-stu-id="8aa60-135">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


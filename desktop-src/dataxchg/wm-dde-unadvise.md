---
title: 'WM_DDE_UNADVISE 訊息 (的) '
description: 動態資料交換 (DDE) 用戶端應用程式張貼一個 WM \_ dde \_ UNADVISE 訊息，通知 DDE 伺服器應用程式，該專案的指定專案或特定剪貼簿格式不應再更新。
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- WM_DDE_UNADVISE 訊息資料交換
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466368"
---
# <a name="wm_dde_unadvise-message"></a><span data-ttu-id="31796-104">WM \_ DDE \_ UNADVISE 訊息</span><span class="sxs-lookup"><span data-stu-id="31796-104">WM\_DDE\_UNADVISE message</span></span>

<span data-ttu-id="31796-105">動態資料交換 (DDE) 用戶端應用程式張貼一個 **WM \_ dde \_ UNADVISE** 訊息，通知 DDE 伺服器應用程式，該專案的指定專案或特定剪貼簿格式不應再更新。</span><span class="sxs-lookup"><span data-stu-id="31796-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_UNADVISE** message to inform a DDE server application that the specified item or a particular clipboard format for the item should no longer be updated.</span></span> <span data-ttu-id="31796-106">這會終止指定專案的暖或經常性存取資料連結。</span><span class="sxs-lookup"><span data-stu-id="31796-106">This terminates the warm or hot data link for the specified item.</span></span>

<span data-ttu-id="31796-107">若要張貼此訊息，請使用下列參數呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) 函數。</span><span class="sxs-lookup"><span data-stu-id="31796-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a><span data-ttu-id="31796-108">參數</span><span class="sxs-lookup"><span data-stu-id="31796-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31796-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31796-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31796-110">傳送訊息之用戶端視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="31796-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="31796-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31796-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31796-112">低序位字組指定要撤銷更新要求之專案的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="31796-112">The low-order word specifies the clipboard format of the item for which the update request is being retracted.</span></span> <span data-ttu-id="31796-113">如果這是 **Null**，就會終止專案的所有作用中 [**WM \_ DDE \_ 通知**](wm-dde-advise.md) 交談。</span><span class="sxs-lookup"><span data-stu-id="31796-113">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) conversations for the item are to be terminated.</span></span>

<span data-ttu-id="31796-114">高序位單字包含全域 atom，可識別正在撤銷更新要求的專案。</span><span class="sxs-lookup"><span data-stu-id="31796-114">The high-order word contains a global atom that identifies the item for which the update request is being retracted.</span></span> <span data-ttu-id="31796-115">如果這是 **Null**，就會終止與交談相關聯的所有作用中 [**WM \_ DDE \_ 通知**](wm-dde-advise.md) 連結。</span><span class="sxs-lookup"><span data-stu-id="31796-115">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) links associated with the conversation are to be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31796-116">備註</span><span class="sxs-lookup"><span data-stu-id="31796-116">Remarks</span></span>

<span data-ttu-id="31796-117">用戶端應用程式會呼叫 [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)函式，以配置 *lParam* 的高序位字組。</span><span class="sxs-lookup"><span data-stu-id="31796-117">The client application allocates the high-order word of *lParam* by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="31796-118">伺服器應用程式會張貼 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息，以回應正面或負面。</span><span class="sxs-lookup"><span data-stu-id="31796-118">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="31796-119">張貼 **WM \_ DDE DDE \_ ACK** 時，伺服器可以重複使用 atom，也可以刪除 atom 並建立新的 atom。</span><span class="sxs-lookup"><span data-stu-id="31796-119">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="31796-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="31796-120">Requirements</span></span>



| <span data-ttu-id="31796-121">需求</span><span class="sxs-lookup"><span data-stu-id="31796-121">Requirement</span></span> | <span data-ttu-id="31796-122">值</span><span class="sxs-lookup"><span data-stu-id="31796-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31796-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31796-123">Minimum supported client</span></span><br/> | <span data-ttu-id="31796-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31796-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="31796-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31796-125">Minimum supported server</span></span><br/> | <span data-ttu-id="31796-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31796-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="31796-127">標頭</span><span class="sxs-lookup"><span data-stu-id="31796-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="31796-128"><dt> (包含 Windows. h) </dt></span><span class="sxs-lookup"><span data-stu-id="31796-128"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31796-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31796-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="31796-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="31796-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="31796-131">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="31796-131">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="31796-132">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="31796-132">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="31796-133">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="31796-133">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="31796-134">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="31796-134">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="31796-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="31796-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="31796-136">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="31796-136">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="31796-137">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="31796-137">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="31796-138">**WM \_ DDE \_ 建議**</span><span class="sxs-lookup"><span data-stu-id="31796-138">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

<span data-ttu-id="31796-139">**概念**</span><span class="sxs-lookup"><span data-stu-id="31796-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="31796-140">關於動態資料交換</span><span class="sxs-lookup"><span data-stu-id="31796-140">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


---
title: 'EN_SEARCHWEB (CommCtrl 的通知碼) '
description: 當編輯控制項失去鍵盤焦點時傳送。 編輯控制項的父視窗會透過 WM 通知訊息接收此通知碼 \_ 。
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_SEARCHWEB 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_SEARCHWEB
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 2b995c90e8f4a607d7181adc8a357314acb84dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464421"
---
# <a name="en_searchweb-notification-code"></a><span data-ttu-id="381c4-105">EN \_ SEARCHWEB 通知碼</span><span class="sxs-lookup"><span data-stu-id="381c4-105">EN\_SEARCHWEB notification code</span></span>

<span data-ttu-id="381c4-106">當 [搜尋 web] 功能啟用時，在編輯控制項執行 web 搜尋之後傳送，請參閱 [EM_ENABLESEARCHWEB](em-enablesearchweb.md)。</span><span class="sxs-lookup"><span data-stu-id="381c4-106">Sent after an edit control performed a web search when the "Search the web" feature is enabled, see [EM_ENABLESEARCHWEB](em-enablesearchweb.md).</span></span> <span data-ttu-id="381c4-107">編輯控制項的父視窗會透過 [**WM \_ 通知**](wm-notify.md) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="381c4-107">The parent window of the edit control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SEARCHWEB

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="381c4-108">參數</span><span class="sxs-lookup"><span data-stu-id="381c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="381c4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="381c4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="381c4-110">編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="381c4-110">Handle to the edit control.</span></span>

</dd> <dt>

<span data-ttu-id="381c4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="381c4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="381c4-112">[**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="381c4-112">A pointer to a [**NMSEARCHWEB**](/windows/desktop/api/Commctrl/ns-commctrl-nmsearchweb) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="381c4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="381c4-113">Requirements</span></span>



| <span data-ttu-id="381c4-114">需求</span><span class="sxs-lookup"><span data-stu-id="381c4-114">Requirement</span></span> | <span data-ttu-id="381c4-115">值</span><span class="sxs-lookup"><span data-stu-id="381c4-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="381c4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="381c4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="381c4-117">Windows 10， \[ 僅限 1809 desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="381c4-117">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="381c4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="381c4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="381c4-119">僅限 Windows Server 2019 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="381c4-119">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="381c4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="381c4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="381c4-121"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="381c4-121"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="381c4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="381c4-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="381c4-123">**參考**</span><span class="sxs-lookup"><span data-stu-id="381c4-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="381c4-124">**EM \_ ENABLESEARCHWEB**</span><span class="sxs-lookup"><span data-stu-id="381c4-124">**EM\_ENABLESEARCHWEB**</span></span>](em-enablesearchweb.md)
</dt> <dt>

<span data-ttu-id="381c4-125">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="381c4-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="381c4-126">**WM \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="381c4-126">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 






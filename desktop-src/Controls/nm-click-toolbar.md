---
title: 'NM_CLICK (工具列) 通知碼 (Commctrl) '
description: 當使用者按一下具有滑鼠左鍵的專案時，由工具列控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: fa43c9bc-db2a-4460-b193-2b4694d06d83
keywords:
- NM_CLICK (工具列) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca31e3553327c94d371617d016a85395519c211d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844463"
---
# <a name="nm_click-toolbar-notification-code"></a><span data-ttu-id="20374-105">NM \_ 按一下 (工具列) 通知碼</span><span class="sxs-lookup"><span data-stu-id="20374-105">NM\_CLICK (toolbar) notification code</span></span>

<span data-ttu-id="20374-106">當使用者按一下具有滑鼠左鍵的專案時，由工具列控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="20374-106">Sent by a toolbar control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="20374-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="20374-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="20374-108">參數</span><span class="sxs-lookup"><span data-stu-id="20374-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20374-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20374-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20374-110">[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="20374-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="20374-111">**DwItemSpec** 成員包含已按下之區段的索引。</span><span class="sxs-lookup"><span data-stu-id="20374-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20374-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="20374-112">Return value</span></span>

<span data-ttu-id="20374-113">傳回 **TRUE** 表示滑鼠按一下已處理，並隱藏系統的預設處理。</span><span class="sxs-lookup"><span data-stu-id="20374-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="20374-114">傳回 **FALSE** 以允許按一下的預設處理。</span><span class="sxs-lookup"><span data-stu-id="20374-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="remarks"></a><span data-ttu-id="20374-115">備註</span><span class="sxs-lookup"><span data-stu-id="20374-115">Remarks</span></span>

<span data-ttu-id="20374-116">按一下具有滑鼠左鍵的專案，會導致工具列將 [BN \_ 按一下](bn-clicked.md)通知程式碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command)訊息傳送至父視窗。</span><span class="sxs-lookup"><span data-stu-id="20374-116">Clicking an item with the left mouse button causes the toolbar to send a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with the [BN\_CLICKED](bn-clicked.md) notification code to the parent window.</span></span> <span data-ttu-id="20374-117">NM \_ CLICK 通知會在 **WM \_ 命令** 訊息之後傳送。</span><span class="sxs-lookup"><span data-stu-id="20374-117">The NM\_CLICK notification is sent after the **WM\_COMMAND** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="20374-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="20374-118">Requirements</span></span>



| <span data-ttu-id="20374-119">需求</span><span class="sxs-lookup"><span data-stu-id="20374-119">Requirement</span></span> | <span data-ttu-id="20374-120">值</span><span class="sxs-lookup"><span data-stu-id="20374-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20374-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20374-121">Minimum supported client</span></span><br/> | <span data-ttu-id="20374-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20374-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20374-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20374-123">Minimum supported server</span></span><br/> | <span data-ttu-id="20374-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20374-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20374-125">標頭</span><span class="sxs-lookup"><span data-stu-id="20374-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="20374-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="20374-126"><dt>Commctrl.h</dt></span></span> </dl> |



 


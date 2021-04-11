---
title: 'NM_DBLCLK (狀態列) 通知碼 (Commctrl) '
description: 通知狀態列控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 4c02c76d-2bdb-48ef-aa8e-635d0e200eb1
keywords:
- NM_DBLCLK (的狀態列) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28866effbc4143dc9d0d5a3800f88711c99f88db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933915"
---
# <a name="nm_dblclk-status-bar-notification-code"></a><span data-ttu-id="1ff6c-105">NM \_ DBLCLK (狀態列) 通知碼</span><span class="sxs-lookup"><span data-stu-id="1ff6c-105">NM\_DBLCLK (status bar) notification code</span></span>

<span data-ttu-id="1ff6c-106">通知狀態列控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="1ff6c-106">Notifies the parent window of a status bar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="1ff6c-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="1ff6c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    LPNMMOUSE lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1ff6c-108">參數</span><span class="sxs-lookup"><span data-stu-id="1ff6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ff6c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ff6c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ff6c-110">[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1ff6c-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="1ff6c-111">**DwItemSpec** 成員包含已按下之區段的索引。</span><span class="sxs-lookup"><span data-stu-id="1ff6c-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ff6c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ff6c-112">Return value</span></span>

<span data-ttu-id="1ff6c-113">傳回 **TRUE** 表示滑鼠按一下已處理，並隱藏系統的預設處理。</span><span class="sxs-lookup"><span data-stu-id="1ff6c-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="1ff6c-114">傳回 **FALSE** 以允許按一下的預設處理。</span><span class="sxs-lookup"><span data-stu-id="1ff6c-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff6c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ff6c-115">Requirements</span></span>



| <span data-ttu-id="1ff6c-116">需求</span><span class="sxs-lookup"><span data-stu-id="1ff6c-116">Requirement</span></span> | <span data-ttu-id="1ff6c-117">值</span><span class="sxs-lookup"><span data-stu-id="1ff6c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff6c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ff6c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1ff6c-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ff6c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ff6c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ff6c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1ff6c-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ff6c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ff6c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1ff6c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ff6c-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ff6c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






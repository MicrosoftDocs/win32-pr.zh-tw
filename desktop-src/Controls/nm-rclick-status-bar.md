---
title: 'NM_RCLICK (狀態列) 通知碼 (Commctrl) '
description: 通知狀態列控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- NM_RCLICK (的狀態列) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326ac6600716419648ecfacf25cd8423551fd03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317524"
---
# <a name="nm_rclick-status-bar-notification-code"></a><span data-ttu-id="9f143-105">NM \_ RCLICK (狀態列) 通知碼</span><span class="sxs-lookup"><span data-stu-id="9f143-105">NM\_RCLICK (status bar) notification code</span></span>

<span data-ttu-id="9f143-106">通知狀態列控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。</span><span class="sxs-lookup"><span data-stu-id="9f143-106">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="9f143-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="9f143-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9f143-108">參數</span><span class="sxs-lookup"><span data-stu-id="9f143-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f143-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f143-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f143-110">[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9f143-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f143-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f143-111">Return value</span></span>

<span data-ttu-id="9f143-112">傳回 **TRUE** 表示滑鼠按一下已處理，並隱藏系統的預設處理。</span><span class="sxs-lookup"><span data-stu-id="9f143-112">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="9f143-113">傳回 **FALSE** 以允許按一下的預設處理。</span><span class="sxs-lookup"><span data-stu-id="9f143-113">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f143-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f143-114">Requirements</span></span>



| <span data-ttu-id="9f143-115">需求</span><span class="sxs-lookup"><span data-stu-id="9f143-115">Requirement</span></span> | <span data-ttu-id="9f143-116">值</span><span class="sxs-lookup"><span data-stu-id="9f143-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f143-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f143-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9f143-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f143-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f143-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f143-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9f143-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f143-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f143-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9f143-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f143-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f143-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






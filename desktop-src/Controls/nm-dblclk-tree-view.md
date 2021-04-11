---
title: 'NM_DBLCLK (樹狀檢視) 通知碼 (Commctrl) '
description: 通知樹狀檢視控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 2ed3b3ad-a252-496a-bfcf-0cec5678f192
keywords:
- NM_DBLCLK (樹狀檢視) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 78f89671e1a26962eacf255d4c98ea0baa1578de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024584"
---
# <a name="nm_dblclk-tree-view-notification-code"></a><span data-ttu-id="92635-105">NM \_ DBLCLK (樹狀檢視) 通知碼</span><span class="sxs-lookup"><span data-stu-id="92635-105">NM\_DBLCLK (tree view) notification code</span></span>

<span data-ttu-id="92635-106">通知樹狀檢視控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="92635-106">Notifies the parent window of a tree-view control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="92635-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="92635-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="92635-108">參數</span><span class="sxs-lookup"><span data-stu-id="92635-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92635-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92635-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92635-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="92635-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92635-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="92635-111">Return value</span></span>

<span data-ttu-id="92635-112">傳回非零以防止預設處理，或零以允許預設處理。</span><span class="sxs-lookup"><span data-stu-id="92635-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="92635-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="92635-113">Requirements</span></span>



| <span data-ttu-id="92635-114">需求</span><span class="sxs-lookup"><span data-stu-id="92635-114">Requirement</span></span> | <span data-ttu-id="92635-115">值</span><span class="sxs-lookup"><span data-stu-id="92635-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92635-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92635-116">Minimum supported client</span></span><br/> | <span data-ttu-id="92635-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92635-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92635-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92635-118">Minimum supported server</span></span><br/> | <span data-ttu-id="92635-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92635-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92635-120">標頭</span><span class="sxs-lookup"><span data-stu-id="92635-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="92635-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="92635-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






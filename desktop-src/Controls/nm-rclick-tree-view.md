---
title: 'NM_RCLICK (樹狀檢視) 通知碼 (Commctrl) '
description: 通知樹狀檢視控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 5816d8b8-7f3d-477d-9116-1b3670d99240
keywords:
- NM_RCLICK (樹狀檢視) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 58d72ee220bf33189e8954a2e1ef454b22886553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106619"
---
# <a name="nm_rclick-tree-view-notification-code"></a><span data-ttu-id="2ecf5-105">NM \_ RCLICK (樹狀檢視) 通知碼</span><span class="sxs-lookup"><span data-stu-id="2ecf5-105">NM\_RCLICK (tree view) notification code</span></span>

<span data-ttu-id="2ecf5-106">通知樹狀檢視控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。</span><span class="sxs-lookup"><span data-stu-id="2ecf5-106">Notifies the parent window of a tree-view control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="2ecf5-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="2ecf5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2ecf5-108">參數</span><span class="sxs-lookup"><span data-stu-id="2ecf5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ecf5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ecf5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ecf5-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2ecf5-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ecf5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ecf5-111">Return value</span></span>

<span data-ttu-id="2ecf5-112">傳回非零以防止預設處理，或零以允許預設處理。</span><span class="sxs-lookup"><span data-stu-id="2ecf5-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ecf5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ecf5-113">Requirements</span></span>



| <span data-ttu-id="2ecf5-114">需求</span><span class="sxs-lookup"><span data-stu-id="2ecf5-114">Requirement</span></span> | <span data-ttu-id="2ecf5-115">值</span><span class="sxs-lookup"><span data-stu-id="2ecf5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ecf5-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ecf5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2ecf5-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ecf5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ecf5-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ecf5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2ecf5-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ecf5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ecf5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2ecf5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ecf5-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ecf5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






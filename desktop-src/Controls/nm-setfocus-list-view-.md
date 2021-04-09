---
title: 'NM_SETFOCUS (清單視圖) 通知碼 (Commctrl) '
description: 通知清單視圖控制項的父視窗，控制項已收到輸入焦點。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 43d3b09a-f095-4f30-87a8-2f2e782d6720
keywords:
- NM_SETFOCUS (清單視圖) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99cc84e76c0203a6e2930d3d9f50bc61a1e31395
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024925"
---
# <a name="nm_setfocus-list-view-notification-code"></a><span data-ttu-id="7dc19-105">NM \_ SETFOCUS (清單視圖) 通知碼</span><span class="sxs-lookup"><span data-stu-id="7dc19-105">NM\_SETFOCUS (list view) notification code</span></span>

<span data-ttu-id="7dc19-106">通知清單視圖控制項的父視窗，控制項已收到輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="7dc19-106">Notifies a list-view control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="7dc19-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="7dc19-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7dc19-108">參數</span><span class="sxs-lookup"><span data-stu-id="7dc19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dc19-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7dc19-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dc19-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7dc19-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dc19-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7dc19-111">Return value</span></span>

<span data-ttu-id="7dc19-112">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="7dc19-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc19-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dc19-113">Requirements</span></span>



| <span data-ttu-id="7dc19-114">需求</span><span class="sxs-lookup"><span data-stu-id="7dc19-114">Requirement</span></span> | <span data-ttu-id="7dc19-115">值</span><span class="sxs-lookup"><span data-stu-id="7dc19-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc19-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7dc19-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc19-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7dc19-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7dc19-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7dc19-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc19-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7dc19-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7dc19-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7dc19-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc19-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc19-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






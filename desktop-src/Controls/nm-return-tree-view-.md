---
title: 'NM_RETURN (樹狀檢視) 通知碼 (Commctrl) '
description: 通知樹狀檢視控制項的父視窗，控制項具有輸入焦點，而且使用者已按下該按鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e4a048ec-4643-458a-bf75-f5b08163d6c6
keywords:
- NM_RETURN (樹狀檢視) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a0abf3152a9236103301f1c74acfcac69d43f07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934799"
---
# <a name="nm_return-tree-view-notification-code"></a><span data-ttu-id="b7393-105">NM 傳回 \_ (樹狀檢視) 通知碼</span><span class="sxs-lookup"><span data-stu-id="b7393-105">NM\_RETURN (tree view) notification code</span></span>

<span data-ttu-id="b7393-106">通知樹狀檢視控制項的父視窗，控制項具有輸入焦點，而且使用者已按下該按鍵。</span><span class="sxs-lookup"><span data-stu-id="b7393-106">Notifies a tree-view control's parent window that the control has the input focus and that the user has pressed the key.</span></span> <span data-ttu-id="b7393-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="b7393-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b7393-108">參數</span><span class="sxs-lookup"><span data-stu-id="b7393-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7393-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7393-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7393-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b7393-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7393-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7393-111">Return value</span></span>

<span data-ttu-id="b7393-112">傳回非零以防止預設處理，或零以允許預設處理。</span><span class="sxs-lookup"><span data-stu-id="b7393-112">Return nonzero to prevent the default processing, or zero to allow the default processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7393-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7393-113">Requirements</span></span>



| <span data-ttu-id="b7393-114">需求</span><span class="sxs-lookup"><span data-stu-id="b7393-114">Requirement</span></span> | <span data-ttu-id="b7393-115">值</span><span class="sxs-lookup"><span data-stu-id="b7393-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7393-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7393-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b7393-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7393-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7393-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7393-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b7393-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7393-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7393-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b7393-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7393-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7393-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






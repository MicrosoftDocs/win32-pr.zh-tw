---
title: 'NM_KILLFOCUS (樹狀檢視) 通知碼 (Commctrl) '
description: 通知樹狀檢視控制項的父視窗，表示控制項已遺失輸入焦點。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: f6646a39-6480-4417-9c1c-ffd2417ca7dd
keywords:
- NM_KILLFOCUS (樹狀檢視) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7123f47469a02fcec92805a27d81e173c5e1d10a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933911"
---
# <a name="nm_killfocus-tree-view-notification-code"></a><span data-ttu-id="16c9e-105">NM \_ KILLFOCUS (樹狀檢視) 通知碼</span><span class="sxs-lookup"><span data-stu-id="16c9e-105">NM\_KILLFOCUS (tree view) notification code</span></span>

<span data-ttu-id="16c9e-106">通知樹狀檢視控制項的父視窗，表示控制項已遺失輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="16c9e-106">Notifies a tree-view control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="16c9e-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="16c9e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="16c9e-108">參數</span><span class="sxs-lookup"><span data-stu-id="16c9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16c9e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16c9e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16c9e-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="16c9e-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16c9e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="16c9e-111">Return value</span></span>

<span data-ttu-id="16c9e-112">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="16c9e-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="16c9e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="16c9e-113">Requirements</span></span>



| <span data-ttu-id="16c9e-114">需求</span><span class="sxs-lookup"><span data-stu-id="16c9e-114">Requirement</span></span> | <span data-ttu-id="16c9e-115">值</span><span class="sxs-lookup"><span data-stu-id="16c9e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16c9e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16c9e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="16c9e-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16c9e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16c9e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16c9e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="16c9e-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16c9e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16c9e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="16c9e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="16c9e-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="16c9e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






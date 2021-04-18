---
title: 'TBN_QUERYDELETE (Commctrl 的通知碼) '
description: 當使用者正在自訂工具列時，通知工具列的父視窗是否可從工具列中刪除按鈕。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508296"
---
# <a name="tbn_querydelete-notification-code"></a><span data-ttu-id="ae2b4-105">TBN \_ QUERYDELETE 通知碼</span><span class="sxs-lookup"><span data-stu-id="ae2b4-105">TBN\_QUERYDELETE notification code</span></span>

<span data-ttu-id="ae2b4-106">當使用者正在自訂工具列時，通知工具列的父視窗是否可從工具列中刪除按鈕。</span><span class="sxs-lookup"><span data-stu-id="ae2b4-106">Notifies the toolbar's parent window whether a button may be deleted from a toolbar while the user is customizing the toolbar.</span></span> <span data-ttu-id="ae2b4-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="ae2b4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ae2b4-108">參數</span><span class="sxs-lookup"><span data-stu-id="ae2b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae2b4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae2b4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae2b4-110">[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ae2b4-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="ae2b4-111">**iItem** 成員包含所要刪除的按鈕之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="ae2b4-111">The **iItem** member contains the zero-based index of the button to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae2b4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae2b4-112">Return value</span></span>

<span data-ttu-id="ae2b4-113">傳回 **TRUE** 表示允許刪除按鈕，或傳回 **FALSE** 以防止刪除按鈕。</span><span class="sxs-lookup"><span data-stu-id="ae2b4-113">Returns **TRUE** to allow the button to be deleted, or **FALSE** to prevent the button from being deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2b4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae2b4-114">Requirements</span></span>



| <span data-ttu-id="ae2b4-115">需求</span><span class="sxs-lookup"><span data-stu-id="ae2b4-115">Requirement</span></span> | <span data-ttu-id="ae2b4-116">值</span><span class="sxs-lookup"><span data-stu-id="ae2b4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2b4-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae2b4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2b4-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae2b4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae2b4-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae2b4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2b4-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae2b4-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae2b4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ae2b4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae2b4-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2b4-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






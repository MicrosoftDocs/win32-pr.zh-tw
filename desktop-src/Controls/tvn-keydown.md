---
title: 'TVN_KEYDOWN (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，讓使用者按下按鍵，並讓樹狀檢視控制項擁有輸入焦點。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464245"
---
# <a name="tvn_keydown-notification-code"></a><span data-ttu-id="cd8ff-105">IZDEBSKI \_ KEYDOWN 通知碼</span><span class="sxs-lookup"><span data-stu-id="cd8ff-105">TVN\_KEYDOWN notification code</span></span>

<span data-ttu-id="cd8ff-106">通知樹狀檢視控制項的父視窗，讓使用者按下按鍵，並讓樹狀檢視控制項擁有輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="cd8ff-106">Notifies a tree-view control's parent window that the user pressed a key and the tree-view control has the input focus.</span></span> <span data-ttu-id="cd8ff-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="cd8ff-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a><span data-ttu-id="cd8ff-108">參數</span><span class="sxs-lookup"><span data-stu-id="cd8ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd8ff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd8ff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd8ff-110">[**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cd8ff-110">Pointer to an [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) structure.</span></span> <span data-ttu-id="cd8ff-111">**WVKey** 成員會指定虛擬金鑰碼。</span><span class="sxs-lookup"><span data-stu-id="cd8ff-111">The **wVKey** member specifies the virtual key code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd8ff-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd8ff-112">Return value</span></span>

<span data-ttu-id="cd8ff-113">如果 *lParam* 的 **wVKey** 成員是字元按鍵碼，則會使用該字元作為增量搜尋的一部分。</span><span class="sxs-lookup"><span data-stu-id="cd8ff-113">If the **wVKey** member of *lParam* is a character key code, the character will be used as part of an incremental search.</span></span> <span data-ttu-id="cd8ff-114">傳回非零值以排除增量搜尋中的字元，或零以包含搜尋中的字元。</span><span class="sxs-lookup"><span data-stu-id="cd8ff-114">Return nonzero to exclude the character from the incremental search, or zero to include the character in the search.</span></span> <span data-ttu-id="cd8ff-115">若為所有其他索引鍵，則會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="cd8ff-115">For all other keys, the return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd8ff-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd8ff-116">Requirements</span></span>



| <span data-ttu-id="cd8ff-117">需求</span><span class="sxs-lookup"><span data-stu-id="cd8ff-117">Requirement</span></span> | <span data-ttu-id="cd8ff-118">值</span><span class="sxs-lookup"><span data-stu-id="cd8ff-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd8ff-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd8ff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cd8ff-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd8ff-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cd8ff-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd8ff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cd8ff-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd8ff-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd8ff-123">標頭</span><span class="sxs-lookup"><span data-stu-id="cd8ff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd8ff-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd8ff-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






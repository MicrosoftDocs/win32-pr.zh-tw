---
title: 'TBN_DROPDOWN (Commctrl 的通知碼) '
description: 當使用者按一下下拉式按鈕時，由工具列控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- TBN_DROPDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934191"
---
# <a name="tbn_dropdown-notification-code"></a><span data-ttu-id="7bc60-105">TBN \_ 下拉式通知碼</span><span class="sxs-lookup"><span data-stu-id="7bc60-105">TBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="7bc60-106">當使用者按一下下拉式按鈕時，由工具列控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="7bc60-106">Sent by a toolbar control when the user clicks a dropdown button.</span></span> <span data-ttu-id="7bc60-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="7bc60-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7bc60-108">參數</span><span class="sxs-lookup"><span data-stu-id="7bc60-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bc60-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7bc60-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7bc60-110">[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7bc60-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="7bc60-111">針對此通知碼，只有此結構的 **hdr** 和 **iItem** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="7bc60-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bc60-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="7bc60-112">Return value</span></span>

<span data-ttu-id="7bc60-113">傳回下列其中一值：</span><span class="sxs-lookup"><span data-stu-id="7bc60-113">Returns one of the following values:</span></span>



| <span data-ttu-id="7bc60-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7bc60-114">Return code</span></span>                                                                                          | <span data-ttu-id="7bc60-115">Description</span><span class="sxs-lookup"><span data-stu-id="7bc60-115">Description</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7bc60-116"><dt>**TBDDRET \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="7bc60-116"><dt>**TBDDRET\_DEFAULT**</dt></span></span> </dl>      | <span data-ttu-id="7bc60-117">已處理下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="7bc60-117">The drop-down was handled.</span></span><br/>                                             |
| <dl> <span data-ttu-id="7bc60-118"><dt>**TBDDRET \_ NODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="7bc60-118"><dt>**TBDDRET\_NODEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="7bc60-119">未處理下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="7bc60-119">The drop-down was not handled.</span></span><br/>                                         |
| <dl> <span data-ttu-id="7bc60-120"><dt>**TBDDRET \_ TREATPRESSED**</dt></span><span class="sxs-lookup"><span data-stu-id="7bc60-120"><dt>**TBDDRET\_TREATPRESSED**</dt></span></span> </dl> | <span data-ttu-id="7bc60-121">已處理下拉式清單，但是將按鈕視為一般按鈕。</span><span class="sxs-lookup"><span data-stu-id="7bc60-121">The drop-down was handled, but treat the button like a regular button.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7bc60-122">備註</span><span class="sxs-lookup"><span data-stu-id="7bc60-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7bc60-123">下拉式按鈕可以是純 ([**BTNS \_ 下拉式**](toolbar-control-and-button-styles.md) 樣式) 、在按鈕影像旁邊顯示箭號 ([**BTNS \_ WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) style) ，或是顯示與影像 ([**TBSTYLE 範例 \_ \_ DRAWDDARROWS**](toolbar-extended-styles.md) 樣式) 分開的箭號。</span><span class="sxs-lookup"><span data-stu-id="7bc60-123">Dropdown buttons can be plain ([**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style), display an arrow next to the button image ([**BTNS\_WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) style), or display an arrow that is separated from the image ([**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style).</span></span> <span data-ttu-id="7bc60-124">如果使用分隔箭號， \_ 只有當使用者按一下按鈕的箭號部分時，才會傳送 TBN 下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="7bc60-124">If a separated arrow is used, TBN\_DROPDOWN is sent only if the user clicks the arrow portion of the button.</span></span> <span data-ttu-id="7bc60-125">如果使用者按一下按鈕的主要部分，則會傳送具有按鈕識別碼的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息，就像使用標準按鈕一樣。</span><span class="sxs-lookup"><span data-stu-id="7bc60-125">If the user clicks the main part of the button, a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with button's ID is sent, just as with a standard button.</span></span> <span data-ttu-id="7bc60-126">針對其他兩個下拉式按鈕樣式， \_ 當使用者按一下按鈕的任一個部分時，就會傳送 TBN 下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="7bc60-126">For the other two styles of dropdown button, TBN\_DROPDOWN is sent when the user clicks any part of the button.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7bc60-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bc60-127">Requirements</span></span>



| <span data-ttu-id="7bc60-128">需求</span><span class="sxs-lookup"><span data-stu-id="7bc60-128">Requirement</span></span> | <span data-ttu-id="7bc60-129">值</span><span class="sxs-lookup"><span data-stu-id="7bc60-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7bc60-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7bc60-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7bc60-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7bc60-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7bc60-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7bc60-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7bc60-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7bc60-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7bc60-134">標頭</span><span class="sxs-lookup"><span data-stu-id="7bc60-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bc60-135"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7bc60-135"><dt>Commctrl.h</dt></span></span> </dl> |



 


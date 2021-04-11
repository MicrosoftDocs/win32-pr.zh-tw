---
title: 'TBN_QUERYINSERT (Commctrl 的通知碼) '
description: 當使用者正在自訂工具列時，通知工具列的父視窗是否可將按鈕插入指定按鈕的左邊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935009"
---
# <a name="tbn_queryinsert-notification-code"></a><span data-ttu-id="6a854-105">TBN \_ QUERYINSERT 通知碼</span><span class="sxs-lookup"><span data-stu-id="6a854-105">TBN\_QUERYINSERT notification code</span></span>

<span data-ttu-id="6a854-106">當使用者正在自訂工具列時，通知工具列的父視窗是否可將按鈕插入指定按鈕的左邊。</span><span class="sxs-lookup"><span data-stu-id="6a854-106">Notifies the toolbar's parent window whether a button may be inserted to the left of the specified button while the user is customizing a toolbar.</span></span> <span data-ttu-id="6a854-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="6a854-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6a854-108">參數</span><span class="sxs-lookup"><span data-stu-id="6a854-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a854-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a854-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a854-110">[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6a854-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="6a854-111">**iItem** 成員包含所要插入的按鈕之以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="6a854-111">The **iItem** member contains the zero-based index of the button to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a854-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a854-112">Return value</span></span>

<span data-ttu-id="6a854-113">傳回 **TRUE** 表示允許在指定按鈕之前插入按鈕，或傳回 **FALSE** 以防止插入按鈕。</span><span class="sxs-lookup"><span data-stu-id="6a854-113">Return **TRUE** to allow a button to be inserted in front of the given button, or **FALSE** to prevent the button from being inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a854-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a854-114">Requirements</span></span>



| <span data-ttu-id="6a854-115">需求</span><span class="sxs-lookup"><span data-stu-id="6a854-115">Requirement</span></span> | <span data-ttu-id="6a854-116">值</span><span class="sxs-lookup"><span data-stu-id="6a854-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a854-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a854-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6a854-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a854-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a854-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a854-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6a854-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a854-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a854-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6a854-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a854-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a854-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: 'LVN_MARQUEEBEGIN (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，表示已開始) 選取範圍 (的周框方塊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966158"
---
# <a name="lvn_marqueebegin-notification-code"></a><span data-ttu-id="6efd6-105">LVN \_ MARQUEEBEGIN 通知碼</span><span class="sxs-lookup"><span data-stu-id="6efd6-105">LVN\_MARQUEEBEGIN notification code</span></span>

<span data-ttu-id="6efd6-106">通知清單視圖控制項的父視窗，表示已開始) 選取範圍 (的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="6efd6-106">Notifies a list-view control's parent window that a bounding box (marquee) selection has begun.</span></span> <span data-ttu-id="6efd6-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="6efd6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6efd6-108">參數</span><span class="sxs-lookup"><span data-stu-id="6efd6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6efd6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6efd6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6efd6-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6efd6-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6efd6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6efd6-111">Return value</span></span>

<span data-ttu-id="6efd6-112">若要接受通知碼，請傳回零。</span><span class="sxs-lookup"><span data-stu-id="6efd6-112">To accept the notification code, return zero.</span></span> <span data-ttu-id="6efd6-113">若要結束周框方塊選取範圍，則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="6efd6-113">To quit the bounding box selection, return nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6efd6-114">備註</span><span class="sxs-lookup"><span data-stu-id="6efd6-114">Remarks</span></span>

<span data-ttu-id="6efd6-115">周 *框方塊選取範圍* 是按一下清單視圖視窗的工作區，並拖曳以同時選取多個專案的流程。</span><span class="sxs-lookup"><span data-stu-id="6efd6-115">A *bounding box selection* is the process of clicking the list-view window's client area and dragging to select multiple items simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="6efd6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6efd6-116">Requirements</span></span>



| <span data-ttu-id="6efd6-117">需求</span><span class="sxs-lookup"><span data-stu-id="6efd6-117">Requirement</span></span> | <span data-ttu-id="6efd6-118">值</span><span class="sxs-lookup"><span data-stu-id="6efd6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6efd6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6efd6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6efd6-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6efd6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6efd6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6efd6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6efd6-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6efd6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6efd6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6efd6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6efd6-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6efd6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






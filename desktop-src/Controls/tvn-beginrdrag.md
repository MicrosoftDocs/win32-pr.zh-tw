---
title: 'TVN_BEGINRDRAG (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，有關啟動與滑鼠右鍵有關的拖放作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- TVN_BEGINRDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec15b5f48d4ed5612778622bb3655ae153c1b9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935000"
---
# <a name="tvn_beginrdrag-notification-code"></a><span data-ttu-id="14adc-105">IZDEBSKI \_ BEGINRDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="14adc-105">TVN\_BEGINRDRAG notification code</span></span>

<span data-ttu-id="14adc-106">通知樹狀檢視控制項的父視窗，有關啟動與滑鼠右鍵有關的拖放作業。</span><span class="sxs-lookup"><span data-stu-id="14adc-106">Notifies a tree-view control's parent window about the initiation of a drag-and-drop operation involving the right mouse button.</span></span> <span data-ttu-id="14adc-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="14adc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="14adc-108">參數</span><span class="sxs-lookup"><span data-stu-id="14adc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14adc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14adc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14adc-110">[**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="14adc-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="14adc-111">**ItemNew** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其中包含有關要拖曳之專案的 **hItem**、 **state** 和 **lParam** 成員中的有效資訊。</span><span class="sxs-lookup"><span data-stu-id="14adc-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information in the **hItem**, **state**, and **lParam** members about the item to be dragged.</span></span> <span data-ttu-id="14adc-112">**PtDrag** 成員會指定滑鼠目前的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="14adc-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14adc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="14adc-113">Return value</span></span>

<span data-ttu-id="14adc-114">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="14adc-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="14adc-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="14adc-115">Requirements</span></span>



| <span data-ttu-id="14adc-116">需求</span><span class="sxs-lookup"><span data-stu-id="14adc-116">Requirement</span></span> | <span data-ttu-id="14adc-117">值</span><span class="sxs-lookup"><span data-stu-id="14adc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14adc-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14adc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="14adc-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14adc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14adc-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14adc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="14adc-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14adc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14adc-122">標頭</span><span class="sxs-lookup"><span data-stu-id="14adc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="14adc-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="14adc-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="14adc-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="14adc-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="14adc-125">**Izdebski \_BEGINRDRAGW** (Unicode) 和 **izdebski \_ BEGINRDRAGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="14adc-125">**TVN\_BEGINRDRAGW** (Unicode) and **TVN\_BEGINRDRAGA** (ANSI)</span></span><br/>             |



 

 






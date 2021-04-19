---
title: 'NM_RCLICK (工具列) 通知碼 (Commctrl) '
description: 當使用者按一下具有滑鼠右鍵的工具列時，由工具列控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e9d2d871-e922-444d-a76c-e73f249ed410
keywords:
- NM_RCLICK (工具列) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: 6464c30a031aa55aef94bccd3ab852720fb14403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967575"
---
# <a name="nm_rclick-toolbar-notification-code"></a><span data-ttu-id="ccc13-105">NM \_ RCLICK (工具列) 通知碼</span><span class="sxs-lookup"><span data-stu-id="ccc13-105">NM\_RCLICK (toolbar) notification code</span></span>

<span data-ttu-id="ccc13-106">當使用者按一下具有滑鼠右鍵的工具列時，由工具列控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="ccc13-106">Sent by a toolbar control when the user clicks the toolbar with the right mouse button.</span></span> <span data-ttu-id="ccc13-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="ccc13-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ccc13-108">參數</span><span class="sxs-lookup"><span data-stu-id="ccc13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc13-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ccc13-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ccc13-110">[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含此通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ccc13-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="ccc13-111">如果滑鼠已按下工具列專案， **dwItemSpec** 成員就會包含專案識別碼，而 **dwItemData** 成員會包含專案資料。</span><span class="sxs-lookup"><span data-stu-id="ccc13-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="ccc13-112">如果按一下工具列上的分隔符號或空白字元， **dwItemSpec** 成員會包含-1。</span><span class="sxs-lookup"><span data-stu-id="ccc13-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccc13-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ccc13-113">Return value</span></span>

<span data-ttu-id="ccc13-114">傳回 **FALSE** 以允許工具列控制項執行事件的預設處理，或傳回 **TRUE** 以防止控制項處理事件。</span><span class="sxs-lookup"><span data-stu-id="ccc13-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc13-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccc13-115">Requirements</span></span>



| <span data-ttu-id="ccc13-116">需求</span><span class="sxs-lookup"><span data-stu-id="ccc13-116">Requirement</span></span> | <span data-ttu-id="ccc13-117">值</span><span class="sxs-lookup"><span data-stu-id="ccc13-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc13-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ccc13-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc13-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccc13-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ccc13-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ccc13-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc13-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ccc13-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ccc13-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ccc13-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc13-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc13-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






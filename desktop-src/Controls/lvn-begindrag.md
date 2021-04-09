---
title: 'LVN_BEGINDRAG (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，表示正在起始包含滑鼠左鍵的拖放作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 2b9bbff8-f5f7-47ac-b662-a327ff49caf7
keywords:
- LVN_BEGINDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69166cd38242db915f70772b5dfbd3bab6ba56df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024660"
---
# <a name="lvn_begindrag-notification-code"></a><span data-ttu-id="37613-105">LVN \_ BEGINDRAG 通知碼</span><span class="sxs-lookup"><span data-stu-id="37613-105">LVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="37613-106">通知清單視圖控制項的父視窗，表示正在起始包含滑鼠左鍵的拖放作業。</span><span class="sxs-lookup"><span data-stu-id="37613-106">Notifies a list-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="37613-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="37613-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="37613-108">參數</span><span class="sxs-lookup"><span data-stu-id="37613-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37613-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37613-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37613-110">[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="37613-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="37613-111">**IItem** 成員會識別要拖曳的專案，而其他成員則為零。</span><span class="sxs-lookup"><span data-stu-id="37613-111">The **iItem** member identifies the item being dragged, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37613-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="37613-112">Return value</span></span>

<span data-ttu-id="37613-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="37613-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="37613-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="37613-114">Requirements</span></span>



| <span data-ttu-id="37613-115">需求</span><span class="sxs-lookup"><span data-stu-id="37613-115">Requirement</span></span> | <span data-ttu-id="37613-116">值</span><span class="sxs-lookup"><span data-stu-id="37613-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37613-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37613-117">Minimum supported client</span></span><br/> | <span data-ttu-id="37613-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37613-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37613-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37613-119">Minimum supported server</span></span><br/> | <span data-ttu-id="37613-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37613-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37613-121">標頭</span><span class="sxs-lookup"><span data-stu-id="37613-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="37613-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="37613-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






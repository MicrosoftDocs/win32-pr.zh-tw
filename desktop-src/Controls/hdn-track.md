---
title: 'HDN_TRACK (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，表示使用者正在拖曳標題控制項中的分隔線。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- HDN_TRACK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91b55ac23e2de17788b17c1f121530308de9e7a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843891"
---
# <a name="hdn_track-notification-code"></a><span data-ttu-id="62855-105">HDN \_ TRACK 通知碼</span><span class="sxs-lookup"><span data-stu-id="62855-105">HDN\_TRACK notification code</span></span>

<span data-ttu-id="62855-106">通知標題控制項的父視窗，表示使用者正在拖曳標題控制項中的分隔線。</span><span class="sxs-lookup"><span data-stu-id="62855-106">Notifies a header control's parent window that the user is dragging a divider in the header control.</span></span> <span data-ttu-id="62855-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="62855-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="62855-108">參數</span><span class="sxs-lookup"><span data-stu-id="62855-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62855-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62855-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62855-110">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項的相關資訊，以及正在拖曳其分割的專案。</span><span class="sxs-lookup"><span data-stu-id="62855-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62855-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="62855-111">Return value</span></span>

<span data-ttu-id="62855-112">傳回 **FALSE** 以繼續追蹤分隔線，或 **TRUE** 表示結束追蹤。</span><span class="sxs-lookup"><span data-stu-id="62855-112">Returns **FALSE** to continue tracking the divider, or **TRUE** to end tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="62855-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="62855-113">Requirements</span></span>



| <span data-ttu-id="62855-114">需求</span><span class="sxs-lookup"><span data-stu-id="62855-114">Requirement</span></span> | <span data-ttu-id="62855-115">值</span><span class="sxs-lookup"><span data-stu-id="62855-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62855-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62855-116">Minimum supported client</span></span><br/> | <span data-ttu-id="62855-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62855-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62855-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62855-118">Minimum supported server</span></span><br/> | <span data-ttu-id="62855-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62855-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62855-120">標頭</span><span class="sxs-lookup"><span data-stu-id="62855-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="62855-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="62855-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="62855-122">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="62855-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="62855-123">**HDN \_TRACKW** (Unicode) 和 **HDN \_ TRACKA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="62855-123">**HDN\_TRACKW** (Unicode) and **HDN\_TRACKA** (ANSI)</span></span><br/>                       |



 

 






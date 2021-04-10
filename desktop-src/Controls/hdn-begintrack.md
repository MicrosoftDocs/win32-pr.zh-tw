---
title: 'HDN_BEGINTRACK (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，使用者已開始拖曳控制項中的分隔線 (也就是說，當滑鼠游標位於標題控制項) 的分隔線上時，使用者按下滑鼠左鍵。
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- HDN_BEGINTRACK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106685"
---
# <a name="hdn_begintrack-notification-code"></a><span data-ttu-id="183ff-104">HDN \_ BEGINTRACK 通知碼</span><span class="sxs-lookup"><span data-stu-id="183ff-104">HDN\_BEGINTRACK notification code</span></span>

<span data-ttu-id="183ff-105">通知標題控制項的父視窗，使用者已開始拖曳控制項中的分隔線 (也就是說，當滑鼠游標位於標題控制項) 的分隔線上時，使用者按下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="183ff-105">Notifies a header control's parent window that the user has begun dragging a divider in the control (that is, the user has pressed the left mouse button while the mouse cursor is on a divider in the header control).</span></span> <span data-ttu-id="183ff-106">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="183ff-106">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="183ff-107">參數</span><span class="sxs-lookup"><span data-stu-id="183ff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="183ff-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="183ff-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="183ff-109">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項的相關資訊，以及要拖曳其分割的專案。</span><span class="sxs-lookup"><span data-stu-id="183ff-109">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is to be dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="183ff-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="183ff-110">Return value</span></span>

<span data-ttu-id="183ff-111">傳回 **FALSE** 以允許追蹤分隔，或為 **TRUE** 以防止追蹤。</span><span class="sxs-lookup"><span data-stu-id="183ff-111">Returns **FALSE** to allow tracking of the divider, or **TRUE** to prevent tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="183ff-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="183ff-112">Requirements</span></span>



| <span data-ttu-id="183ff-113">需求</span><span class="sxs-lookup"><span data-stu-id="183ff-113">Requirement</span></span> | <span data-ttu-id="183ff-114">值</span><span class="sxs-lookup"><span data-stu-id="183ff-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="183ff-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="183ff-115">Minimum supported client</span></span><br/> | <span data-ttu-id="183ff-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="183ff-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="183ff-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="183ff-117">Minimum supported server</span></span><br/> | <span data-ttu-id="183ff-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="183ff-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="183ff-119">標頭</span><span class="sxs-lookup"><span data-stu-id="183ff-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="183ff-120"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="183ff-120"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="183ff-121">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="183ff-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="183ff-122">**HDN \_BEGINTRACKW** (Unicode) 和 **HDN \_ BEGINTRACKA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="183ff-122">**HDN\_BEGINTRACKW** (Unicode) and **HDN\_BEGINTRACKA** (ANSI)</span></span><br/>             |



 

 






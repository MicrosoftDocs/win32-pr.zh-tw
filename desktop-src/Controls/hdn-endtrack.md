---
title: 'HDN_ENDTRACK (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，指出使用者已完成拖曳分隔線。 此通知碼以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- HDN_ENDTRACK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ab7625690a2de0414f1da391f26f919c1c2617
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024670"
---
# <a name="hdn_endtrack-notification-code"></a><span data-ttu-id="acd06-105">HDN \_ ENDTRACK 通知碼</span><span class="sxs-lookup"><span data-stu-id="acd06-105">HDN\_ENDTRACK notification code</span></span>

<span data-ttu-id="acd06-106">通知標題控制項的父視窗，指出使用者已完成拖曳分隔線。</span><span class="sxs-lookup"><span data-stu-id="acd06-106">Notifies a header control's parent window that the user has finished dragging a divider.</span></span> <span data-ttu-id="acd06-107">此通知碼以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="acd06-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="acd06-108">參數</span><span class="sxs-lookup"><span data-stu-id="acd06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acd06-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acd06-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acd06-110">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項的相關資訊，以及已拖曳其分割的專案。</span><span class="sxs-lookup"><span data-stu-id="acd06-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acd06-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="acd06-111">Return value</span></span>

<span data-ttu-id="acd06-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="acd06-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="acd06-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="acd06-113">Requirements</span></span>



| <span data-ttu-id="acd06-114">需求</span><span class="sxs-lookup"><span data-stu-id="acd06-114">Requirement</span></span> | <span data-ttu-id="acd06-115">值</span><span class="sxs-lookup"><span data-stu-id="acd06-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="acd06-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="acd06-116">Minimum supported client</span></span><br/> | <span data-ttu-id="acd06-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acd06-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="acd06-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="acd06-118">Minimum supported server</span></span><br/> | <span data-ttu-id="acd06-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acd06-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="acd06-120">標頭</span><span class="sxs-lookup"><span data-stu-id="acd06-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="acd06-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="acd06-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="acd06-122">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="acd06-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="acd06-123">**HDN \_ENDTRACKW** (Unicode) 和 **HDN \_ ENDTRACKA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="acd06-123">**HDN\_ENDTRACKW** (Unicode) and **HDN\_ENDTRACKA** (ANSI)</span></span><br/>                 |



 

 






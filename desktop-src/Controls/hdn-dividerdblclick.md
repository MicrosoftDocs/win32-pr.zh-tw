---
title: 'HDN_DIVIDERDBLCLICK (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，使用者按兩下控制項的 [分割區] 區域。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- HDN_DIVIDERDBLCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129096139a4d698f25de543a2628b473bfd66e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025508"
---
# <a name="hdn_dividerdblclick-notification-code"></a><span data-ttu-id="6dc75-105">HDN \_ DIVIDERDBLCLICK 通知碼</span><span class="sxs-lookup"><span data-stu-id="6dc75-105">HDN\_DIVIDERDBLCLICK notification code</span></span>

<span data-ttu-id="6dc75-106">通知標題控制項的父視窗，使用者按兩下控制項的 [分割區] 區域。</span><span class="sxs-lookup"><span data-stu-id="6dc75-106">Notifies a header control's parent window that the user double-clicked the divider area of the control.</span></span> <span data-ttu-id="6dc75-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="6dc75-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6dc75-108">參數</span><span class="sxs-lookup"><span data-stu-id="6dc75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dc75-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6dc75-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6dc75-110">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項的相關資訊，以及按兩下其分隔線的專案。</span><span class="sxs-lookup"><span data-stu-id="6dc75-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was double-clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dc75-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6dc75-111">Return value</span></span>

<span data-ttu-id="6dc75-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6dc75-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dc75-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dc75-113">Requirements</span></span>



| <span data-ttu-id="6dc75-114">需求</span><span class="sxs-lookup"><span data-stu-id="6dc75-114">Requirement</span></span> | <span data-ttu-id="6dc75-115">值</span><span class="sxs-lookup"><span data-stu-id="6dc75-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc75-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6dc75-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6dc75-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dc75-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6dc75-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6dc75-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6dc75-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dc75-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6dc75-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6dc75-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dc75-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6dc75-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6dc75-122">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="6dc75-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6dc75-123">**HDN \_DIVIDERDBLCLICKW** (Unicode) 和 **HDN \_ DIVIDERDBLCLICKA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="6dc75-123">**HDN\_DIVIDERDBLCLICKW** (Unicode) and **HDN\_DIVIDERDBLCLICKA** (ANSI)</span></span><br/>   |



 

 






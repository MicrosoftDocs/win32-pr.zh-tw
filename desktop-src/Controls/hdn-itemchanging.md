---
title: 'HDN_ITEMCHANGING (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，標題專案的屬性即將變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- HDN_ITEMCHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843148"
---
# <a name="hdn_itemchanging-notification-code"></a><span data-ttu-id="b481d-105">HDN \_ ITEMCHANGING 通知碼</span><span class="sxs-lookup"><span data-stu-id="b481d-105">HDN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="b481d-106">通知標題控制項的父視窗，標題專案的屬性即將變更。</span><span class="sxs-lookup"><span data-stu-id="b481d-106">Notifies a header control's parent window that the attributes of a header item are about to change.</span></span> <span data-ttu-id="b481d-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="b481d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b481d-108">參數</span><span class="sxs-lookup"><span data-stu-id="b481d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b481d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b481d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b481d-110">[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項和標頭專案的相關資訊，包括即將變更的屬性。</span><span class="sxs-lookup"><span data-stu-id="b481d-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b481d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b481d-111">Return value</span></span>

<span data-ttu-id="b481d-112">傳回 **FALSE** 表示允許變更，或 **TRUE** 表示防止這些變更。</span><span class="sxs-lookup"><span data-stu-id="b481d-112">Returns **FALSE** to allow the changes, or **TRUE** to prevent them.</span></span>

## <a name="requirements"></a><span data-ttu-id="b481d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b481d-113">Requirements</span></span>



| <span data-ttu-id="b481d-114">需求</span><span class="sxs-lookup"><span data-stu-id="b481d-114">Requirement</span></span> | <span data-ttu-id="b481d-115">值</span><span class="sxs-lookup"><span data-stu-id="b481d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b481d-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b481d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b481d-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b481d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b481d-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b481d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b481d-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b481d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b481d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b481d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b481d-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b481d-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b481d-122">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b481d-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b481d-123">**HDN \_ITEMCHANGINGW** (Unicode) 和 **HDN \_ ITEMCHANGINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b481d-123">**HDN\_ITEMCHANGINGW** (Unicode) and **HDN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



 

 






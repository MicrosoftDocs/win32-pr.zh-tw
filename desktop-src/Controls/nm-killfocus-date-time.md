---
title: 'NM_KILLFOCUS (日期時間) 通知碼 (Commctrl) '
description: 通知日期和時間選擇器控制項的父視窗，表示控制項已遺失輸入焦點。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 33d6b88b-9608-4227-a822-1dc7a77d3a3f
keywords:
- NM_KILLFOCUS (日期時間) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af47dca130d1025341e2a3c625c1bf7a9c44c42a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933912"
---
# <a name="nm_killfocus-date-time-notification-code"></a><span data-ttu-id="e2dac-105">NM \_ KILLFOCUS (日期時間) 通知碼</span><span class="sxs-lookup"><span data-stu-id="e2dac-105">NM\_KILLFOCUS (date time) notification code</span></span>

<span data-ttu-id="e2dac-106">通知日期和時間選擇器控制項的父視窗，表示控制項已遺失輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="e2dac-106">Notifies a date and time picker control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="e2dac-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="e2dac-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e2dac-108">參數</span><span class="sxs-lookup"><span data-stu-id="e2dac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2dac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2dac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2dac-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的位址，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e2dac-110">The address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2dac-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2dac-111">Return value</span></span>

<span data-ttu-id="e2dac-112">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="e2dac-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2dac-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2dac-113">Requirements</span></span>



| <span data-ttu-id="e2dac-114">需求</span><span class="sxs-lookup"><span data-stu-id="e2dac-114">Requirement</span></span> | <span data-ttu-id="e2dac-115">值</span><span class="sxs-lookup"><span data-stu-id="e2dac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2dac-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2dac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2dac-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2dac-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2dac-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2dac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2dac-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2dac-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2dac-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e2dac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2dac-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2dac-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






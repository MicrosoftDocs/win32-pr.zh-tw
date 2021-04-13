---
title: 'DTN_FORMAT (Commctrl 的通知碼) '
description: 由日期和時間選擇器所傳送 (DTP) 控制項，要求在回呼欄位中顯示文字。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- DTN_FORMAT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fadd11b090777d2226eeed85f32d2062e8340e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465920"
---
# <a name="dtn_format-notification-code"></a><span data-ttu-id="a96f4-105">DTN \_ 格式通知碼</span><span class="sxs-lookup"><span data-stu-id="a96f4-105">DTN\_FORMAT notification code</span></span>

<span data-ttu-id="a96f4-106">由日期和時間選擇器所傳送 (DTP) 控制項，要求在回呼欄位中顯示文字。</span><span class="sxs-lookup"><span data-stu-id="a96f4-106">Sent by a date and time picker (DTP) control to request text to be displayed in a callback field.</span></span> <span data-ttu-id="a96f4-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="a96f4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a96f4-108">參數</span><span class="sxs-lookup"><span data-stu-id="a96f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a96f4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a96f4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a96f4-110">[**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata)結構的指標，其中包含此通知碼實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a96f4-110">A pointer to an [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) structure containing information regarding this instance of the notification code.</span></span> <span data-ttu-id="a96f4-111">結構包含定義回呼欄位的子字串，並接收控制項將顯示的格式化字串。</span><span class="sxs-lookup"><span data-stu-id="a96f4-111">The structure contains the substring that defines the callback field and receives the formatted string that the control will display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a96f4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a96f4-112">Return value</span></span>

<span data-ttu-id="a96f4-113">控制項的擁有者必須傳回零。</span><span class="sxs-lookup"><span data-stu-id="a96f4-113">The owner of the control must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a96f4-114">備註</span><span class="sxs-lookup"><span data-stu-id="a96f4-114">Remarks</span></span>

<span data-ttu-id="a96f4-115">處理此通知碼可讓控制項的擁有者提供控制項將顯示的自訂字串。</span><span class="sxs-lookup"><span data-stu-id="a96f4-115">Handling this notification code allows the owner of the control to provide a custom string that the control will display.</span></span> <span data-ttu-id="a96f4-116"> (如需回呼欄位的其他資訊，請參閱 [回呼欄位](date-and-time-picker-controls.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="a96f4-116">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="a96f4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a96f4-117">Requirements</span></span>



| <span data-ttu-id="a96f4-118">需求</span><span class="sxs-lookup"><span data-stu-id="a96f4-118">Requirement</span></span> | <span data-ttu-id="a96f4-119">值</span><span class="sxs-lookup"><span data-stu-id="a96f4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a96f4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a96f4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a96f4-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a96f4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a96f4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a96f4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a96f4-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a96f4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a96f4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a96f4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a96f4-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a96f4-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a96f4-126">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a96f4-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a96f4-127">**DTN \_FORMATW** (Unicode) 和 **DTN \_ FORMATA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a96f4-127">**DTN\_FORMATW** (Unicode) and **DTN\_FORMATA** (ANSI)</span></span><br/>                     |



 

 






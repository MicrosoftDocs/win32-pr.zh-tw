---
title: 'DTN_FORMATQUERY (Commctrl 的通知碼) '
description: 由日期和時間選擇器所傳送 (DTP) 控制項，以取得將顯示在回呼欄位中之字串的允許大小上限。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- DTN_FORMATQUERY 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e9653f369f13e0ef4a775265d763e854db4de7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933964"
---
# <a name="dtn_formatquery-notification-code"></a><span data-ttu-id="37d6d-105">DTN \_ FORMATQUERY 通知碼</span><span class="sxs-lookup"><span data-stu-id="37d6d-105">DTN\_FORMATQUERY notification code</span></span>

<span data-ttu-id="37d6d-106">由日期和時間選擇器所傳送 (DTP) 控制項，以取得將顯示在回呼欄位中之字串的允許大小上限。</span><span class="sxs-lookup"><span data-stu-id="37d6d-106">Sent by a date and time picker (DTP) control to retrieve the maximum allowable size of the string that will be displayed in a callback field.</span></span> <span data-ttu-id="37d6d-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="37d6d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="37d6d-108">參數</span><span class="sxs-lookup"><span data-stu-id="37d6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37d6d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37d6d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37d6d-110">[**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya)結構的指標，其中包含回呼欄位的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="37d6d-110">A pointer to an [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure containing information about the callback field.</span></span> <span data-ttu-id="37d6d-111">結構包含定義回呼欄位的子字串，並接收將在回呼欄位中顯示之字串的最大允許大小。</span><span class="sxs-lookup"><span data-stu-id="37d6d-111">The structure contains a substring that defines a callback field and receives the maximum allowable size of the string that will be displayed in the callback field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37d6d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="37d6d-112">Return value</span></span>

<span data-ttu-id="37d6d-113">控制項的擁有者必須計算將顯示在回呼欄位中之文字的最大可能寬度、設定 [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya)結構的 **szMax** 成員，然後傳回零。</span><span class="sxs-lookup"><span data-stu-id="37d6d-113">The owner of the control must calculate the maximum possible width of the text that will be displayed in the callback field, set the **szMax** member of the [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure, and return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="37d6d-114">備註</span><span class="sxs-lookup"><span data-stu-id="37d6d-114">Remarks</span></span>

<span data-ttu-id="37d6d-115">處理此通知程式碼可讓控制項進行調整，以調整將顯示在特定回呼欄位中的字串大小上限。</span><span class="sxs-lookup"><span data-stu-id="37d6d-115">Handling this notification code prepares the control to adjust for the maximum size of the string that will be displayed in a particular callback field.</span></span> <span data-ttu-id="37d6d-116">這樣可讓控制項隨時適當地顯示輸出，減少控制項顯示內的閃爍。</span><span class="sxs-lookup"><span data-stu-id="37d6d-116">This enables the control to properly display output at all times, reducing flicker within the control's display.</span></span> <span data-ttu-id="37d6d-117"> (如需回呼欄位的其他資訊，請參閱 [回呼欄位](date-and-time-picker-controls.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="37d6d-117">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="37d6d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="37d6d-118">Requirements</span></span>



| <span data-ttu-id="37d6d-119">需求</span><span class="sxs-lookup"><span data-stu-id="37d6d-119">Requirement</span></span> | <span data-ttu-id="37d6d-120">值</span><span class="sxs-lookup"><span data-stu-id="37d6d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37d6d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37d6d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="37d6d-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37d6d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37d6d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37d6d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="37d6d-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37d6d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37d6d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="37d6d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="37d6d-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="37d6d-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="37d6d-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="37d6d-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="37d6d-128">**DTN \_FORMATQUERYW** (Unicode) 和 **DTN \_ FORMATQUERYA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="37d6d-128">**DTN\_FORMATQUERYW** (Unicode) and **DTN\_FORMATQUERYA** (ANSI)</span></span><br/>           |



 

 






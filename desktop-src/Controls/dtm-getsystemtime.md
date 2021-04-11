---
title: 'DTM_GETSYSTEMTIME 訊息 (Commctrl .h) '
description: 從日期和時間選擇器取得目前選取的時間 (DTP) 控制項，並將它放在指定的 SYSTEMTIME 結構中。 您可以明確地傳送此訊息，或使用 DateTime \_ GetSystemtime 宏。
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- DTM_GETSYSTEMTIME message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104843"
---
# <a name="dtm_getsystemtime-message"></a><span data-ttu-id="0f274-105">DTM \_ GETSYSTEMTIME 訊息</span><span class="sxs-lookup"><span data-stu-id="0f274-105">DTM\_GETSYSTEMTIME message</span></span>

<span data-ttu-id="0f274-106">從日期和時間選擇器取得目前選取的時間 (DTP) 控制項，並將它放在指定的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構中。</span><span class="sxs-lookup"><span data-stu-id="0f274-106">Gets the currently selected time from a date and time picker (DTP) control and places it in a specified [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="0f274-107">您可以明確地傳送此訊息，或使用 [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) 宏。</span><span class="sxs-lookup"><span data-stu-id="0f274-107">You can send this message explicitly or use the [**DateTime\_GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f274-108">參數</span><span class="sxs-lookup"><span data-stu-id="0f274-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f274-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f274-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0f274-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0f274-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0f274-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f274-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f274-112">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0f274-112">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="0f274-113">如果 **DTM \_ GETSYSTEMTIME** 傳回 GDT \_ VALID，此結構將會包含目前所選取的時間。</span><span class="sxs-lookup"><span data-stu-id="0f274-113">If **DTM\_GETSYSTEMTIME** returns GDT\_VALID, this structure will contain the currently selected time.</span></span> <span data-ttu-id="0f274-114">否則，它不會包含有效的資訊。</span><span class="sxs-lookup"><span data-stu-id="0f274-114">Otherwise, it will not contain valid information.</span></span> <span data-ttu-id="0f274-115">此參數必須是有效的指標;它不能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0f274-115">This parameter must be a valid pointer; it cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f274-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f274-116">Return value</span></span>

<span data-ttu-id="0f274-117">\_如果成功將時間資訊放入 *lParam* 中，則傳回 GDT 有效。</span><span class="sxs-lookup"><span data-stu-id="0f274-117">Returns GDT\_VALID if the time information was successfully placed in *lParam*.</span></span> <span data-ttu-id="0f274-118">\_如果控制項設定為 [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md)樣式，而且沒有選取控制項核取方塊，則會傳回 GDT NONE。</span><span class="sxs-lookup"><span data-stu-id="0f274-118">Returns GDT\_NONE if the control was set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style and the control check box was not selected.</span></span> <span data-ttu-id="0f274-119">\_如果發生錯誤，則傳回 GDT 錯誤。</span><span class="sxs-lookup"><span data-stu-id="0f274-119">Returns GDT\_ERROR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f274-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f274-120">Requirements</span></span>



| <span data-ttu-id="0f274-121">需求</span><span class="sxs-lookup"><span data-stu-id="0f274-121">Requirement</span></span> | <span data-ttu-id="0f274-122">值</span><span class="sxs-lookup"><span data-stu-id="0f274-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f274-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f274-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0f274-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f274-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f274-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f274-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0f274-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f274-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f274-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0f274-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f274-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f274-128"><dt>Commctrl.h</dt></span></span> </dl> |



 


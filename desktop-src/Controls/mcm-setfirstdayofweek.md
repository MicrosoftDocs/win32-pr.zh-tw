---
title: 'MCM_SETFIRSTDAYOFWEEK 訊息 (Commctrl .h) '
description: 設定月曆控制項的每週第一天。 您可以使用 MonthCal SetFirstDayOfWeek 宏明確地傳送此訊息 \_ 。
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- MCM_SETFIRSTDAYOFWEEK message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32452c9043bbd7c3bbcf96f9dc32e67714eacce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967762"
---
# <a name="mcm_setfirstdayofweek-message"></a><span data-ttu-id="14b04-105">MCM \_ SETFIRSTDAYOFWEEK 訊息</span><span class="sxs-lookup"><span data-stu-id="14b04-105">MCM\_SETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="14b04-106">設定月曆控制項的每週第一天。</span><span class="sxs-lookup"><span data-stu-id="14b04-106">Sets the first day of the week for a month calendar control.</span></span> <span data-ttu-id="14b04-107">您可以使用 [**MonthCal \_ SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="14b04-107">You can send this message explicitly or by using the [**MonthCal\_SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="14b04-108">參數</span><span class="sxs-lookup"><span data-stu-id="14b04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b04-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14b04-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="14b04-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="14b04-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="14b04-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14b04-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14b04-112">**Int** 類型的值，代表要將哪一天設定為星期幾的第一天，其中0是星期一、1是星期二等等。</span><span class="sxs-lookup"><span data-stu-id="14b04-112">Value of type **int** representing which day is to be set as the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b04-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="14b04-113">Return value</span></span>

<span data-ttu-id="14b04-114">傳回包含兩個值的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="14b04-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="14b04-115">如果第一周的第一天不等於地區設定 IFIRSTDAYOFWEEK，則最 **大的單字** 為非零值，否則為 \_ 零。</span><span class="sxs-lookup"><span data-stu-id="14b04-115">The high word is a **BOOL** value that is nonzero if the previous first day of the week did not equal LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="14b04-116">低字組是一個 INT 值，代表一周的前一天。</span><span class="sxs-lookup"><span data-stu-id="14b04-116">The low word is an INT value that represents the previous first day of the week.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b04-117">備註</span><span class="sxs-lookup"><span data-stu-id="14b04-117">Remarks</span></span>

<span data-ttu-id="14b04-118">如果一周的第一天設定為預設 (地區設定 IFIRSTDAYOFWEEK) 以外的任何值 \_ ，則此控制項不會根據地區設定變更自動更新第一天的變更。</span><span class="sxs-lookup"><span data-stu-id="14b04-118">If the first day of the week is set to anything other than the default (LOCALE\_IFIRSTDAYOFWEEK), the control will not automatically update first-day-of-the-week changes based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b04-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="14b04-119">Requirements</span></span>



| <span data-ttu-id="14b04-120">需求</span><span class="sxs-lookup"><span data-stu-id="14b04-120">Requirement</span></span> | <span data-ttu-id="14b04-121">值</span><span class="sxs-lookup"><span data-stu-id="14b04-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14b04-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14b04-122">Minimum supported client</span></span><br/> | <span data-ttu-id="14b04-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14b04-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14b04-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14b04-124">Minimum supported server</span></span><br/> | <span data-ttu-id="14b04-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14b04-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14b04-126">標頭</span><span class="sxs-lookup"><span data-stu-id="14b04-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="14b04-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="14b04-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






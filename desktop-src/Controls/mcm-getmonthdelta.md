---
title: 'MCM_GETMONTHDELTA 訊息 (Commctrl .h) '
description: 抓取月曆控制項的滾動速率。 捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。 您可以使用 MonthCal GetMonthDelta 宏明確地傳送此訊息 \_ 。
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- MCM_GETMONTHDELTA message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01eaa40b930e6317cc2be6b674f0cea58115ae40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106661"
---
# <a name="mcm_getmonthdelta-message"></a><span data-ttu-id="2fb78-106">MCM \_ GETMONTHDELTA 訊息</span><span class="sxs-lookup"><span data-stu-id="2fb78-106">MCM\_GETMONTHDELTA message</span></span>

<span data-ttu-id="2fb78-107">抓取月曆控制項的滾動速率。</span><span class="sxs-lookup"><span data-stu-id="2fb78-107">Retrieves the scroll rate for a month calendar control.</span></span> <span data-ttu-id="2fb78-108">捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。</span><span class="sxs-lookup"><span data-stu-id="2fb78-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="2fb78-109">您可以使用 [**MonthCal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2fb78-109">You can send this message explicitly or by using the [**MonthCal\_GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2fb78-110">參數</span><span class="sxs-lookup"><span data-stu-id="2fb78-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fb78-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2fb78-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2fb78-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2fb78-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2fb78-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2fb78-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2fb78-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2fb78-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fb78-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2fb78-115">Return value</span></span>

<span data-ttu-id="2fb78-116">如果先前使用 [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) 訊息設定了月份差異，則會傳回代表月曆目前滾動率的 INT 值。</span><span class="sxs-lookup"><span data-stu-id="2fb78-116">If the month delta was previously set using the [**MCM\_SETMONTHDELTA**](mcm-setmonthdelta.md) message, returns an INT value that represents the month calendar's current scroll rate.</span></span> <span data-ttu-id="2fb78-117">如果先前未使用 **MCM \_ SETMONTHDELTA** 訊息來設定月份差異，或重設為預設的月差異，則會傳回 INT 值，代表目前可見的月數。</span><span class="sxs-lookup"><span data-stu-id="2fb78-117">If the month delta was not previously set using the **MCM\_SETMONTHDELTA** message, or the month delta was reset to the default, returns an INT value that represents the current number of months visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fb78-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fb78-118">Requirements</span></span>



| <span data-ttu-id="2fb78-119">需求</span><span class="sxs-lookup"><span data-stu-id="2fb78-119">Requirement</span></span> | <span data-ttu-id="2fb78-120">值</span><span class="sxs-lookup"><span data-stu-id="2fb78-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb78-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fb78-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb78-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fb78-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2fb78-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fb78-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb78-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fb78-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2fb78-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2fb78-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fb78-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2fb78-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






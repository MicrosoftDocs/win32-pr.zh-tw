---
title: 'MCM_GETMAXTODAYWIDTH 訊息 (Commctrl .h) '
description: 抓取 \ 0034 的最大寬度; today \ 0034;月曆控制項中的字串。 這包括標籤文字和日期文字。 您可以使用 MonthCal GetMaxTodayWidth 宏明確地傳送此訊息 \_ 。
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- MCM_GETMAXTODAYWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685987"
---
# <a name="mcm_getmaxtodaywidth-message"></a><span data-ttu-id="8c9a2-106">MCM \_ GETMAXTODAYWIDTH 訊息</span><span class="sxs-lookup"><span data-stu-id="8c9a2-106">MCM\_GETMAXTODAYWIDTH message</span></span>

<span data-ttu-id="8c9a2-107">抓取月曆控制項中 "today" 字串的最大寬度。</span><span class="sxs-lookup"><span data-stu-id="8c9a2-107">Retrieves the maximum width of the "today" string in a month calendar control.</span></span> <span data-ttu-id="8c9a2-108">這包括標籤文字和日期文字。</span><span class="sxs-lookup"><span data-stu-id="8c9a2-108">This includes the label text and the date text.</span></span> <span data-ttu-id="8c9a2-109">您可以使用 [**MonthCal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8c9a2-109">You can send this message explicitly or by using the [**MonthCal\_GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c9a2-110">參數</span><span class="sxs-lookup"><span data-stu-id="8c9a2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c9a2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c9a2-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8c9a2-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8c9a2-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8c9a2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c9a2-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8c9a2-114">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8c9a2-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c9a2-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c9a2-115">Return value</span></span>

<span data-ttu-id="8c9a2-116">傳回 "today" 字串的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c9a2-116">Returns the width of the "today" string, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c9a2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c9a2-117">Requirements</span></span>



| <span data-ttu-id="8c9a2-118">需求</span><span class="sxs-lookup"><span data-stu-id="8c9a2-118">Requirement</span></span> | <span data-ttu-id="8c9a2-119">值</span><span class="sxs-lookup"><span data-stu-id="8c9a2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9a2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c9a2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c9a2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c9a2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c9a2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c9a2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c9a2-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c9a2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c9a2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8c9a2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c9a2-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c9a2-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: 'MCM_SIZERECTTOMIN 訊息 (Commctrl .h) '
description: 計算給定矩形中可容納多少日曆，然後傳回矩形必須符合該行事歷數量的最小值。 您可以使用 MonthCal SizeRectToMin 宏明確地傳送此訊息 \_ 。
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- MCM_SIZERECTTOMIN message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f525f4cca9280b92fab0b9b86aa1d950ed990ef4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105983"
---
# <a name="mcm_sizerecttomin-message"></a><span data-ttu-id="7dbe6-105">MCM \_ SIZERECTTOMIN 訊息</span><span class="sxs-lookup"><span data-stu-id="7dbe6-105">MCM\_SIZERECTTOMIN message</span></span>

<span data-ttu-id="7dbe6-106">計算給定矩形中可容納多少日曆，然後傳回矩形必須符合該行事歷數量的最小值。</span><span class="sxs-lookup"><span data-stu-id="7dbe6-106">Calculates how many calendars will fit in the given rectangle, and then returns the minimum size that a rectangle needs to be to fit that number of calendars.</span></span> <span data-ttu-id="7dbe6-107">您可以使用 [**MonthCal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="7dbe6-107">You can send this message explicitly or by using the [**MonthCal\_SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7dbe6-108">參數</span><span class="sxs-lookup"><span data-stu-id="7dbe6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dbe6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7dbe6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dbe6-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7dbe6-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7dbe6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7dbe6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dbe6-112">On 專案時，會包含一個 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構的指標，此結構描述的區域大於或等於符合所需的行事歷數目所需的大小。</span><span class="sxs-lookup"><span data-stu-id="7dbe6-112">On entry, contains a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that describes a region that is greater than or equal to the size necessary to fit the desired number of calendars.</span></span> <span data-ttu-id="7dbe6-113">當此函式傳回時，會包含適合此日曆數目的最小 **矩形** 結構。</span><span class="sxs-lookup"><span data-stu-id="7dbe6-113">When this function returns, contains the minimum **RECT** structure that fits this number of calendars.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dbe6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7dbe6-114">Return value</span></span>

<span data-ttu-id="7dbe6-115">未使用的。</span><span class="sxs-lookup"><span data-stu-id="7dbe6-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dbe6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dbe6-116">Requirements</span></span>



| <span data-ttu-id="7dbe6-117">需求</span><span class="sxs-lookup"><span data-stu-id="7dbe6-117">Requirement</span></span> | <span data-ttu-id="7dbe6-118">值</span><span class="sxs-lookup"><span data-stu-id="7dbe6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dbe6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7dbe6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7dbe6-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7dbe6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7dbe6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7dbe6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7dbe6-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7dbe6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7dbe6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7dbe6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dbe6-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7dbe6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 


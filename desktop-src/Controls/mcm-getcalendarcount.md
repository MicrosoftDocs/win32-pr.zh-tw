---
title: 'MCM_GETCALENDARCOUNT 訊息 (Commctrl .h) '
description: 取得目前在行事曆控制項中顯示的行事歷數目。 您可以使用 MonthCal GetCalendarCount 宏明確地傳送此訊息 \_ 。
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- MCM_GETCALENDARCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a3be9e9bcc5db8c1aab32cacbcc2ded82727af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104807"
---
# <a name="mcm_getcalendarcount-message"></a><span data-ttu-id="8e958-105">MCM \_ GETCALENDARCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="8e958-105">MCM\_GETCALENDARCOUNT message</span></span>

<span data-ttu-id="8e958-106">取得目前在行事曆控制項中顯示的行事歷數目。</span><span class="sxs-lookup"><span data-stu-id="8e958-106">Gets the number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="8e958-107">您可以使用 [**MonthCal \_ GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8e958-107">You can send this message explicitly or by using the [**MonthCal\_GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e958-108">參數</span><span class="sxs-lookup"><span data-stu-id="8e958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e958-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e958-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e958-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8e958-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8e958-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e958-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e958-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8e958-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e958-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e958-113">Return value</span></span>

<span data-ttu-id="8e958-114">行事曆控制項目前顯示的行事歷數目。</span><span class="sxs-lookup"><span data-stu-id="8e958-114">Number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="8e958-115">允許的行事歷數目上限為12。</span><span class="sxs-lookup"><span data-stu-id="8e958-115">The maximum number of allowed calendars is 12.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e958-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e958-116">Requirements</span></span>



| <span data-ttu-id="8e958-117">需求</span><span class="sxs-lookup"><span data-stu-id="8e958-117">Requirement</span></span> | <span data-ttu-id="8e958-118">值</span><span class="sxs-lookup"><span data-stu-id="8e958-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e958-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e958-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8e958-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e958-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e958-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e958-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8e958-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e958-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e958-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8e958-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e958-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8e958-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






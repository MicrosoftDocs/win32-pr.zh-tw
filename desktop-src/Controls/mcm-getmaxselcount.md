---
title: 'MCM_GETMAXSELCOUNT 訊息 (Commctrl .h) '
description: 抓取月曆控制項中可選取的最大日期範圍。 您可以使用 MonthCal GetMaxSelCount 宏明確地傳送此訊息 \_ 。
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- MCM_GETMAXSELCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025250"
---
# <a name="mcm_getmaxselcount-message"></a><span data-ttu-id="58bd4-105">MCM \_ GETMAXSELCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="58bd4-105">MCM\_GETMAXSELCOUNT message</span></span>

<span data-ttu-id="58bd4-106">抓取月曆控制項中可選取的最大日期範圍。</span><span class="sxs-lookup"><span data-stu-id="58bd4-106">Retrieves the maximum date range that can be selected in a month calendar control.</span></span> <span data-ttu-id="58bd4-107">您可以使用 [**MonthCal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="58bd4-107">You can send this message explicitly or by using the [**MonthCal\_GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="58bd4-108">參數</span><span class="sxs-lookup"><span data-stu-id="58bd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58bd4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58bd4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="58bd4-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="58bd4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="58bd4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58bd4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="58bd4-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="58bd4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58bd4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="58bd4-113">Return value</span></span>

<span data-ttu-id="58bd4-114">傳回 INT 值，代表可以為控制項選取的總天數。</span><span class="sxs-lookup"><span data-stu-id="58bd4-114">Returns an INT value that represents the total number of days that can be selected for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="58bd4-115">備註</span><span class="sxs-lookup"><span data-stu-id="58bd4-115">Remarks</span></span>

<span data-ttu-id="58bd4-116">您可以使用 [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) 訊息來變更可選取的最大日期範圍。</span><span class="sxs-lookup"><span data-stu-id="58bd4-116">You can change the maximum date range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="58bd4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="58bd4-117">Requirements</span></span>



| <span data-ttu-id="58bd4-118">需求</span><span class="sxs-lookup"><span data-stu-id="58bd4-118">Requirement</span></span> | <span data-ttu-id="58bd4-119">值</span><span class="sxs-lookup"><span data-stu-id="58bd4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58bd4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58bd4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="58bd4-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58bd4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58bd4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58bd4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="58bd4-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58bd4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58bd4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="58bd4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="58bd4-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="58bd4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






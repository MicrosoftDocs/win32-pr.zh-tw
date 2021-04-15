---
title: 'MCM_GETCURRENTVIEW 訊息 (Commctrl .h) '
description: 取得行事曆的目前視圖。 您可以使用 MonthCal GetCurrentView 宏明確地傳送此訊息 \_ 。
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- MCM_GETCURRENTVIEW message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466492"
---
# <a name="mcm_getcurrentview-message"></a><span data-ttu-id="c5dcc-105">MCM \_ GETCURRENTVIEW 訊息</span><span class="sxs-lookup"><span data-stu-id="c5dcc-105">MCM\_GETCURRENTVIEW message</span></span>

<span data-ttu-id="c5dcc-106">取得行事曆的目前視圖。</span><span class="sxs-lookup"><span data-stu-id="c5dcc-106">Gets the current view of the calendar.</span></span> <span data-ttu-id="c5dcc-107">您可以使用 [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c5dcc-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5dcc-108">參數</span><span class="sxs-lookup"><span data-stu-id="c5dcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5dcc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5dcc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5dcc-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c5dcc-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c5dcc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5dcc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5dcc-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c5dcc-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5dcc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5dcc-113">Return value</span></span>

<span data-ttu-id="c5dcc-114">目前的觀點。</span><span class="sxs-lookup"><span data-stu-id="c5dcc-114">Current view.</span></span> <span data-ttu-id="c5dcc-115">下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c5dcc-115">One of the following values.</span></span>



| <span data-ttu-id="c5dcc-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c5dcc-116">Return code</span></span>                                                                                  | <span data-ttu-id="c5dcc-117">Description</span><span class="sxs-lookup"><span data-stu-id="c5dcc-117">Description</span></span>              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="c5dcc-118"><dt>**MCMV \_ 月份**</dt></span><span class="sxs-lookup"><span data-stu-id="c5dcc-118"><dt>**MCMV\_MONTH**</dt></span></span> </dl>   | <span data-ttu-id="c5dcc-119">每月的觀點。</span><span class="sxs-lookup"><span data-stu-id="c5dcc-119">Monthly view.</span></span><br/> |
| <dl> <span data-ttu-id="c5dcc-120"><dt>**MCMV \_ 年**</dt></span><span class="sxs-lookup"><span data-stu-id="c5dcc-120"><dt>**MCMV\_YEAR**</dt></span></span> </dl>    | <span data-ttu-id="c5dcc-121">年度觀點。</span><span class="sxs-lookup"><span data-stu-id="c5dcc-121">Annual view.</span></span><br/>  |
| <dl> <span data-ttu-id="c5dcc-122"><dt>**MCMV \_ 十年**</dt></span><span class="sxs-lookup"><span data-stu-id="c5dcc-122"><dt>**MCMV\_DECADE**</dt></span></span> </dl>  | <span data-ttu-id="c5dcc-123">十年的觀點。</span><span class="sxs-lookup"><span data-stu-id="c5dcc-123">Decade view.</span></span><br/>  |
| <dl> <span data-ttu-id="c5dcc-124"><dt>**MCMV \_ 世紀**</dt></span><span class="sxs-lookup"><span data-stu-id="c5dcc-124"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="c5dcc-125">世紀的觀點。</span><span class="sxs-lookup"><span data-stu-id="c5dcc-125">Century view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c5dcc-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5dcc-126">Requirements</span></span>



| <span data-ttu-id="c5dcc-127">需求</span><span class="sxs-lookup"><span data-stu-id="c5dcc-127">Requirement</span></span> | <span data-ttu-id="c5dcc-128">值</span><span class="sxs-lookup"><span data-stu-id="c5dcc-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5dcc-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5dcc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c5dcc-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5dcc-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5dcc-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5dcc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c5dcc-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5dcc-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5dcc-133">標頭</span><span class="sxs-lookup"><span data-stu-id="c5dcc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5dcc-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5dcc-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






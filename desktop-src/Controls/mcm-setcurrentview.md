---
title: 'MCM_SETCURRENTVIEW 訊息 (Commctrl .h) '
description: 設定行事曆的目前視圖。 您可以使用 MonthCal SetCurrentView 宏明確地傳送此訊息 \_ 。
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- MCM_SETCURRENTVIEW message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d383c984932c19805f452cb39841c2edf36809b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935012"
---
# <a name="mcm_setcurrentview-message"></a><span data-ttu-id="1a728-105">MCM \_ SETCURRENTVIEW 訊息</span><span class="sxs-lookup"><span data-stu-id="1a728-105">MCM\_SETCURRENTVIEW message</span></span>

<span data-ttu-id="1a728-106">設定行事曆的目前視圖。</span><span class="sxs-lookup"><span data-stu-id="1a728-106">Sets the current view of the calendar.</span></span> <span data-ttu-id="1a728-107">您可以使用 [**MonthCal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1a728-107">You can send this message explicitly or by using the [**MonthCal\_SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a728-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a728-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a728-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a728-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a728-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1a728-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1a728-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a728-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a728-112">新觀點。</span><span class="sxs-lookup"><span data-stu-id="1a728-112">New view.</span></span> <span data-ttu-id="1a728-113">下列其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="1a728-113">One of the following constants.</span></span>



| <span data-ttu-id="1a728-114">值</span><span class="sxs-lookup"><span data-stu-id="1a728-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="1a728-115">意義</span><span class="sxs-lookup"><span data-stu-id="1a728-115">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <span data-ttu-id="1a728-116"><dt>**MCMV \_ 月份**</dt></span><span class="sxs-lookup"><span data-stu-id="1a728-116"><dt>**MCMV\_MONTH**</dt></span></span> </dl>       | <span data-ttu-id="1a728-117">每月的觀點。</span><span class="sxs-lookup"><span data-stu-id="1a728-117">Monthly view.</span></span><br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <span data-ttu-id="1a728-118"><dt>**MCMV \_ 年**</dt></span><span class="sxs-lookup"><span data-stu-id="1a728-118"><dt>**MCMV\_YEAR**</dt></span></span> </dl>          | <span data-ttu-id="1a728-119">年度觀點。</span><span class="sxs-lookup"><span data-stu-id="1a728-119">Annual view.</span></span><br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <span data-ttu-id="1a728-120"><dt>**MCMV \_ 十年**</dt></span><span class="sxs-lookup"><span data-stu-id="1a728-120"><dt>**MCMV\_DECADE**</dt></span></span> </dl>    | <span data-ttu-id="1a728-121">十年的觀點。</span><span class="sxs-lookup"><span data-stu-id="1a728-121">Decade view.</span></span><br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <span data-ttu-id="1a728-122"><dt>**MCMV \_ 世紀**</dt></span><span class="sxs-lookup"><span data-stu-id="1a728-122"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="1a728-123">世紀的觀點。</span><span class="sxs-lookup"><span data-stu-id="1a728-123">Century view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a728-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a728-124">Return value</span></span>

<span data-ttu-id="1a728-125">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="1a728-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a728-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a728-126">Requirements</span></span>



| <span data-ttu-id="1a728-127">需求</span><span class="sxs-lookup"><span data-stu-id="1a728-127">Requirement</span></span> | <span data-ttu-id="1a728-128">值</span><span class="sxs-lookup"><span data-stu-id="1a728-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a728-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a728-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1a728-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a728-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a728-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a728-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1a728-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a728-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a728-133">標頭</span><span class="sxs-lookup"><span data-stu-id="1a728-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a728-134"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a728-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






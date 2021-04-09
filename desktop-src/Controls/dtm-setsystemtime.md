---
title: 'DTM_SETSYSTEMTIME 訊息 (Commctrl .h) '
description: 設定日期和時間選擇器 (DTP) 控制項的時間。 您可以明確地傳送此訊息，或使用 DateTime \_ SetSystemtime 宏。
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- DTM_SETSYSTEMTIME message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b2a3c625ad4ff02bed138a8086ca0da984de35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934848"
---
# <a name="dtm_setsystemtime-message"></a><span data-ttu-id="63132-105">DTM \_ SETSYSTEMTIME 訊息</span><span class="sxs-lookup"><span data-stu-id="63132-105">DTM\_SETSYSTEMTIME message</span></span>

<span data-ttu-id="63132-106">設定日期和時間選擇器 (DTP) 控制項的時間。</span><span class="sxs-lookup"><span data-stu-id="63132-106">Sets the time in a date and time picker (DTP) control.</span></span> <span data-ttu-id="63132-107">您可以明確地傳送此訊息，或使用 [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) 宏。</span><span class="sxs-lookup"><span data-stu-id="63132-107">You can send this message explicitly or use the [**DateTime\_SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="63132-108">參數</span><span class="sxs-lookup"><span data-stu-id="63132-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63132-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63132-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63132-110">值，指定應執行的動作。</span><span class="sxs-lookup"><span data-stu-id="63132-110">A value specifying the action that should be performed.</span></span> <span data-ttu-id="63132-111">此值必須設定為下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="63132-111">This value must be set to one of the following:</span></span>



| <span data-ttu-id="63132-112">值</span><span class="sxs-lookup"><span data-stu-id="63132-112">Value</span></span>                                                                                                                                             | <span data-ttu-id="63132-113">意義</span><span class="sxs-lookup"><span data-stu-id="63132-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <span data-ttu-id="63132-114"><dt>**GDT \_ 有效**</dt></span><span class="sxs-lookup"><span data-stu-id="63132-114"><dt>**GDT\_VALID**</dt></span></span> </dl> | <span data-ttu-id="63132-115">根據 *lParam* 指向的結構內的資料，設定 DTP 控制項。</span><span class="sxs-lookup"><span data-stu-id="63132-115">Set the DTP control according to the data within the structure that *lParam* points to.</span></span> <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <span data-ttu-id="63132-116"><dt>**GDT \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="63132-116"><dt>**GDT\_NONE**</dt></span></span> </dl>    | <span data-ttu-id="63132-117">將 [DTP] 控制項設定為 [無日期]，並清除其核取方塊。</span><span class="sxs-lookup"><span data-stu-id="63132-117">Set the DTP control to "no date" and clear its check box.</span></span> <span data-ttu-id="63132-118">當指定這個旗標時，會忽略 *lParam* 。</span><span class="sxs-lookup"><span data-stu-id="63132-118">When this flag is specified, *lParam* is ignored.</span></span> <span data-ttu-id="63132-119">此旗標只適用于設定為 [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) 樣式的 DTP 控制項。</span><span class="sxs-lookup"><span data-stu-id="63132-119">This flag applies only to DTP controls that are set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="63132-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63132-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63132-121">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的指標，其中包含用來設定 DTP 控制項的系統時間。</span><span class="sxs-lookup"><span data-stu-id="63132-121">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure containing the system time used to set the DTP control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63132-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="63132-122">Return value</span></span>

<span data-ttu-id="63132-123">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="63132-123">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="63132-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="63132-124">Requirements</span></span>



| <span data-ttu-id="63132-125">需求</span><span class="sxs-lookup"><span data-stu-id="63132-125">Requirement</span></span> | <span data-ttu-id="63132-126">值</span><span class="sxs-lookup"><span data-stu-id="63132-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63132-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63132-127">Minimum supported client</span></span><br/> | <span data-ttu-id="63132-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63132-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63132-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63132-129">Minimum supported server</span></span><br/> | <span data-ttu-id="63132-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63132-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63132-131">標頭</span><span class="sxs-lookup"><span data-stu-id="63132-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="63132-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="63132-132"><dt>Commctrl.h</dt></span></span> </dl> |



 


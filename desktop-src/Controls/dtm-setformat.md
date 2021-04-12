---
title: 'DTM_SETFORMAT 訊息 (Commctrl .h) '
description: 根據指定的格式字串，設定日期和時間選擇器的顯示 (DTP) 控制項。 您可以明確地傳送此訊息，或使用 DateTime \_ SetFormat 宏。
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- DTM_SETFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025297"
---
# <a name="dtm_setformat-message"></a><span data-ttu-id="87585-105">DTM \_ SETFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="87585-105">DTM\_SETFORMAT message</span></span>

<span data-ttu-id="87585-106">根據指定的格式字串，設定日期和時間選擇器的顯示 (DTP) 控制項。</span><span class="sxs-lookup"><span data-stu-id="87585-106">Sets the display of a date and time picker (DTP) control based on a given format string.</span></span> <span data-ttu-id="87585-107">您可以明確地傳送此訊息，或使用 [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) 宏。</span><span class="sxs-lookup"><span data-stu-id="87585-107">You can send this message explicitly or use the [**DateTime\_SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="87585-108">參數</span><span class="sxs-lookup"><span data-stu-id="87585-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87585-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87585-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="87585-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="87585-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="87585-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87585-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87585-112">以零結束的 [格式字串](date-and-time-picker-controls.md) 指標，可定義所需的顯示。</span><span class="sxs-lookup"><span data-stu-id="87585-112">A pointer to a zero-terminated [format string](date-and-time-picker-controls.md) that defines the desired display.</span></span> <span data-ttu-id="87585-113">將此參數設定為 **Null** ，會將控制項重設為目前樣式的預設格式字串。</span><span class="sxs-lookup"><span data-stu-id="87585-113">Setting this parameter to **NULL** will reset the control to the default format string for the current style.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87585-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="87585-114">Return value</span></span>

<span data-ttu-id="87585-115">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="87585-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="87585-116">備註</span><span class="sxs-lookup"><span data-stu-id="87585-116">Remarks</span></span>

<span data-ttu-id="87585-117">您可以在格式字串中包含額外的字元，以產生更豐富的顯示。</span><span class="sxs-lookup"><span data-stu-id="87585-117">It is acceptable to include extra characters within the format string to produce a more rich display.</span></span> <span data-ttu-id="87585-118">不過，任何非字元都必須括在單引號內。</span><span class="sxs-lookup"><span data-stu-id="87585-118">However, any nonformat characters must be enclosed within single quotes.</span></span> <span data-ttu-id="87585-119">例如，Today 格式字串 "' Today： ' hh '： '： ' ddddMMMdd '，' yyy" 會產生像是 "Today：04:22:31 星期二3月23日，1996" 的輸出。</span><span class="sxs-lookup"><span data-stu-id="87585-119">For example, the format string "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" would produce output like "Today is: 04:22:31 Tuesday Mar 23, 1996".</span></span>

> [!Note]  
> <span data-ttu-id="87585-120">當 DTP 控制項使用預設格式字串時，會追蹤地區設定的變更。</span><span class="sxs-lookup"><span data-stu-id="87585-120">A DTP control tracks locale changes when it is using the default format string.</span></span> <span data-ttu-id="87585-121">如果您設定自訂格式字串，將不會更新它以回應地區設定變更。</span><span class="sxs-lookup"><span data-stu-id="87585-121">If you set a custom format string, it will not be updated in response to locale changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="87585-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="87585-122">Requirements</span></span>



| <span data-ttu-id="87585-123">需求</span><span class="sxs-lookup"><span data-stu-id="87585-123">Requirement</span></span> | <span data-ttu-id="87585-124">值</span><span class="sxs-lookup"><span data-stu-id="87585-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87585-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87585-125">Minimum supported client</span></span><br/> | <span data-ttu-id="87585-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87585-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87585-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87585-127">Minimum supported server</span></span><br/> | <span data-ttu-id="87585-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87585-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87585-129">標頭</span><span class="sxs-lookup"><span data-stu-id="87585-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="87585-130"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="87585-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="87585-131">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="87585-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="87585-132">**DTM \_SETFORMATW** (Unicode) 和 **DTM \_ SETFORMATA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="87585-132">**DTM\_SETFORMATW** (Unicode) and **DTM\_SETFORMATA** (ANSI)</span></span><br/>               |



 

 






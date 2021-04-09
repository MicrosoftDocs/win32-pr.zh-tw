---
title: 'TTM_SETDELAYTIME 訊息 (Commctrl .h) '
description: 設定工具提示控制項的初始、彈出和 reshow 持續期間。
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- TTM_SETDELAYTIME message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934391"
---
# <a name="ttm_setdelaytime-message"></a><span data-ttu-id="7cc15-104">TTM \_ SETDELAYTIME 訊息</span><span class="sxs-lookup"><span data-stu-id="7cc15-104">TTM\_SETDELAYTIME message</span></span>

<span data-ttu-id="7cc15-105">設定工具提示控制項的初始、彈出和 reshow 持續期間。</span><span class="sxs-lookup"><span data-stu-id="7cc15-105">Sets the initial, pop-up, and reshow durations for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7cc15-106">參數</span><span class="sxs-lookup"><span data-stu-id="7cc15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cc15-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7cc15-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7cc15-108">指定要設定之時間值的旗標。</span><span class="sxs-lookup"><span data-stu-id="7cc15-108">Flag that specifies which time value to set.</span></span> <span data-ttu-id="7cc15-109">此參數可以是下列其中一個值</span><span class="sxs-lookup"><span data-stu-id="7cc15-109">This parameter can be one of the following values</span></span>



| <span data-ttu-id="7cc15-110">值</span><span class="sxs-lookup"><span data-stu-id="7cc15-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="7cc15-111">意義</span><span class="sxs-lookup"><span data-stu-id="7cc15-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="7cc15-112"><dt>**TTDT \_ AUTOPOP**</dt></span><span class="sxs-lookup"><span data-stu-id="7cc15-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl>       | <span data-ttu-id="7cc15-113">設定當指標在工具周框內為固定時，工具提示視窗保持可見的時間量。</span><span class="sxs-lookup"><span data-stu-id="7cc15-113">Set the amount of time a tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span> <span data-ttu-id="7cc15-114">若要將 autopop 延遲時間傳回為其預設值，請將 *lParam* 設定為-1。</span><span class="sxs-lookup"><span data-stu-id="7cc15-114">To return the autopop delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="7cc15-115"><dt>**TTDT \_ 初始**</dt></span><span class="sxs-lookup"><span data-stu-id="7cc15-115"><dt>**TTDT\_INITIAL**</dt></span></span> </dl>       | <span data-ttu-id="7cc15-116">設定在顯示工具提示視窗之前，指標必須保持在工具周框內保持靜止的時間量。</span><span class="sxs-lookup"><span data-stu-id="7cc15-116">Set the amount of time a pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span> <span data-ttu-id="7cc15-117">若要傳回初始延遲時間為其預設值，請將 *lParam* 設定為-1。</span><span class="sxs-lookup"><span data-stu-id="7cc15-117">To return the initial delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="7cc15-118"><dt>**TTDT \_ RESHOW**</dt></span><span class="sxs-lookup"><span data-stu-id="7cc15-118"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>          | <span data-ttu-id="7cc15-119">設定當指標從某個工具移至另一個工具時，後續工具提示視窗顯示所需的時間量。</span><span class="sxs-lookup"><span data-stu-id="7cc15-119">Set the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span> <span data-ttu-id="7cc15-120">若要將 reshow 延遲時間傳回為其預設值，請將 *lParam* 設定為-1。</span><span class="sxs-lookup"><span data-stu-id="7cc15-120">To return the reshow delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <span data-ttu-id="7cc15-121"><dt>**TTDT \_ 自動**</dt></span><span class="sxs-lookup"><span data-stu-id="7cc15-121"><dt>**TTDT\_AUTOMATIC**</dt></span></span> </dl> | <span data-ttu-id="7cc15-122">將三個延遲時間設定為預設比例。</span><span class="sxs-lookup"><span data-stu-id="7cc15-122">Set all three delay times to default proportions.</span></span> <span data-ttu-id="7cc15-123">Autopop 時間將會是初始時間的10倍，而 reshow 時間會是最初的第一次。</span><span class="sxs-lookup"><span data-stu-id="7cc15-123">The autopop time will be ten times the initial time and the reshow time will be one fifth the initial time.</span></span> <span data-ttu-id="7cc15-124">如果設定此旗標，請使用正值 *lParam* 來指定初始時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7cc15-124">If this flag is set, use a positive value of *lParam* to specify the initial time, in milliseconds.</span></span> <span data-ttu-id="7cc15-125">將 *lParam* 設定為負值，以將所有三個延遲時間傳回至其預設值。</span><span class="sxs-lookup"><span data-stu-id="7cc15-125">Set *lParam* to a negative value to return all three delay times to their default values.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7cc15-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7cc15-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7cc15-127">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定延遲時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7cc15-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the delay time, in milliseconds.</span></span> <span data-ttu-id="7cc15-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))必須為零。</span><span class="sxs-lookup"><span data-stu-id="7cc15-128">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cc15-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="7cc15-129">Return value</span></span>

<span data-ttu-id="7cc15-130">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="7cc15-130">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cc15-131">備註</span><span class="sxs-lookup"><span data-stu-id="7cc15-131">Remarks</span></span>

<span data-ttu-id="7cc15-132">預設的延遲時間是以按兩下時間為基礎。</span><span class="sxs-lookup"><span data-stu-id="7cc15-132">The default delay times are based on the double-click time.</span></span> <span data-ttu-id="7cc15-133">針對500毫秒的預設按兩下時間，初始、autopop 和 reshow 延遲時間分別為500毫秒、5000毫秒和100毫秒。</span><span class="sxs-lookup"><span data-stu-id="7cc15-133">For the default double-click time of 500 ms, the initial, autopop, and reshow delay times are 500ms, 5000ms, and 100ms respectively.</span></span> <span data-ttu-id="7cc15-134">下列程式碼片段會使用 [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) 函數來判斷任何系統的三個延遲時間。</span><span class="sxs-lookup"><span data-stu-id="7cc15-134">The following code fragment uses the [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) function to determine the three delay times for any system.</span></span>


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a><span data-ttu-id="7cc15-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cc15-135">Requirements</span></span>



| <span data-ttu-id="7cc15-136">需求</span><span class="sxs-lookup"><span data-stu-id="7cc15-136">Requirement</span></span> | <span data-ttu-id="7cc15-137">值</span><span class="sxs-lookup"><span data-stu-id="7cc15-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc15-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7cc15-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7cc15-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cc15-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7cc15-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7cc15-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7cc15-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7cc15-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7cc15-142">標頭</span><span class="sxs-lookup"><span data-stu-id="7cc15-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cc15-143"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7cc15-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cc15-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cc15-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cc15-145">**TTM \_ GETDELAYTIME**</span><span class="sxs-lookup"><span data-stu-id="7cc15-145">**TTM\_GETDELAYTIME**</span></span>](ttm-getdelaytime.md)
</dt> </dl>

 


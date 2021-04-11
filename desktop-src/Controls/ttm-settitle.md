---
title: 'TTM_SETTITLE 訊息 (Commctrl .h) '
description: 將標準圖示和標題字串新增至工具提示。
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- TTM_SETTITLE message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7972a9d40347995e9d641e7fc8706f9ad4c58bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844259"
---
# <a name="ttm_settitle-message"></a><span data-ttu-id="acb48-104">TTM \_ SETTITLE 訊息</span><span class="sxs-lookup"><span data-stu-id="acb48-104">TTM\_SETTITLE message</span></span>

<span data-ttu-id="acb48-105">將標準圖示和標題字串新增至工具提示。</span><span class="sxs-lookup"><span data-stu-id="acb48-105">Adds a standard icon and title string to a tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="acb48-106">參數</span><span class="sxs-lookup"><span data-stu-id="acb48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acb48-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="acb48-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acb48-108">將 *wParam* 設定為下列其中一個值，以指定要顯示的圖示。</span><span class="sxs-lookup"><span data-stu-id="acb48-108">Set *wParam* to one of the following values to specify the icon to be displayed.</span></span> <span data-ttu-id="acb48-109">從 Windows XP SP2 和更新版本，此參數也可以包含 **HICON** 值。</span><span class="sxs-lookup"><span data-stu-id="acb48-109">As of Windows XP SP2 and later, this parameter can also contain an **HICON** value.</span></span> <span data-ttu-id="acb48-110">任何大於 TTI 誤差的值 \_ 都假設為 **HICON**。</span><span class="sxs-lookup"><span data-stu-id="acb48-110">Any value greater than TTI\_ERROR is assumed to be an **HICON**.</span></span>



| <span data-ttu-id="acb48-111">值</span><span class="sxs-lookup"><span data-stu-id="acb48-111">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="acb48-112">意義</span><span class="sxs-lookup"><span data-stu-id="acb48-112">Meaning</span></span>                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <span data-ttu-id="acb48-113"><dt>**TTI \_ 無**</dt></span><span class="sxs-lookup"><span data-stu-id="acb48-113"><dt>**TTI\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="acb48-114">無圖示。</span><span class="sxs-lookup"><span data-stu-id="acb48-114">No icon.</span></span><br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <span data-ttu-id="acb48-115"><dt>**TTI \_ 資訊**</dt></span><span class="sxs-lookup"><span data-stu-id="acb48-115"><dt>**TTI\_INFO**</dt></span></span> </dl>                             | <span data-ttu-id="acb48-116">資訊圖示。</span><span class="sxs-lookup"><span data-stu-id="acb48-116">Info icon.</span></span><br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <span data-ttu-id="acb48-117"><dt>**TTI \_ 警告**</dt></span><span class="sxs-lookup"><span data-stu-id="acb48-117"><dt>**TTI\_WARNING**</dt></span></span> </dl>                    | <span data-ttu-id="acb48-118">警告圖示</span><span class="sxs-lookup"><span data-stu-id="acb48-118">Warning icon</span></span><br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <span data-ttu-id="acb48-119"><dt>**TTI \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="acb48-119"><dt>**TTI\_ERROR**</dt></span></span> </dl>                          | <span data-ttu-id="acb48-120">錯誤圖示</span><span class="sxs-lookup"><span data-stu-id="acb48-120">Error Icon</span></span><br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <span data-ttu-id="acb48-121"><dt>**TTI \_ 資訊 \_ 很大**</dt></span><span class="sxs-lookup"><span data-stu-id="acb48-121"><dt>**TTI\_INFO\_LARGE**</dt></span></span> </dl>          | <span data-ttu-id="acb48-122">大型錯誤圖示</span><span class="sxs-lookup"><span data-stu-id="acb48-122">Large error Icon</span></span><br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <span data-ttu-id="acb48-123"><dt>**TTI \_ 警告 \_ 很大**</dt></span><span class="sxs-lookup"><span data-stu-id="acb48-123"><dt>**TTI\_WARNING\_LARGE**</dt></span></span> </dl> | <span data-ttu-id="acb48-124">大型錯誤圖示</span><span class="sxs-lookup"><span data-stu-id="acb48-124">Large error Icon</span></span><br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <span data-ttu-id="acb48-125"><dt>**TTI \_ 錯誤 \_ 大**</dt></span><span class="sxs-lookup"><span data-stu-id="acb48-125"><dt>**TTI\_ERROR\_LARGE**</dt></span></span> </dl>       | <span data-ttu-id="acb48-126">大型錯誤圖示</span><span class="sxs-lookup"><span data-stu-id="acb48-126">Large error Icon</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="acb48-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acb48-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acb48-128">標題字串的指標。</span><span class="sxs-lookup"><span data-stu-id="acb48-128">Pointer to the title string.</span></span> <span data-ttu-id="acb48-129">您必須將值指派給 *lParam*。</span><span class="sxs-lookup"><span data-stu-id="acb48-129">You must assign a value to *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acb48-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="acb48-130">Return value</span></span>

<span data-ttu-id="acb48-131">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="acb48-131">Returns **TRUE** if successful, **FALSE** if not.</span></span>

## <a name="remarks"></a><span data-ttu-id="acb48-132">備註</span><span class="sxs-lookup"><span data-stu-id="acb48-132">Remarks</span></span>

<span data-ttu-id="acb48-133">工具提示的標題會出現在文字上方的不同字型中。</span><span class="sxs-lookup"><span data-stu-id="acb48-133">The title of a tooltip appears above the text, in a different font.</span></span> <span data-ttu-id="acb48-134">沒有標題就夠了。工具提示也必須有文字，否則就不會顯示。</span><span class="sxs-lookup"><span data-stu-id="acb48-134">It is not sufficient to have a title; the tooltip must have text as well, or it is not displayed.</span></span>

<span data-ttu-id="acb48-135">當 *wParam* 包含 **HICON** 時，[工具提示] 視窗會建立圖示的複本。</span><span class="sxs-lookup"><span data-stu-id="acb48-135">When *wParam* contains an **HICON**, a copy of the icon is created by the tooltip window.</span></span>

<span data-ttu-id="acb48-136">呼叫 **TTM \_ SETTITLE** 時， *lParam* 所指向的字串不得超過 100 **TCHARs** 的長度，包括終止的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="acb48-136">When calling **TTM\_SETTITLE**, the string pointed to by *lParam* must not exceed 100 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="acb48-137">範例</span><span class="sxs-lookup"><span data-stu-id="acb48-137">Examples</span></span>

<span data-ttu-id="acb48-138">下列範例顯示如何將標題和系統圖示新增至工具提示。</span><span class="sxs-lookup"><span data-stu-id="acb48-138">The following example shows how to add a title and a system icon to a tooltip.</span></span>


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a><span data-ttu-id="acb48-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="acb48-139">Requirements</span></span>



| <span data-ttu-id="acb48-140">需求</span><span class="sxs-lookup"><span data-stu-id="acb48-140">Requirement</span></span> | <span data-ttu-id="acb48-141">值</span><span class="sxs-lookup"><span data-stu-id="acb48-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="acb48-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="acb48-142">Minimum supported client</span></span><br/> | <span data-ttu-id="acb48-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acb48-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="acb48-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="acb48-144">Minimum supported server</span></span><br/> | <span data-ttu-id="acb48-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acb48-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="acb48-146">標頭</span><span class="sxs-lookup"><span data-stu-id="acb48-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="acb48-147"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="acb48-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="acb48-148">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="acb48-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="acb48-149">**TTM \_SETTITLEW** (Unicode) 和 **TTM \_ SETTITLEA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="acb48-149">**TTM\_SETTITLEW** (Unicode) and **TTM\_SETTITLEA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="acb48-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="acb48-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acb48-151">關於工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="acb48-151">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 






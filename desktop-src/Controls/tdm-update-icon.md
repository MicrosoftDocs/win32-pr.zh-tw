---
title: 'TDM_UPDATE_ICON 訊息 (Commctrl .h) '
description: 重新整理工作對話方塊的圖示。
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- TDM_UPDATE_ICON message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935092"
---
# <a name="tdm_update_icon-message"></a><span data-ttu-id="1cb52-104">TDM \_ 更新 \_ 圖示訊息</span><span class="sxs-lookup"><span data-stu-id="1cb52-104">TDM\_UPDATE\_ICON message</span></span>

<span data-ttu-id="1cb52-105">重新整理工作對話方塊的圖示。</span><span class="sxs-lookup"><span data-stu-id="1cb52-105">Refreshes the icon of a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="1cb52-106">參數</span><span class="sxs-lookup"><span data-stu-id="1cb52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cb52-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cb52-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cb52-108">表示要更新的圖示元素。</span><span class="sxs-lookup"><span data-stu-id="1cb52-108">Indicates which icon element to update.</span></span> <span data-ttu-id="1cb52-109">此參數必須是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="1cb52-109">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="1cb52-110">值</span><span class="sxs-lookup"><span data-stu-id="1cb52-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="1cb52-111">意義</span><span class="sxs-lookup"><span data-stu-id="1cb52-111">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <span data-ttu-id="1cb52-112"><dt>**TDIE \_ 圖示 \_ MAIN**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb52-112"><dt>**TDIE\_ICON\_MAIN**</dt></span></span> </dl>       | <span data-ttu-id="1cb52-113">主要圖示。</span><span class="sxs-lookup"><span data-stu-id="1cb52-113">Main icon.</span></span><br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <span data-ttu-id="1cb52-114"><dt>**TDIE \_ 圖示 \_ 頁尾**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb52-114"><dt>**TDIE\_ICON\_FOOTER**</dt></span></span> </dl> | <span data-ttu-id="1cb52-115">頁尾圖示。</span><span class="sxs-lookup"><span data-stu-id="1cb52-115">Footer icon.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1cb52-116">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1cb52-116">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cb52-117">字串的指標， (PCWSTR) 或 (HICON) 顯示的圖示控制碼。</span><span class="sxs-lookup"><span data-stu-id="1cb52-117">A pointer to a string (PCWSTR) or handle to an icon (HICON) to display.</span></span> <span data-ttu-id="1cb52-118">如果 *lParam* 為 **Null**，則不論 *wParam* 的值為何，都不會顯示任何圖示。</span><span class="sxs-lookup"><span data-stu-id="1cb52-118">If *lParam* is **NULL**, no icon is displayed, regardless of the value of *wParam*.</span></span>

<span data-ttu-id="1cb52-119">如果 *wParam* 的值為 TDIE \_ 圖示 \_ main，且 .tdf \_ USE \_ HICON \_ main 旗標是在用來建立工作對話方塊的 [**dwFlags**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)結構的 **TASKDIALOGCONFIG** 成員上設定，則 *lParam* 必須包含圖示的控制碼 (HICON) 才能顯示。</span><span class="sxs-lookup"><span data-stu-id="1cb52-119">If the value of *wParam* is TDIE\_ICON\_MAIN and the TDF\_USE\_HICON\_MAIN flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="1cb52-120">如果 *wParam* 的值是 TDIE \_ 圖示頁尾 \_ ，且 .tdf \_ USE HICON 頁尾旗標 \_ \_ 是在用來建立工作對話方塊的 [**dwFlags**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)結構的 **TASKDIALOGCONFIG** 成員上設定，則 *lParam* 必須包含圖示的控制碼 (HICON) 才能顯示。</span><span class="sxs-lookup"><span data-stu-id="1cb52-120">If the value of *wParam* is TDIE\_ICON\_FOOTER and the TDF\_USE\_HICON\_FOOTER flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="1cb52-121">如果 .TDF \_ use \_ HICON \_ MAIN 或 .tdf \_ use HICON 頁尾 \_ \_ 旗標 **未** 在 **dwFlags** 成員上設定，則 *lParam* 必須指向以 Null 終止的 Unicode 字串 (PCWSTR) ，其中包含透過 [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) 宏傳遞的有效資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1cb52-121">If the TDF\_USE\_HICON\_MAIN or TDF\_USE\_HICON\_FOOTER flags are **not** set on the **dwFlags** member, *lParam* must point to a null-terminated, Unicode string (PCWSTR) that contains a valid resource identifier passed through the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="1cb52-122">圖示會根據 *wParam* 的值顯示：如果值為 TDIE \_ 圖示 \_ MAIN，圖示就會顯示在標頭中; 如果值為 TDIE \_ 圖示頁尾 \_ ，圖示就會顯示在頁尾中。</span><span class="sxs-lookup"><span data-stu-id="1cb52-122">The icon is displayed based on the value of *wParam*: if the value is TDIE\_ICON\_MAIN, the icon is displayed in the header; if the value is TDIE\_ICON\_FOOTER, the icon is displayed in the footer.</span></span> <span data-ttu-id="1cb52-123">資源必須是來自應用程式的資源模組 (在 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)) 結構的 **hInstance** 成員中指定，或如果 **hInstance** 為 **Null**，則會從系統的資源模組 (imageres.dll) 。</span><span class="sxs-lookup"><span data-stu-id="1cb52-123">The resource must be either from the application's resource module (specified in the **hInstance** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure), or if **hInstance** is **NULL**, from the system's resource module (imageres.dll).</span></span> <span data-ttu-id="1cb52-124">若要識別系統資源，請使用透過 **MAKEINTRESOURCE** 宏傳遞的有效系統識別碼，或 commctrl 中的下列其中一個預先定義值：</span><span class="sxs-lookup"><span data-stu-id="1cb52-124">To identify a system resource, use a valid system identifier passed through the **MAKEINTRESOURCE** macro or one of the following predefined values from commctrl.h:</span></span>



| <span data-ttu-id="1cb52-125">值</span><span class="sxs-lookup"><span data-stu-id="1cb52-125">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="1cb52-126">意義</span><span class="sxs-lookup"><span data-stu-id="1cb52-126">Meaning</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <span data-ttu-id="1cb52-127"><dt>**TD \_ 錯誤 \_ 圖示**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb52-127"><dt>**TD\_ERROR\_ICON**</dt></span></span> </dl>                   | <span data-ttu-id="1cb52-128">停止符號圖示。</span><span class="sxs-lookup"><span data-stu-id="1cb52-128">A stop sign icon.</span></span><br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <span data-ttu-id="1cb52-129"><dt>**TD \_ 警告 \_ 圖示**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb52-129"><dt>**TD\_WARNING\_ICON**</dt></span></span> </dl>             | <span data-ttu-id="1cb52-130">驚嘆號圖示。</span><span class="sxs-lookup"><span data-stu-id="1cb52-130">An exclamation point icon.</span></span><br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <span data-ttu-id="1cb52-131"><dt>**TD \_ 資訊 \_ 圖示**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb52-131"><dt>**TD\_INFORMATION\_ICON**</dt></span></span> </dl> | <span data-ttu-id="1cb52-132">圓圈圖示中的小寫字母 "i"。</span><span class="sxs-lookup"><span data-stu-id="1cb52-132">A lowercase letter "i" in a circle icon.</span></span><br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <span data-ttu-id="1cb52-133"><dt>**TD \_ 防護 \_ 圖示**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb52-133"><dt>**TD\_SHIELD\_ICON**</dt></span></span> </dl>                | <span data-ttu-id="1cb52-134">安全性保護盾圖示。</span><span class="sxs-lookup"><span data-stu-id="1cb52-134">A security shield icon.</span></span><br/>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cb52-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cb52-135">Return value</span></span>

<span data-ttu-id="1cb52-136">傳回值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="1cb52-136">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cb52-137">備註</span><span class="sxs-lookup"><span data-stu-id="1cb52-137">Remarks</span></span>

<span data-ttu-id="1cb52-138">具有圖示的工作對話方塊配置可能會失敗，而且不會反映在傳回值中。</span><span class="sxs-lookup"><span data-stu-id="1cb52-138">The layout of the task dialog with the icon may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="1cb52-139">\_[確定] 的傳回值只會反映工作對話方塊收到的訊息，並嘗試進行處理。</span><span class="sxs-lookup"><span data-stu-id="1cb52-139">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="1cb52-140">如果工作對話方塊的配置失敗，對話方塊將會關閉，並且會在註冊的回呼函式傳回 **HRESULT** 程式碼。</span><span class="sxs-lookup"><span data-stu-id="1cb52-140">If the layout of the task dialog fails, the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="1cb52-141">如需回呼函數語法的詳細資訊，請參閱 [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)。</span><span class="sxs-lookup"><span data-stu-id="1cb52-141">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

<span data-ttu-id="1cb52-142">如果在沒有頁尾的情況下建立工作對話方塊 (也就是，用來建立工作對話方塊的 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) 結構的適當頁尾成員是 **Null**) 而且會傳送此訊息，不會將頁尾動態新增至工作對話方塊。</span><span class="sxs-lookup"><span data-stu-id="1cb52-142">If the task dialog is created without a footer (that is, the appropriate footer members of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog are **NULL**) and this message is sent, a footer is not dynamically added to the task dialog.</span></span> <span data-ttu-id="1cb52-143">當您在沒有標頭的情況下建立工作對話方塊時，傳送此訊息來更新標頭圖示也是如此。</span><span class="sxs-lookup"><span data-stu-id="1cb52-143">The same is true for sending this message to update a header icon when a task dialog is created without a header.</span></span> <span data-ttu-id="1cb52-144">若要在執行時間加入頁首或頁尾，請使用 [**TDM \_ 導覽 \_ 頁面**](tdm-navigate-page.md) 功能。</span><span class="sxs-lookup"><span data-stu-id="1cb52-144">To add a header or footer at run time, use the [**TDM\_NAVIGATE\_PAGE**](tdm-navigate-page.md) functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cb52-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cb52-145">Requirements</span></span>



| <span data-ttu-id="1cb52-146">需求</span><span class="sxs-lookup"><span data-stu-id="1cb52-146">Requirement</span></span> | <span data-ttu-id="1cb52-147">值</span><span class="sxs-lookup"><span data-stu-id="1cb52-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb52-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1cb52-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1cb52-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cb52-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1cb52-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1cb52-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1cb52-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cb52-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1cb52-152">標頭</span><span class="sxs-lookup"><span data-stu-id="1cb52-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cb52-153"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1cb52-153"><dt>Commctrl.h</dt></span></span> </dl> |



 


---
title: 'PSM_ADDPAGE 訊息 (Prsht.idl .h) '
description: 將新頁面加入現有屬性工作表的結尾。 您可以使用 PropSheet AddPage 宏明確地傳送此訊息 \_ 。
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- PSM_ADDPAGE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844031"
---
# <a name="psm_addpage-message"></a><span data-ttu-id="300a8-105">PSM \_ ADDPAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="300a8-105">PSM\_ADDPAGE message</span></span>

<span data-ttu-id="300a8-106">將新頁面加入現有屬性工作表的結尾。</span><span class="sxs-lookup"><span data-stu-id="300a8-106">Adds a new page to the end of an existing property sheet.</span></span> <span data-ttu-id="300a8-107">您可以使用 [**PropSheet \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="300a8-107">You can send this message explicitly or by using the [**PropSheet\_AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="300a8-108">參數</span><span class="sxs-lookup"><span data-stu-id="300a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="300a8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="300a8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="300a8-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="300a8-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="300a8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="300a8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="300a8-112">要加入之頁面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="300a8-112">Handle to the page to add.</span></span> <span data-ttu-id="300a8-113">頁面必須已由先前對 [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) 函式的呼叫所建立。</span><span class="sxs-lookup"><span data-stu-id="300a8-113">The page must have been created by a previous call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="300a8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="300a8-114">Return value</span></span>

<span data-ttu-id="300a8-115">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="300a8-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="300a8-116">備註</span><span class="sxs-lookup"><span data-stu-id="300a8-116">Remarks</span></span>

<span data-ttu-id="300a8-117">新頁面應該不會大於目前屬性工作表中最大的頁面，因為未調整內容工作表的大小以符合新頁面。</span><span class="sxs-lookup"><span data-stu-id="300a8-117">The new page should be no larger than the largest page currently in the property sheet because the property sheet is not resized to fit the new page.</span></span>

<span data-ttu-id="300a8-118">當屬性工作表正在動作頁面清單時，會發生一些訊息和一個函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="300a8-118">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="300a8-119">當此動作執行時，嘗試修改頁面清單將會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="300a8-119">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="300a8-120">因此，您不應該 \_ 在 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 的執行中或在處理下列通知和 Windows 訊息時使用 PSM ADDPAGE 訊息。</span><span class="sxs-lookup"><span data-stu-id="300a8-120">Accordingly, you should not use the PSM\_ADDPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="300a8-121">PSN \_ APPLY</span><span class="sxs-lookup"><span data-stu-id="300a8-121">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="300a8-122">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="300a8-122">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="300a8-123">PSN \_ 重設</span><span class="sxs-lookup"><span data-stu-id="300a8-123">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="300a8-124">PSN \_ ADVANCED.FIELD.SETACTIVE</span><span class="sxs-lookup"><span data-stu-id="300a8-124">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="300a8-125">**WM 損 \_ 毀**</span><span class="sxs-lookup"><span data-stu-id="300a8-125">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="300a8-126">**WM \_ INITDIALOG**</span><span class="sxs-lookup"><span data-stu-id="300a8-126">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="300a8-127">如果您在處理其中一個訊息時，或當 [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) 正在運作時需要修改屬性工作表頁面，請自行張貼私用 Windows 訊息。</span><span class="sxs-lookup"><span data-stu-id="300a8-127">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="300a8-128">在屬性工作表管理員完成其工作之前，您的應用程式將不會收到該訊息。</span><span class="sxs-lookup"><span data-stu-id="300a8-128">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="300a8-129">然後您可以修改頁面清單。</span><span class="sxs-lookup"><span data-stu-id="300a8-129">Then you can modify the list of pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="300a8-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="300a8-130">Requirements</span></span>



| <span data-ttu-id="300a8-131">需求</span><span class="sxs-lookup"><span data-stu-id="300a8-131">Requirement</span></span> | <span data-ttu-id="300a8-132">值</span><span class="sxs-lookup"><span data-stu-id="300a8-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="300a8-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="300a8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="300a8-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="300a8-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="300a8-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="300a8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="300a8-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="300a8-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="300a8-137">標頭</span><span class="sxs-lookup"><span data-stu-id="300a8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="300a8-138"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="300a8-138"><dt>Prsht.h</dt></span></span> </dl> |



 


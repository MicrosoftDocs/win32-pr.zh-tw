---
title: 'PSM_GETRESULT 訊息 (Prsht.idl .h) '
description: 由非強制回應屬性工作表用來取出 PropertySheet 傳回的強制回應屬性工作表資訊。 您可以明確地傳送此訊息，或使用 PropSheet \_ GetResult 宏。
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509076"
---
# <a name="psm_getresult-message"></a><span data-ttu-id="86108-105">PSM \_ GETRESULT 訊息</span><span class="sxs-lookup"><span data-stu-id="86108-105">PSM\_GETRESULT message</span></span>

<span data-ttu-id="86108-106">由非強制回應屬性工作表用來取出 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)傳回的強制回應屬性工作表資訊。</span><span class="sxs-lookup"><span data-stu-id="86108-106">Used by modeless property sheets to retrieve the information returned to modal property sheets by [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span></span> <span data-ttu-id="86108-107">您可以明確地傳送此訊息，或使用 [**PropSheet \_ GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) 宏。</span><span class="sxs-lookup"><span data-stu-id="86108-107">You can send this message explicitly or use the [**PropSheet\_GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="86108-108">參數</span><span class="sxs-lookup"><span data-stu-id="86108-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86108-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86108-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86108-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="86108-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="86108-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86108-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86108-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="86108-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86108-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="86108-113">Return value</span></span>

<span data-ttu-id="86108-114">如果成功，則傳回正值，否則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="86108-114">Returns a positive value if successful, or -1 otherwise.</span></span> <span data-ttu-id="86108-115">下列傳回值具有特殊意義。</span><span class="sxs-lookup"><span data-stu-id="86108-115">The following return values have a special meaning.</span></span>



| <span data-ttu-id="86108-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="86108-116">Return code</span></span>                                                                                         | <span data-ttu-id="86108-117">Description</span><span class="sxs-lookup"><span data-stu-id="86108-117">Description</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86108-118"><dt>**識別碼 \_ PSREBOOTSYSTEM**</dt></span><span class="sxs-lookup"><span data-stu-id="86108-118"><dt>**ID\_PSREBOOTSYSTEM**</dt></span></span> </dl>   | <span data-ttu-id="86108-119">頁面傳送了 [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) 訊息給屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="86108-119">A page sent a [**PSM\_REBOOTSYSTEM**](psm-rebootsystem.md) message to the property sheet.</span></span> <span data-ttu-id="86108-120">電腦必須重新開機，使用者的變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="86108-120">The computer must be restarted for the user's changes to take effect.</span></span><br/> |
| <dl> <span data-ttu-id="86108-121"><dt>**識別碼 \_ PSRESTARTWINDOWS**</dt></span><span class="sxs-lookup"><span data-stu-id="86108-121"><dt>**ID\_PSRESTARTWINDOWS**</dt></span></span> </dl> | <span data-ttu-id="86108-122">頁面傳送了 [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) 訊息給屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="86108-122">A page sent a [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) message to the property sheet.</span></span> <span data-ttu-id="86108-123">必須重新開機 Windows，使用者的變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="86108-123">Windows must be restarted for the user's changes to take effect.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="86108-124">備註</span><span class="sxs-lookup"><span data-stu-id="86108-124">Remarks</span></span>

<span data-ttu-id="86108-125">若要取出延伸的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="86108-125">To retrieve extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="86108-126">此訊息的傳回值與 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 針對模式屬性工作表傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="86108-126">The return value for this message is identical to what [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) returns for a modal property sheet.</span></span>

[<span data-ttu-id="86108-127">版本5.80。</span><span class="sxs-lookup"><span data-stu-id="86108-127">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="86108-128">[**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)傳回值會針對強制回應和非強制回應屬性工作表攜帶不同的資訊。</span><span class="sxs-lookup"><span data-stu-id="86108-128">The [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) return value carries different information for modal and modeless property sheets.</span></span> <span data-ttu-id="86108-129">在某些情況下，非強制回應屬性工作表可能需要從 **PropertySheet** 接收的資訊（如果已強制回應）。</span><span class="sxs-lookup"><span data-stu-id="86108-129">In some cases, modeless property sheets may need the information they would have received from **PropertySheet** if they had been modal.</span></span> <span data-ttu-id="86108-130">尤其是，他們可能需要知道識別碼 \_ PSREBOOTSYSTEM 或識別碼 PSRESTARTWINDOWS 是否 \_ 會傳回。</span><span class="sxs-lookup"><span data-stu-id="86108-130">In particular, they may need to know whether ID\_PSREBOOTSYSTEM or ID\_PSRESTARTWINDOWS would have been returned.</span></span>

<span data-ttu-id="86108-131">若為非強制回應屬性工作表，您的訊息迴圈應該使用 [**psm \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md) 將訊息傳遞至 [屬性工作表] 對話方塊，並使用 [ [**psm \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) ] 來判斷何時要終結對話方塊。</span><span class="sxs-lookup"><span data-stu-id="86108-131">For a modeless property sheet, your message loop should use [**PSM\_ISDIALOGMESSAGE**](psm-isdialogmessage.md) to pass messages to the property sheet dialog box, and [**PSM\_GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) to determine when to destroy the dialog box.</span></span> <span data-ttu-id="86108-132">當使用者按一下 [ **確定]** 或 [ **取消** ] 按鈕時， **PSM \_ GETCURRENTPAGEHWND** 會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="86108-132">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**.</span></span> <span data-ttu-id="86108-133">然後，您可以藉由傳送 **PSM \_ GETRESULT** 訊息來取得強制回應屬性工作表從 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)接收的值。</span><span class="sxs-lookup"><span data-stu-id="86108-133">You can then retrieve the value that a modal property sheet would have received from [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) by sending a **PSM\_GETRESULT** message.</span></span>

> [!Note]  
> <span data-ttu-id="86108-134">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="86108-134">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86108-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="86108-135">Requirements</span></span>



| <span data-ttu-id="86108-136">需求</span><span class="sxs-lookup"><span data-stu-id="86108-136">Requirement</span></span> | <span data-ttu-id="86108-137">值</span><span class="sxs-lookup"><span data-stu-id="86108-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="86108-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86108-138">Minimum supported client</span></span><br/> | <span data-ttu-id="86108-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86108-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="86108-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86108-140">Minimum supported server</span></span><br/> | <span data-ttu-id="86108-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86108-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="86108-142">標頭</span><span class="sxs-lookup"><span data-stu-id="86108-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="86108-143"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="86108-143"><dt>Prsht.h</dt></span></span> </dl> |



 


---
title: 'PSM_RESTARTWINDOWS 訊息 (Prsht.idl .h) '
description: 指出必須重新開機 Windows，變更才會生效。
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- PSM_RESTARTWINDOWS message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843424"
---
# <a name="psm_restartwindows-message"></a><span data-ttu-id="95a54-104">PSM \_ RESTARTWINDOWS 訊息</span><span class="sxs-lookup"><span data-stu-id="95a54-104">PSM\_RESTARTWINDOWS message</span></span>

<span data-ttu-id="95a54-105">指出必須重新開機 Windows，變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="95a54-105">Indicates that Windows needs to be restarted for the changes to take effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="95a54-106">參數</span><span class="sxs-lookup"><span data-stu-id="95a54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95a54-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95a54-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95a54-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="95a54-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="95a54-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95a54-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95a54-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="95a54-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95a54-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="95a54-111">Return value</span></span>

<span data-ttu-id="95a54-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="95a54-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95a54-113">備註</span><span class="sxs-lookup"><span data-stu-id="95a54-113">Remarks</span></span>

<span data-ttu-id="95a54-114">應用程式應該只傳送此訊息以回應 [PSN \_ APPLY](psn-apply.md) 或 [PSN \_ KILLACTIVE](psn-killactive.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="95a54-114">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span> <span data-ttu-id="95a54-115">您可以明確地傳送 **PSM \_ RESTARTWINDOWS** 訊息或使用 [**PropSheet \_ RESTARTWINDOWS**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) 宏。</span><span class="sxs-lookup"><span data-stu-id="95a54-115">You can send the **PSM\_RESTARTWINDOWS** message explicitly or by using the [**PropSheet\_RestartWindows**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) macro.</span></span>

<span data-ttu-id="95a54-116">此訊息會使 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式傳回 ID \_ PSRESTARTWINDOWS 值，但只有在使用者按一下 [ **確定]** 按鈕以關閉屬性工作表時才會傳回。</span><span class="sxs-lookup"><span data-stu-id="95a54-116">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSRESTARTWINDOWS value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="95a54-117">應用程式需要重新開機 Windows 的責任，您可以使用 [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) 函式來完成這項工作。</span><span class="sxs-lookup"><span data-stu-id="95a54-117">It is the application's responsibility to restart Windows, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

> [!Note]  
> <span data-ttu-id="95a54-118">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="95a54-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95a54-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="95a54-119">Requirements</span></span>



| <span data-ttu-id="95a54-120">需求</span><span class="sxs-lookup"><span data-stu-id="95a54-120">Requirement</span></span> | <span data-ttu-id="95a54-121">值</span><span class="sxs-lookup"><span data-stu-id="95a54-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95a54-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95a54-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95a54-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95a54-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="95a54-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95a54-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95a54-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95a54-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="95a54-126">標頭</span><span class="sxs-lookup"><span data-stu-id="95a54-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="95a54-127"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="95a54-127"><dt>Prsht.h</dt></span></span> </dl> |



 


---
title: 'PSM_REBOOTSYSTEM 訊息 (Prsht.idl .h) '
description: 指出需要重新開機系統，變更才會生效。 您可以 \_ 明確地傳送 PSM REBOOTSYSTEM 訊息或使用 PropSheet \_ REBOOTSYSTEM 宏。
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- PSM_REBOOTSYSTEM message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464869"
---
# <a name="psm_rebootsystem-message"></a><span data-ttu-id="934c2-105">PSM \_ REBOOTSYSTEM 訊息</span><span class="sxs-lookup"><span data-stu-id="934c2-105">PSM\_REBOOTSYSTEM message</span></span>

<span data-ttu-id="934c2-106">指出需要重新開機系統，變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="934c2-106">Indicates the system needs to be restarted for the changes to take effect.</span></span> <span data-ttu-id="934c2-107">您可以明確地傳送 **PSM \_ REBOOTSYSTEM** 訊息或使用 [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) 宏。</span><span class="sxs-lookup"><span data-stu-id="934c2-107">You can send the **PSM\_REBOOTSYSTEM** message explicitly or by using the [**PropSheet\_RebootSystem**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="934c2-108">參數</span><span class="sxs-lookup"><span data-stu-id="934c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="934c2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="934c2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="934c2-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="934c2-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="934c2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="934c2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="934c2-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="934c2-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="934c2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="934c2-113">Return value</span></span>

<span data-ttu-id="934c2-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="934c2-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="934c2-115">備註</span><span class="sxs-lookup"><span data-stu-id="934c2-115">Remarks</span></span>

<span data-ttu-id="934c2-116">應用程式應該只傳送此訊息以回應 [PSN \_ APPLY](psn-apply.md) 或 [PSN \_ KILLACTIVE](psn-killactive.md) 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="934c2-116">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification message.</span></span>

<span data-ttu-id="934c2-117">此訊息會使 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式傳回 ID \_ PSREBOOTSYSTEM 值，但只有在使用者按一下 [ **確定]** 按鈕以關閉屬性工作表時才會傳回。</span><span class="sxs-lookup"><span data-stu-id="934c2-117">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSREBOOTSYSTEM value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="934c2-118">應用程式必須負責重新開機系統，這可以使用 [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) 函數來完成。</span><span class="sxs-lookup"><span data-stu-id="934c2-118">It is the application's responsibility to reboot the system, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

<span data-ttu-id="934c2-119">這則訊息會取代之前或之後的所有 [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="934c2-119">This message supersedes all [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) messages that precede or follow it.</span></span>

> [!Note]  
> <span data-ttu-id="934c2-120">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="934c2-120">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="934c2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="934c2-121">Requirements</span></span>



| <span data-ttu-id="934c2-122">需求</span><span class="sxs-lookup"><span data-stu-id="934c2-122">Requirement</span></span> | <span data-ttu-id="934c2-123">值</span><span class="sxs-lookup"><span data-stu-id="934c2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="934c2-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="934c2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="934c2-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="934c2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="934c2-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="934c2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="934c2-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="934c2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="934c2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="934c2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="934c2-129"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="934c2-129"><dt>Prsht.h</dt></span></span> </dl> |



 


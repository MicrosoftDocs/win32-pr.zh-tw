---
title: 'PSM_APPLY 訊息 (Prsht.idl .h) '
description: 模擬 [套用] 按鈕的選取專案，表示一或多個頁面已變更，而且需要驗證和記錄變更。
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- PSM_APPLY message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844028"
---
# <a name="psm_apply-message"></a><span data-ttu-id="7d22d-104">PSM 套用 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="7d22d-104">PSM\_APPLY message</span></span>

<span data-ttu-id="7d22d-105">模擬 **[套用] 按鈕的** 選取專案，表示一或多個頁面已變更，而且需要驗證和記錄變更。</span><span class="sxs-lookup"><span data-stu-id="7d22d-105">Simulates the selection of the **Apply** button, indicating that one or more pages have changed and the changes need to be validated and recorded.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d22d-106">參數</span><span class="sxs-lookup"><span data-stu-id="7d22d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d22d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d22d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d22d-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7d22d-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7d22d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d22d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d22d-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7d22d-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d22d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d22d-111">Return value</span></span>

<span data-ttu-id="7d22d-112">如果所有頁面都成功套用變更，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7d22d-112">Returns **TRUE** if all pages successfully applied the changes, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d22d-113">備註</span><span class="sxs-lookup"><span data-stu-id="7d22d-113">Remarks</span></span>

<span data-ttu-id="7d22d-114">屬性工作表會將 [PSN \_ KILLACTIVE](psn-killactive.md) 通知程式碼傳送至目前的頁面。</span><span class="sxs-lookup"><span data-stu-id="7d22d-114">The property sheet sends the [PSN\_KILLACTIVE](psn-killactive.md) notification code to the current page.</span></span> <span data-ttu-id="7d22d-115">如果目前的頁面傳回 **FALSE**，則屬性工作表會將 [PSN \_](psn-apply.md) 套用通知程式碼至所有使用中頁面。</span><span class="sxs-lookup"><span data-stu-id="7d22d-115">If the current page returns **FALSE**, the property sheet sends the [PSN\_APPLY](psn-apply.md) notification code to all active pages.</span></span> <span data-ttu-id="7d22d-116">您可以 \_ 使用 [**PropSheet \_ apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) 宏明確地傳送 PSM 套用訊息。</span><span class="sxs-lookup"><span data-stu-id="7d22d-116">You can send the PSM\_APPLY message explicitly or by using the [**PropSheet\_Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) macro.</span></span>

> [!Note]  
> <span data-ttu-id="7d22d-117">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="7d22d-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7d22d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d22d-118">Requirements</span></span>



| <span data-ttu-id="7d22d-119">需求</span><span class="sxs-lookup"><span data-stu-id="7d22d-119">Requirement</span></span> | <span data-ttu-id="7d22d-120">值</span><span class="sxs-lookup"><span data-stu-id="7d22d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d22d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d22d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7d22d-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d22d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7d22d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d22d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7d22d-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d22d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7d22d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7d22d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d22d-126"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d22d-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 






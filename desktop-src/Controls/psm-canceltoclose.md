---
title: 'PSM_CANCELTOCLOSE 訊息 (Prsht.idl .h) '
description: 當應用程式在最近的 PSN 套用無法取消的通知之後，由應用程式傳送 \_ 。 您可以使用 PropSheet CancelToClose 宏明確地傳送此訊息 \_ 。
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- PSM_CANCELTOCLOSE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105276"
---
# <a name="psm_canceltoclose-message"></a><span data-ttu-id="3ca30-105">PSM \_ CANCELTOCLOSE 訊息</span><span class="sxs-lookup"><span data-stu-id="3ca30-105">PSM\_CANCELTOCLOSE message</span></span>

<span data-ttu-id="3ca30-106">當應用程式在最近的 PSN 套用無法取消的通知之後 [， \_ ](psn-apply.md) 由應用程式傳送。</span><span class="sxs-lookup"><span data-stu-id="3ca30-106">Sent by an application when it has performed changes since the most recent [PSN\_APPLY](psn-apply.md) notification that cannot be canceled.</span></span> <span data-ttu-id="3ca30-107">您可以使用 [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3ca30-107">You can send this message explicitly or by using the [**PropSheet\_CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ca30-108">參數</span><span class="sxs-lookup"><span data-stu-id="3ca30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ca30-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ca30-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ca30-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3ca30-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3ca30-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ca30-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3ca30-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3ca30-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ca30-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ca30-113">Return value</span></span>

<span data-ttu-id="3ca30-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="3ca30-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca30-115">備註</span><span class="sxs-lookup"><span data-stu-id="3ca30-115">Remarks</span></span>

<span data-ttu-id="3ca30-116">**PSM \_CANCELTOCLOSE** 會停用 [ **取消** ] 按鈕，並將 [ **確定]** 按鈕的文字變更為 [關閉]。</span><span class="sxs-lookup"><span data-stu-id="3ca30-116">**PSM\_CANCELTOCLOSE** disables the **Cancel** button and changes the text of the **OK** button to "Close".</span></span>

<span data-ttu-id="3ca30-117">大部分的屬性工作表等候執行無法復原的變更，直到收到 PSN 套用 \_ 通知為止。</span><span class="sxs-lookup"><span data-stu-id="3ca30-117">Most property sheets wait to perform irreversible changes until a PSN\_APPLY notification is received.</span></span> <span data-ttu-id="3ca30-118">不過，在某些情況下，屬性工作表可能會在標準 PSN 套用 \_ /PSN 重設順序之外進行無法復原的變更 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3ca30-118">However, in some circumstances, a property sheet may make irreversible changes outside the standard PSN\_APPLY/PSN\_RESET sequence.</span></span> <span data-ttu-id="3ca30-119">其中一個範例是包含 [ **編輯** ] 按鈕的屬性工作表，可用來顯示編輯屬性的 subdialog 方塊。</span><span class="sxs-lookup"><span data-stu-id="3ca30-119">One example is a property sheet that contains an **Edit** button that is used to display a subdialog box for editing a property.</span></span> <span data-ttu-id="3ca30-120">當使用者按一下 **[確定]** 提交變更時，[屬性工作表] 頁面會有數個選項。</span><span class="sxs-lookup"><span data-stu-id="3ca30-120">When the user clicks **OK** to submit the change, the property sheet page has several options.</span></span>

-   <span data-ttu-id="3ca30-121">它可以記錄變更，但要等到收到 PSN 套用 \_ 通知才能套用變更。</span><span class="sxs-lookup"><span data-stu-id="3ca30-121">It can record the changes, but wait until it receives a PSN\_APPLY notification to apply them.</span></span> <span data-ttu-id="3ca30-122">這是慣用的方法。</span><span class="sxs-lookup"><span data-stu-id="3ca30-122">This is the preferred approach.</span></span>
-   <span data-ttu-id="3ca30-123">它可以在離開 subdialog box 之後立即套用變更，但請記住原始設定。</span><span class="sxs-lookup"><span data-stu-id="3ca30-123">It can apply the changes immediately after exiting the subdialog box, but remember the original settings.</span></span> <span data-ttu-id="3ca30-124">如果 \_ 收到 PSN 重設通知，這些設定可以用來還原原始狀態。</span><span class="sxs-lookup"><span data-stu-id="3ca30-124">Those settings can be used to restore the original state if a PSN\_RESET notification is received.</span></span>
-   <span data-ttu-id="3ca30-125">它可以立即套用變更，而不會在收到 [PSN \_ 重設](psn-reset.md) 通知時嘗試還原原始設定。</span><span class="sxs-lookup"><span data-stu-id="3ca30-125">It can apply the changes immediately and not attempt to restore the original settings when it receives a [PSN\_RESET](psn-reset.md) notification.</span></span> <span data-ttu-id="3ca30-126">不建議使用此方法，但如果變更太遠而無法達成其他兩個選項，則可能是必要的。</span><span class="sxs-lookup"><span data-stu-id="3ca30-126">This approach is not recommended, but may be necessary if the changes are too far-reaching for the other two options to be practical.</span></span>

<span data-ttu-id="3ca30-127">針對第三個選項，應用程式應該將 **PSM \_ CANCELTOCLOSE** 訊息傳送至屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="3ca30-127">For the third option, applications should send a **PSM\_CANCELTOCLOSE** message to the property sheet.</span></span> <span data-ttu-id="3ca30-128">這會向使用者指出，藉由按一下 [ **取消** ] 按鈕，就無法反轉使用 [subdialog] 方塊進行的變更。</span><span class="sxs-lookup"><span data-stu-id="3ca30-128">It indicates to the user that the changes made with the subdialog box cannot be reversed by clicking the **Cancel** button.</span></span>

> [!Note]  
> <span data-ttu-id="3ca30-129">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="3ca30-129">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3ca30-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ca30-130">Requirements</span></span>



| <span data-ttu-id="3ca30-131">需求</span><span class="sxs-lookup"><span data-stu-id="3ca30-131">Requirement</span></span> | <span data-ttu-id="3ca30-132">值</span><span class="sxs-lookup"><span data-stu-id="3ca30-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca30-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ca30-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca30-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ca30-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3ca30-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ca30-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca30-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ca30-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3ca30-137">標頭</span><span class="sxs-lookup"><span data-stu-id="3ca30-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ca30-138"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ca30-138"><dt>Prsht.h</dt></span></span> </dl> |



 

 






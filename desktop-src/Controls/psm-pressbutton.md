---
title: 'PSM_PRESSBUTTON 訊息 (Prsht.idl .h) '
description: 模擬屬性工作表按鈕的選取專案。 您可以使用 PropSheet PressButton 宏明確地傳送此訊息 \_ 。
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- PSM_PRESSBUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467104"
---
# <a name="psm_pressbutton-message"></a><span data-ttu-id="6ecb3-105">PSM \_ PRESSBUTTON 訊息</span><span class="sxs-lookup"><span data-stu-id="6ecb3-105">PSM\_PRESSBUTTON message</span></span>

<span data-ttu-id="6ecb3-106">模擬屬性工作表按鈕的選取專案。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-106">Simulates the selection of a property sheet button.</span></span> <span data-ttu-id="6ecb3-107">您可以使用 [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-107">You can send this message explicitly or by using the [**PropSheet\_PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ecb3-108">參數</span><span class="sxs-lookup"><span data-stu-id="6ecb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ecb3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ecb3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ecb3-110">要選取之按鈕的索引。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-110">Index of the button to select.</span></span> <span data-ttu-id="6ecb3-111">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="6ecb3-112">值</span><span class="sxs-lookup"><span data-stu-id="6ecb3-112">Value</span></span>                                                                                                                                                            | <span data-ttu-id="6ecb3-113">意義</span><span class="sxs-lookup"><span data-stu-id="6ecb3-113">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <span data-ttu-id="6ecb3-114"><dt>**PSBTN \_ APPLYNOW**</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb3-114"><dt>**PSBTN\_APPLYNOW**</dt></span></span> </dl> | <span data-ttu-id="6ecb3-115">選取 [ **套用** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-115">Selects the **Apply** button.</span></span> <span data-ttu-id="6ecb3-116">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，此值無效。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-116">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <span data-ttu-id="6ecb3-117"><dt>**PSBTN \_ 回來**</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb3-117"><dt>**PSBTN\_BACK**</dt></span></span> </dl>             | <span data-ttu-id="6ecb3-118">選取 [ **上一步** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-118">Selects the **Back** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <span data-ttu-id="6ecb3-119"><dt>**PSBTN \_ 取消**</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb3-119"><dt>**PSBTN\_CANCEL**</dt></span></span> </dl>       | <span data-ttu-id="6ecb3-120">選取 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-120">Selects the **Cancel** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <span data-ttu-id="6ecb3-121"><dt>**PSBTN \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb3-121"><dt>**PSBTN\_FINISH**</dt></span></span> </dl>       | <span data-ttu-id="6ecb3-122">選取 [ **完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-122">Selects the **Finish** button.</span></span><br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <span data-ttu-id="6ecb3-123"><dt>**PSBTN \_ 說明**</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb3-123"><dt>**PSBTN\_HELP**</dt></span></span> </dl>             | <span data-ttu-id="6ecb3-124">選取 [ **說明** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-124">Selects the **Help** button.</span></span> <span data-ttu-id="6ecb3-125">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，此值無效。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-125">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <span data-ttu-id="6ecb3-126"><dt>**PSBTN \_ 下一步**</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb3-126"><dt>**PSBTN\_NEXT**</dt></span></span> </dl>             | <span data-ttu-id="6ecb3-127">選取 [ **下一步]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-127">Selects the **Next** button.</span></span><br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <span data-ttu-id="6ecb3-128"><dt>**PSBTN \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb3-128"><dt>**PSBTN\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="6ecb3-129">選取 [ **確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-129">Selects the **OK** button.</span></span> <span data-ttu-id="6ecb3-130">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，此值無效。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-130">This value is not valid when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="6ecb3-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ecb3-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ecb3-132">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-132">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ecb3-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ecb3-133">Return value</span></span>

<span data-ttu-id="6ecb3-134">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6ecb3-134">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ecb3-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ecb3-135">Requirements</span></span>



| <span data-ttu-id="6ecb3-136">需求</span><span class="sxs-lookup"><span data-stu-id="6ecb3-136">Requirement</span></span> | <span data-ttu-id="6ecb3-137">值</span><span class="sxs-lookup"><span data-stu-id="6ecb3-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ecb3-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ecb3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6ecb3-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ecb3-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6ecb3-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ecb3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6ecb3-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ecb3-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ecb3-142">標頭</span><span class="sxs-lookup"><span data-stu-id="6ecb3-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ecb3-143"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ecb3-143"><dt>Prsht.h</dt></span></span> </dl> |



 

 






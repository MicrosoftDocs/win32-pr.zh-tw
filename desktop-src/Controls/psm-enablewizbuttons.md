---
title: 'PSM_ENABLEWIZBUTTONS 訊息 (Prsht.idl .h) '
description: 啟用或停用 Aero wizard 中的任何標準按鈕。 您可以明確地傳送此訊息，或使用 PropSheet \_ EnableWizButtons 宏。
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- PSM_ENABLEWIZBUTTONS message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934626"
---
# <a name="psm_enablewizbuttons-message"></a><span data-ttu-id="11f80-105">PSM \_ ENABLEWIZBUTTONS 訊息</span><span class="sxs-lookup"><span data-stu-id="11f80-105">PSM\_ENABLEWIZBUTTONS message</span></span>

<span data-ttu-id="11f80-106">啟用或停用 Aero wizard 中的任何標準按鈕。</span><span class="sxs-lookup"><span data-stu-id="11f80-106">Enables or disables any of the standard buttons in an Aero wizard.</span></span> <span data-ttu-id="11f80-107">您可以明確地傳送此訊息，或使用 [**PropSheet \_ EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) 宏。</span><span class="sxs-lookup"><span data-stu-id="11f80-107">You can send this message explicitly or use the [**PropSheet\_EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="11f80-108">參數</span><span class="sxs-lookup"><span data-stu-id="11f80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11f80-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11f80-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11f80-110">下列其中一個或多個值，可指定要啟用的屬性工作表按鈕。</span><span class="sxs-lookup"><span data-stu-id="11f80-110">One or more of the following values that specify which property sheet buttons are to be enabled.</span></span> <span data-ttu-id="11f80-111">如果這個參數和 *lParam* 中包含一個按鈕值，就會啟用它。</span><span class="sxs-lookup"><span data-stu-id="11f80-111">If a button value is included in both this parameter and *lParam*, it is enabled.</span></span>



| <span data-ttu-id="11f80-112">值</span><span class="sxs-lookup"><span data-stu-id="11f80-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="11f80-113">意義</span><span class="sxs-lookup"><span data-stu-id="11f80-113">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="11f80-114"><dt>**PSWIZB \_ 回來**</dt></span><span class="sxs-lookup"><span data-stu-id="11f80-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="11f80-115">[ **上一頁** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="11f80-115">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="11f80-116"><dt>**PSWIZB \_ 取消**</dt></span><span class="sxs-lookup"><span data-stu-id="11f80-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="11f80-117">[ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="11f80-117">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="11f80-118"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="11f80-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="11f80-119">[ **完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="11f80-119">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="11f80-120"><dt>**PSWIZB \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="11f80-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="11f80-121">[ **完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="11f80-121">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="11f80-122"><dt>**PSWIZB \_ 下一步**</dt></span><span class="sxs-lookup"><span data-stu-id="11f80-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="11f80-123">[ **下一步]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="11f80-123">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="11f80-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11f80-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11f80-125">*WParam* 中使用的一或多個相同值，指定受此呼叫影響的按鈕。</span><span class="sxs-lookup"><span data-stu-id="11f80-125">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="11f80-126">如果按鈕值出現在此參數中，但未出現在 *wParam* 中，則表示該按鈕應停用。</span><span class="sxs-lookup"><span data-stu-id="11f80-126">If a button value appears in this parameter but not in *wParam*, it indicates that the button should be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11f80-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="11f80-127">Return value</span></span>

<span data-ttu-id="11f80-128">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="11f80-128">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="11f80-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="11f80-129">Requirements</span></span>



| <span data-ttu-id="11f80-130">需求</span><span class="sxs-lookup"><span data-stu-id="11f80-130">Requirement</span></span> | <span data-ttu-id="11f80-131">值</span><span class="sxs-lookup"><span data-stu-id="11f80-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11f80-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11f80-132">Minimum supported client</span></span><br/> | <span data-ttu-id="11f80-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11f80-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="11f80-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11f80-134">Minimum supported server</span></span><br/> | <span data-ttu-id="11f80-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11f80-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="11f80-136">標頭</span><span class="sxs-lookup"><span data-stu-id="11f80-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="11f80-137"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="11f80-137"><dt>Prsht.h</dt></span></span> </dl> |



 

 






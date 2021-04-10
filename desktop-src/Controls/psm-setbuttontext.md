---
title: 'PSM_SETBUTTONTEXT 訊息 (Prsht.idl .h) '
description: 設定 Aero wizard 中按鈕的文字。 您可以使用 PropSheet SetButtonText 宏明確地傳送此訊息 \_ 。
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- PSM_SETBUTTONTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024988"
---
# <a name="psm_setbuttontext-message"></a><span data-ttu-id="ee4e2-105">PSM \_ SETBUTTONTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="ee4e2-105">PSM\_SETBUTTONTEXT message</span></span>

<span data-ttu-id="ee4e2-106">設定 Aero wizard 中按鈕的文字。</span><span class="sxs-lookup"><span data-stu-id="ee4e2-106">Sets the text on a button in an Aero wizard.</span></span> <span data-ttu-id="ee4e2-107">您可以使用 [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ee4e2-107">You can send this message explicitly or by using the [**PropSheet\_SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee4e2-108">參數</span><span class="sxs-lookup"><span data-stu-id="ee4e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee4e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee4e2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee4e2-110">下列其中一個值，指定要設定其文字的按鈕。</span><span class="sxs-lookup"><span data-stu-id="ee4e2-110">One of the following values specifying the button whose text is set.</span></span>



| <span data-ttu-id="ee4e2-111">值</span><span class="sxs-lookup"><span data-stu-id="ee4e2-111">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="ee4e2-112">意義</span><span class="sxs-lookup"><span data-stu-id="ee4e2-112">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="ee4e2-113"><dt>**PSWIZB \_ 回來**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4e2-113"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="ee4e2-114">[ **上一頁** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ee4e2-114">The **Back** button.</span></span><br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="ee4e2-115"><dt>**PSWIZB \_ 取消**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4e2-115"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="ee4e2-116">[ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ee4e2-116">The **Cancel** button.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="ee4e2-117"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4e2-117"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="ee4e2-118">[ **完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ee4e2-118">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="ee4e2-119"><dt>**PSWIZB \_ 完成**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4e2-119"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="ee4e2-120">[ **完成]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ee4e2-120">The **Finish** button.</span></span><br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="ee4e2-121"><dt>**PSWIZB \_ 下一步**</dt></span><span class="sxs-lookup"><span data-stu-id="ee4e2-121"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="ee4e2-122">[ **下一步]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ee4e2-122">The **Next** button.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ee4e2-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee4e2-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee4e2-124">要設定的文字。</span><span class="sxs-lookup"><span data-stu-id="ee4e2-124">The text to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee4e2-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee4e2-125">Return value</span></span>

<span data-ttu-id="ee4e2-126">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="ee4e2-126">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee4e2-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee4e2-127">Requirements</span></span>



| <span data-ttu-id="ee4e2-128">需求</span><span class="sxs-lookup"><span data-stu-id="ee4e2-128">Requirement</span></span> | <span data-ttu-id="ee4e2-129">值</span><span class="sxs-lookup"><span data-stu-id="ee4e2-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4e2-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee4e2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4e2-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee4e2-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ee4e2-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee4e2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4e2-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee4e2-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ee4e2-134">標頭</span><span class="sxs-lookup"><span data-stu-id="ee4e2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee4e2-135"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4e2-135"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="ee4e2-136">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="ee4e2-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ee4e2-137">**PSM \_SETBUTTONTEXTW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="ee4e2-137">**PSM\_SETBUTTONTEXTW** (Unicode)</span></span><br/>                                       |



 

 






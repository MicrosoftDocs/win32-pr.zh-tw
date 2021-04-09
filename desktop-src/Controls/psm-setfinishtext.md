---
title: 'PSM_SETFINISHTEXT 訊息 (Prsht.idl .h) '
description: 設定 wizard 中 [完成] 按鈕的文字、顯示並啟用按鈕，以及隱藏 [下一步] 和 [上一頁] 按鈕。 您可以使用 PropSheet SetFinishText 宏明確地傳送此訊息 \_ 。
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- PSM_SETFINISHTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685557"
---
# <a name="psm_setfinishtext-message"></a><span data-ttu-id="b444f-105">PSM \_ SETFINISHTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="b444f-105">PSM\_SETFINISHTEXT message</span></span>

<span data-ttu-id="b444f-106">設定 wizard 中 [ **完成]** 按鈕的文字、顯示並啟用按鈕，以及隱藏 [ **下一步]** 和 [ **上一頁** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="b444f-106">Sets the text of the **Finish** button in a wizard, shows and enables the button, and hides the **Next** and **Back** buttons.</span></span> <span data-ttu-id="b444f-107">您可以使用 [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b444f-107">You can send this message explicitly or by using the [**PropSheet\_SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b444f-108">參數</span><span class="sxs-lookup"><span data-stu-id="b444f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b444f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b444f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b444f-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b444f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b444f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b444f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b444f-112">[ **完成]** 按鈕的新文字指標。</span><span class="sxs-lookup"><span data-stu-id="b444f-112">Pointer to the new text for the **Finish** button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b444f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b444f-113">Return value</span></span>

<span data-ttu-id="b444f-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b444f-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b444f-115">備註</span><span class="sxs-lookup"><span data-stu-id="b444f-115">Remarks</span></span>

<span data-ttu-id="b444f-116">依預設，[ **完成]** 按鈕沒有鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="b444f-116">By default, the **Finish** button does not have a keyboard accelerator.</span></span> <span data-ttu-id="b444f-117">您可以使用此訊息建立鍵盤快速鍵，方法是在您指派給 *lParam* 的文字字串中包含連字號 (&) 。</span><span class="sxs-lookup"><span data-stu-id="b444f-117">You can create a keyboard accelerator with this message by including an ampersand (&) in the text string that you assign to *lParam*.</span></span> <span data-ttu-id="b444f-118">例如，「&完成」會將 F 定義為快速鍵。</span><span class="sxs-lookup"><span data-stu-id="b444f-118">For example, "&Finish" defines F as the accelerator key.</span></span>

## <a name="requirements"></a><span data-ttu-id="b444f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b444f-119">Requirements</span></span>



| <span data-ttu-id="b444f-120">需求</span><span class="sxs-lookup"><span data-stu-id="b444f-120">Requirement</span></span> | <span data-ttu-id="b444f-121">值</span><span class="sxs-lookup"><span data-stu-id="b444f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b444f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b444f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b444f-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b444f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b444f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b444f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b444f-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b444f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b444f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b444f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b444f-127"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b444f-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="b444f-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b444f-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b444f-129">**PSM \_SETFINISHTEXTW** (Unicode) 和 **PSM \_ SETFINISHTEXTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="b444f-129">**PSM\_SETFINISHTEXTW** (Unicode) and **PSM\_SETFINISHTEXTA** (ANSI)</span></span><br/>    |



 

 






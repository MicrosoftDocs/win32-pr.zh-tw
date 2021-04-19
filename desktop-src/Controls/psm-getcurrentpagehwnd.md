---
title: 'PSM_GETCURRENTPAGEHWND 訊息 (Prsht.idl .h) '
description: 抓取屬性工作表目前頁面的視窗控制碼。 您可以使用 PropSheet GetCurrentPageHwnd 宏明確地傳送此訊息 \_ 。
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- PSM_GETCURRENTPAGEHWND message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965926"
---
# <a name="psm_getcurrentpagehwnd-message"></a><span data-ttu-id="86150-105">PSM \_ GETCURRENTPAGEHWND 訊息</span><span class="sxs-lookup"><span data-stu-id="86150-105">PSM\_GETCURRENTPAGEHWND message</span></span>

<span data-ttu-id="86150-106">抓取屬性工作表目前頁面的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="86150-106">Retrieves a handle to the window of the current page of a property sheet.</span></span> <span data-ttu-id="86150-107">您可以使用 [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="86150-107">You can send this message explicitly or by using the [**PropSheet\_GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="86150-108">參數</span><span class="sxs-lookup"><span data-stu-id="86150-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86150-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86150-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86150-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="86150-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="86150-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86150-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86150-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="86150-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86150-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="86150-113">Return value</span></span>

<span data-ttu-id="86150-114">傳回目前屬性工作表頁面的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="86150-114">Returns a handle to the window of the current property sheet page.</span></span>

## <a name="remarks"></a><span data-ttu-id="86150-115">備註</span><span class="sxs-lookup"><span data-stu-id="86150-115">Remarks</span></span>

<span data-ttu-id="86150-116">使用具有非強制回應屬性工作表的 **PSM \_ GETCURRENTPAGEHWND** 訊息，以判斷何時要終結對話方塊。</span><span class="sxs-lookup"><span data-stu-id="86150-116">Use the **PSM\_GETCURRENTPAGEHWND** message with modeless property sheets to determine when to destroy the dialog box.</span></span> <span data-ttu-id="86150-117">當使用者按一下 [ **確定]** 或 [ **取消** ] 按鈕時， **PSM \_ GETCURRENTPAGEHWND** 會傳回 **Null**，然後您可以使用 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 函數來終結對話方塊。</span><span class="sxs-lookup"><span data-stu-id="86150-117">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**, and you can then use the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy the dialog box.</span></span>

> [!Note]  
> <span data-ttu-id="86150-118">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="86150-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86150-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="86150-119">Requirements</span></span>



| <span data-ttu-id="86150-120">需求</span><span class="sxs-lookup"><span data-stu-id="86150-120">Requirement</span></span> | <span data-ttu-id="86150-121">值</span><span class="sxs-lookup"><span data-stu-id="86150-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="86150-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86150-122">Minimum supported client</span></span><br/> | <span data-ttu-id="86150-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86150-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="86150-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86150-124">Minimum supported server</span></span><br/> | <span data-ttu-id="86150-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86150-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="86150-126">標頭</span><span class="sxs-lookup"><span data-stu-id="86150-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="86150-127"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="86150-127"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86150-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86150-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86150-129">**PropertySheet**</span><span class="sxs-lookup"><span data-stu-id="86150-129">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 


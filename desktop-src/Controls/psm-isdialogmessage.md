---
title: 'PSM_ISDIALOGMESSAGE 訊息 (Prsht.idl .h) '
description: 將訊息傳遞至屬性工作表對話方塊，並指出對話方塊是否已處理訊息。 您可以使用 PropSheet IsDialogMessage 宏明確地傳送此訊息 \_ 。
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- PSM_ISDIALOGMESSAGE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843660"
---
# <a name="psm_isdialogmessage-message"></a><span data-ttu-id="4dc03-105">PSM \_ ISDIALOGMESSAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="4dc03-105">PSM\_ISDIALOGMESSAGE message</span></span>

<span data-ttu-id="4dc03-106">將訊息傳遞至屬性工作表對話方塊，並指出對話方塊是否已處理訊息。</span><span class="sxs-lookup"><span data-stu-id="4dc03-106">Passes a message to a property sheet dialog box and indicates whether the dialog box processed the message.</span></span> <span data-ttu-id="4dc03-107">您可以使用 [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="4dc03-107">You can send this message explicitly or by using the [**PropSheet\_IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4dc03-108">參數</span><span class="sxs-lookup"><span data-stu-id="4dc03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dc03-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4dc03-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dc03-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4dc03-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4dc03-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4dc03-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4dc03-112">訊息 [**結構的**](/windows/win32/api/winuser/ns-winuser-msg) 指標，其中包含要檢查的訊息。</span><span class="sxs-lookup"><span data-stu-id="4dc03-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dc03-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4dc03-113">Return value</span></span>

<span data-ttu-id="4dc03-114">如果已處理訊息，則傳回 **TRUE** ; 如果尚未處理訊息，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="4dc03-114">Returns **TRUE** if the message has been processed, or **FALSE** if the message has not been processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dc03-115">備註</span><span class="sxs-lookup"><span data-stu-id="4dc03-115">Remarks</span></span>

<span data-ttu-id="4dc03-116">您的訊息迴圈應該使用具有無訊息屬性工作表的 **PSM \_ ISDIALOGMESSAGE** 訊息，將訊息傳遞至 [屬性工作表] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="4dc03-116">Your message loop should use the **PSM\_ISDIALOGMESSAGE** message with modeless property sheets to pass messages to the property sheet dialog box.</span></span> <span data-ttu-id="4dc03-117">在支援 Unicode 的系統上，請使用 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 和 [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) 函數的 Unicode 版本 (**GetMessageW** 和 **PeekMessageW**) 來取得訊息。</span><span class="sxs-lookup"><span data-stu-id="4dc03-117">On systems that support Unicode, use the Unicode versions of the [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) functions (**GetMessageW** and **PeekMessageW**) to retrieve messages.</span></span>

<span data-ttu-id="4dc03-118">如果傳回值指出已處理訊息，則不能將它傳遞給 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 或 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="4dc03-118">If the return value indicates that the message was processed, it must not be passed to the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) or [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function.</span></span>

> [!Note]  
> <span data-ttu-id="4dc03-119">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="4dc03-119">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4dc03-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="4dc03-120">Requirements</span></span>



| <span data-ttu-id="4dc03-121">需求</span><span class="sxs-lookup"><span data-stu-id="4dc03-121">Requirement</span></span> | <span data-ttu-id="4dc03-122">值</span><span class="sxs-lookup"><span data-stu-id="4dc03-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4dc03-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4dc03-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4dc03-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dc03-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4dc03-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4dc03-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4dc03-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4dc03-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4dc03-127">標頭</span><span class="sxs-lookup"><span data-stu-id="4dc03-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dc03-128"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4dc03-128"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dc03-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4dc03-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dc03-130">**PropertySheet**</span><span class="sxs-lookup"><span data-stu-id="4dc03-130">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 


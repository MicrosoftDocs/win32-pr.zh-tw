---
title: 'PSM_SETHEADERSUBTITLE 訊息 (Prsht.idl .h) '
description: 設定 wizard 內部頁面標頭的子標題文字。 您可以明確地傳送此訊息，或使用 PropSheet \_ SetHeaderSubTitle 宏。
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- PSM_SETHEADERSUBTITLE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934315"
---
# <a name="psm_setheadersubtitle-message"></a><span data-ttu-id="54a8d-105">PSM \_ SETHEADERSUBTITLE 訊息</span><span class="sxs-lookup"><span data-stu-id="54a8d-105">PSM\_SETHEADERSUBTITLE message</span></span>

<span data-ttu-id="54a8d-106">設定 wizard 內部頁面標頭的子標題文字。</span><span class="sxs-lookup"><span data-stu-id="54a8d-106">Sets the subtitle text for the header of a wizard's interior page.</span></span> <span data-ttu-id="54a8d-107">您可以明確地傳送此訊息，或使用 [**PropSheet \_ SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) 宏。</span><span class="sxs-lookup"><span data-stu-id="54a8d-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="54a8d-108">參數</span><span class="sxs-lookup"><span data-stu-id="54a8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54a8d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54a8d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54a8d-110">以零為基底的 wizard 頁面索引。</span><span class="sxs-lookup"><span data-stu-id="54a8d-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="54a8d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54a8d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54a8d-112">新的標頭副標題。</span><span class="sxs-lookup"><span data-stu-id="54a8d-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54a8d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="54a8d-113">Return value</span></span>

<span data-ttu-id="54a8d-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="54a8d-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54a8d-115">備註</span><span class="sxs-lookup"><span data-stu-id="54a8d-115">Remarks</span></span>

<span data-ttu-id="54a8d-116">如果您指定目前的頁面，則會立即重新繪製以顯示新的子標題。</span><span class="sxs-lookup"><span data-stu-id="54a8d-116">If you specify the current page, it will immediately be repainted to display the new subtitle.</span></span>

> [!Note]  
> <span data-ttu-id="54a8d-117">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="54a8d-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54a8d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="54a8d-118">Requirements</span></span>



| <span data-ttu-id="54a8d-119">需求</span><span class="sxs-lookup"><span data-stu-id="54a8d-119">Requirement</span></span> | <span data-ttu-id="54a8d-120">值</span><span class="sxs-lookup"><span data-stu-id="54a8d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54a8d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54a8d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="54a8d-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54a8d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="54a8d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54a8d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="54a8d-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54a8d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54a8d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="54a8d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="54a8d-126"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="54a8d-126"><dt>Prsht.h</dt></span></span> </dl>      |
| <span data-ttu-id="54a8d-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="54a8d-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="54a8d-128">**PSM \_SETHEADERSUBTITLEW** (Unicode) 和 **PSM \_ SETHEADERSUBTITLEA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="54a8d-128">**PSM\_SETHEADERSUBTITLEW** (Unicode) and **PSM\_SETHEADERSUBTITLEA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54a8d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54a8d-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="54a8d-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="54a8d-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54a8d-131">**PSM \_ HWNDTOINDEX**</span><span class="sxs-lookup"><span data-stu-id="54a8d-131">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="54a8d-132">**PSM \_ IDTOINDEX**</span><span class="sxs-lookup"><span data-stu-id="54a8d-132">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="54a8d-133">**PSM \_ PAGETOINDEX**</span><span class="sxs-lookup"><span data-stu-id="54a8d-133">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 






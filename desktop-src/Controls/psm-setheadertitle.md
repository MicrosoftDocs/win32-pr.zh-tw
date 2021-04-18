---
title: 'PSM_SETHEADERTITLE 訊息 (Prsht.idl .h) '
description: 設定 wizard 內部頁面標頭的標題文字。 您可以明確地傳送此訊息，或使用 PropSheet \_ SetHeaderTitle 宏。
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- PSM_SETHEADERTITLE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965275"
---
# <a name="psm_setheadertitle-message"></a><span data-ttu-id="05dfe-105">PSM \_ SETHEADERTITLE 訊息</span><span class="sxs-lookup"><span data-stu-id="05dfe-105">PSM\_SETHEADERTITLE message</span></span>

<span data-ttu-id="05dfe-106">設定 wizard 內部頁面標頭的標題文字。</span><span class="sxs-lookup"><span data-stu-id="05dfe-106">Sets the title text for the header of a wizard's interior page.</span></span> <span data-ttu-id="05dfe-107">您可以明確地傳送此訊息，或使用 [**PropSheet \_ SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) 宏。</span><span class="sxs-lookup"><span data-stu-id="05dfe-107">You can send this message explicitly or use the [**PropSheet\_SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="05dfe-108">參數</span><span class="sxs-lookup"><span data-stu-id="05dfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05dfe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05dfe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05dfe-110">以零為基底的 wizard 頁面索引。</span><span class="sxs-lookup"><span data-stu-id="05dfe-110">Zero-based index of the wizard's page.</span></span>

</dd> <dt>

<span data-ttu-id="05dfe-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05dfe-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05dfe-112">新的標頭副標題。</span><span class="sxs-lookup"><span data-stu-id="05dfe-112">New header subtitle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05dfe-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="05dfe-113">Return value</span></span>

<span data-ttu-id="05dfe-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="05dfe-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05dfe-115">備註</span><span class="sxs-lookup"><span data-stu-id="05dfe-115">Remarks</span></span>

<span data-ttu-id="05dfe-116">如果您指定目前的頁面，則會立即重新繪製以顯示新的標題。</span><span class="sxs-lookup"><span data-stu-id="05dfe-116">If you specify the current page, it will immediately be repainted to display the new title.</span></span>

## <a name="requirements"></a><span data-ttu-id="05dfe-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="05dfe-117">Requirements</span></span>



| <span data-ttu-id="05dfe-118">需求</span><span class="sxs-lookup"><span data-stu-id="05dfe-118">Requirement</span></span> | <span data-ttu-id="05dfe-119">值</span><span class="sxs-lookup"><span data-stu-id="05dfe-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05dfe-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05dfe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="05dfe-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05dfe-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="05dfe-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05dfe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="05dfe-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05dfe-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="05dfe-124">標頭</span><span class="sxs-lookup"><span data-stu-id="05dfe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="05dfe-125"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="05dfe-125"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="05dfe-126">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="05dfe-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="05dfe-127">**PSM \_SETHEADERTITLEW** (Unicode) 和 **PSM \_ SETHEADERTITLEA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="05dfe-127">**PSM\_SETHEADERTITLEW** (Unicode) and **PSM\_SETHEADERTITLEA** (ANSI)</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="05dfe-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05dfe-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="05dfe-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="05dfe-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="05dfe-130">**PSM \_ HWNDTOINDEX**</span><span class="sxs-lookup"><span data-stu-id="05dfe-130">**PSM\_HWNDTOINDEX**</span></span>](psm-hwndtoindex.md)
</dt> <dt>

[<span data-ttu-id="05dfe-131">**PSM \_ IDTOINDEX**</span><span class="sxs-lookup"><span data-stu-id="05dfe-131">**PSM\_IDTOINDEX**</span></span>](psm-idtoindex.md)
</dt> <dt>

[<span data-ttu-id="05dfe-132">**PSM \_ PAGETOINDEX**</span><span class="sxs-lookup"><span data-stu-id="05dfe-132">**PSM\_PAGETOINDEX**</span></span>](psm-pagetoindex.md)
</dt> </dl>

 

 






---
title: 'PSM_CHANGED 訊息 (Prsht.idl .h) '
description: 通知屬性工作表，頁面中的資訊已變更。 您可以使用 PropSheet Changed 宏明確地傳送此訊息 \_ 。
ms.assetid: b092969f-31dc-4e3c-9100-d15f1bdd5aa5
keywords:
- PSM_CHANGED message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_CHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57f931db5e25f816f7ea164ca5871a4e3e7757a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966942"
---
# <a name="psm_changed-message"></a><span data-ttu-id="8c428-105">PSM \_ 變更訊息</span><span class="sxs-lookup"><span data-stu-id="8c428-105">PSM\_CHANGED message</span></span>

<span data-ttu-id="8c428-106">通知屬性工作表，頁面中的資訊已變更。</span><span class="sxs-lookup"><span data-stu-id="8c428-106">Informs a property sheet that information in a page has changed.</span></span> <span data-ttu-id="8c428-107">您可以使用 [**PropSheet \_ Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8c428-107">You can send this message explicitly or by using the [**PropSheet\_Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c428-108">參數</span><span class="sxs-lookup"><span data-stu-id="8c428-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c428-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c428-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c428-110">已變更頁面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8c428-110">Handle to the page that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="8c428-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c428-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c428-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8c428-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c428-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c428-113">Return value</span></span>

<span data-ttu-id="8c428-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="8c428-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c428-115">備註</span><span class="sxs-lookup"><span data-stu-id="8c428-115">Remarks</span></span>

<span data-ttu-id="8c428-116">屬性工作表會啟用 [套用 **] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="8c428-116">The property sheet will enable the **Apply** button.</span></span>

> [!Note]  
> <span data-ttu-id="8c428-117">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="8c428-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c428-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c428-118">Requirements</span></span>



| <span data-ttu-id="8c428-119">需求</span><span class="sxs-lookup"><span data-stu-id="8c428-119">Requirement</span></span> | <span data-ttu-id="8c428-120">值</span><span class="sxs-lookup"><span data-stu-id="8c428-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c428-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c428-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8c428-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c428-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8c428-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c428-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8c428-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c428-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8c428-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8c428-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c428-126"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c428-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 






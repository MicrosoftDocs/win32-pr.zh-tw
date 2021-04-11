---
title: 'PSM_UNCHANGED 訊息 (Prsht.idl .h) '
description: 通知屬性工作表，頁面中的資訊已還原為先前儲存的狀態。 您可以明確地傳送此訊息，或使用 PropSheet \_ 未變更宏。
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- PSM_UNCHANGED message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187309"
---
# <a name="psm_unchanged-message"></a><span data-ttu-id="6168b-105">PSM \_ 未變更訊息</span><span class="sxs-lookup"><span data-stu-id="6168b-105">PSM\_UNCHANGED message</span></span>

<span data-ttu-id="6168b-106">通知屬性工作表，頁面中的資訊已還原為先前儲存的狀態。</span><span class="sxs-lookup"><span data-stu-id="6168b-106">Informs a property sheet that information in a page has reverted to the previously saved state.</span></span> <span data-ttu-id="6168b-107">您可以明確地傳送此訊息，或使用 [**PropSheet \_ 未**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) 變更宏。</span><span class="sxs-lookup"><span data-stu-id="6168b-107">You can send this message explicitly or by using the [**PropSheet\_UnChanged**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6168b-108">參數</span><span class="sxs-lookup"><span data-stu-id="6168b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6168b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6168b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6168b-110">已還原為先前儲存狀態之頁面的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6168b-110">Handle to the page that has reverted to the previously saved state.</span></span>

</dd> <dt>

<span data-ttu-id="6168b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6168b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6168b-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6168b-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6168b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6168b-113">Return value</span></span>

<span data-ttu-id="6168b-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6168b-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6168b-115">備註</span><span class="sxs-lookup"><span data-stu-id="6168b-115">Remarks</span></span>

<span data-ttu-id="6168b-116">如果沒有其他頁面已向屬性工作表註冊變更，屬性工作表會停用 [套用 **] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="6168b-116">The property sheet disables the **Apply** button if no other pages have registered changes with the property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="6168b-117">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="6168b-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6168b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6168b-118">Requirements</span></span>



| <span data-ttu-id="6168b-119">需求</span><span class="sxs-lookup"><span data-stu-id="6168b-119">Requirement</span></span> | <span data-ttu-id="6168b-120">值</span><span class="sxs-lookup"><span data-stu-id="6168b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6168b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6168b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6168b-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6168b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6168b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6168b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6168b-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6168b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6168b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6168b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6168b-126"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6168b-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 






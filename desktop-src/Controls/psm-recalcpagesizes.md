---
title: 'PSM_RECALCPAGESIZES 訊息 (Prsht.idl .h) '
description: 新增或移除頁面之後，重新計算標準或 wizard 屬性工作表的頁面大小。 您可以明確地傳送此訊息，或使用 PropSheet \_ RecalcPageSizes 宏。
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- PSM_RECALCPAGESIZES message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969191"
---
# <a name="psm_recalcpagesizes-message"></a><span data-ttu-id="a604c-105">PSM \_ RECALCPAGESIZES 訊息</span><span class="sxs-lookup"><span data-stu-id="a604c-105">PSM\_RECALCPAGESIZES message</span></span>

<span data-ttu-id="a604c-106">新增或移除頁面之後，重新計算標準或 wizard 屬性工作表的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="a604c-106">Recalculates the page size of a standard or wizard property sheet after pages have been added or removed.</span></span> <span data-ttu-id="a604c-107">您可以明確地傳送此訊息，或使用 [**PropSheet \_ RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) 宏。</span><span class="sxs-lookup"><span data-stu-id="a604c-107">You can send this message explicitly or use the [**PropSheet\_RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a604c-108">參數</span><span class="sxs-lookup"><span data-stu-id="a604c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a604c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a604c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a604c-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a604c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a604c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a604c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a604c-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a604c-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a604c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a604c-113">Return value</span></span>

<span data-ttu-id="a604c-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a604c-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a604c-115">備註</span><span class="sxs-lookup"><span data-stu-id="a604c-115">Remarks</span></span>

<span data-ttu-id="a604c-116">建立屬性工作表時，它會調整大小以符合其初始的頁面集合。</span><span class="sxs-lookup"><span data-stu-id="a604c-116">When a property sheet is created, it is sized to fit its initial collection of pages.</span></span> <span data-ttu-id="a604c-117">為了維持與舊版通用控制項的相容性，屬性工作表和嚮導在後續新增或移除頁面時，不會自動調整大小。</span><span class="sxs-lookup"><span data-stu-id="a604c-117">In order to maintain compatibility with previous versions of the common controls, property sheets and wizards do not automatically resize themselves when pages are subsequently added or removed.</span></span> <span data-ttu-id="a604c-118">使用通用控制項 [5.80 版](common-control-versions.md)時，應用程式應該在加入或移除具有 [**psm \_ ADDPAGE**](psm-addpage.md)、 [**psm \_ INSERTPAGE**](psm-insertpage.md)、 [**psm \_ REMOVEPAGE**](psm-removepage.md)或其對等宏的頁面之後傳送 **psm \_ RECALCPAGESIZES** 訊息。</span><span class="sxs-lookup"><span data-stu-id="a604c-118">With common controls [version 5.80](common-control-versions.md), applications should send a **PSM\_RECALCPAGESIZES** message after adding or removing pages with [**PSM\_ADDPAGE**](psm-addpage.md), [**PSM\_INSERTPAGE**](psm-insertpage.md), [**PSM\_REMOVEPAGE**](psm-removepage.md), or their equivalent macros.</span></span> <span data-ttu-id="a604c-119">它可確保屬性工作表的大小針對其目前的頁面集合正確調整大小。</span><span class="sxs-lookup"><span data-stu-id="a604c-119">It ensures that the property sheet is properly sized for its current collection of pages.</span></span> <span data-ttu-id="a604c-120">如果未傳送此訊息，部分屬性工作表頁面可能會被截斷或太大。</span><span class="sxs-lookup"><span data-stu-id="a604c-120">If this message is not sent, some property sheet pages may be truncated or too large.</span></span>

> [!Note]  
> <span data-ttu-id="a604c-121">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="a604c-121">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a604c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a604c-122">Requirements</span></span>



| <span data-ttu-id="a604c-123">需求</span><span class="sxs-lookup"><span data-stu-id="a604c-123">Requirement</span></span> | <span data-ttu-id="a604c-124">值</span><span class="sxs-lookup"><span data-stu-id="a604c-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a604c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a604c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a604c-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a604c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a604c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a604c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a604c-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a604c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a604c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="a604c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a604c-130"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a604c-130"><dt>Prsht.h</dt></span></span> </dl> |



 

 






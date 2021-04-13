---
title: 'PSM_QUERYSIBLINGS 訊息 (Prsht.idl .h) '
description: 傳送至屬性工作表，然後將訊息轉送到其每個頁面。 您可以使用 PropSheet QuerySiblings 宏明確地傳送此訊息 \_ 。
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- PSM_QUERYSIBLINGS message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508700"
---
# <a name="psm_querysiblings-message"></a><span data-ttu-id="85415-105">PSM \_ QUERYSIBLINGS 訊息</span><span class="sxs-lookup"><span data-stu-id="85415-105">PSM\_QUERYSIBLINGS message</span></span>

<span data-ttu-id="85415-106">傳送至屬性工作表，然後將訊息轉送到其每個頁面。</span><span class="sxs-lookup"><span data-stu-id="85415-106">Sent to a property sheet, which then forwards the message to each of its pages.</span></span> <span data-ttu-id="85415-107">您可以使用 [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="85415-107">You can send this message explicitly or by using the [**PropSheet\_QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="85415-108">參數</span><span class="sxs-lookup"><span data-stu-id="85415-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85415-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85415-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85415-110">第一個應用程式定義的參數。</span><span class="sxs-lookup"><span data-stu-id="85415-110">First application-defined parameter.</span></span>

</dd> <dt>

<span data-ttu-id="85415-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85415-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85415-112">第二個應用程式定義的參數。</span><span class="sxs-lookup"><span data-stu-id="85415-112">Second application-defined parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85415-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="85415-113">Return value</span></span>

<span data-ttu-id="85415-114">從屬性工作表中的頁面傳回非零值; 如果沒有頁面傳回非零值，則為零。</span><span class="sxs-lookup"><span data-stu-id="85415-114">Returns the nonzero value from a page in the property sheet, or zero if no page returns a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85415-115">備註</span><span class="sxs-lookup"><span data-stu-id="85415-115">Remarks</span></span>

<span data-ttu-id="85415-116">如果頁面傳回非零值，則屬性工作表不會將訊息傳送至後續頁面。</span><span class="sxs-lookup"><span data-stu-id="85415-116">If a page returns a nonzero value, the property sheet does not send the message to subsequent pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="85415-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="85415-117">Requirements</span></span>



| <span data-ttu-id="85415-118">需求</span><span class="sxs-lookup"><span data-stu-id="85415-118">Requirement</span></span> | <span data-ttu-id="85415-119">值</span><span class="sxs-lookup"><span data-stu-id="85415-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85415-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85415-120">Minimum supported client</span></span><br/> | <span data-ttu-id="85415-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85415-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="85415-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85415-122">Minimum supported server</span></span><br/> | <span data-ttu-id="85415-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85415-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="85415-124">標頭</span><span class="sxs-lookup"><span data-stu-id="85415-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="85415-125"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="85415-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 






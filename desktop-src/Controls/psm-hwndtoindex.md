---
title: 'PSM_HWNDTOINDEX 訊息 (Prsht.idl .h) '
description: 採用屬性工作表頁面的視窗控制碼，並傳回其以零為基底的索引。 您可以明確地傳送此訊息，或使用 PropSheet \_ HwndToIndex 宏。
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- PSM_HWNDTOINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104196"
---
# <a name="psm_hwndtoindex-message"></a><span data-ttu-id="e758c-105">PSM \_ HWNDTOINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="e758c-105">PSM\_HWNDTOINDEX message</span></span>

<span data-ttu-id="e758c-106">採用屬性工作表頁面的視窗控制碼，並傳回其以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="e758c-106">Takes the window handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="e758c-107">您可以明確地傳送此訊息，或使用 [**PropSheet \_ HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) 宏。</span><span class="sxs-lookup"><span data-stu-id="e758c-107">You can send this message explicitly or use the [**PropSheet\_HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e758c-108">參數</span><span class="sxs-lookup"><span data-stu-id="e758c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e758c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e758c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e758c-110">頁面視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e758c-110">Handle to the page's window.</span></span>

</dd> <dt>

<span data-ttu-id="e758c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e758c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e758c-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e758c-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e758c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e758c-113">Return value</span></span>

<span data-ttu-id="e758c-114">如果成功，則傳回 *wParam* 所指定之屬性工作表頁面的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="e758c-114">Returns the zero-based index of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="e758c-115">否則，它會傳回 -1。</span><span class="sxs-lookup"><span data-stu-id="e758c-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="e758c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e758c-116">Requirements</span></span>



| <span data-ttu-id="e758c-117">需求</span><span class="sxs-lookup"><span data-stu-id="e758c-117">Requirement</span></span> | <span data-ttu-id="e758c-118">值</span><span class="sxs-lookup"><span data-stu-id="e758c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e758c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e758c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e758c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e758c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e758c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e758c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e758c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e758c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e758c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e758c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e758c-124"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e758c-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






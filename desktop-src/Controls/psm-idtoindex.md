---
title: 'PSM_IDTOINDEX 訊息 (Prsht.idl .h) '
description: 取得屬性工作表頁面的資源識別碼，並傳回其以零為基底的索引。 您可以明確地傳送此訊息，或使用 PropSheet \_ IdToIndex 宏。
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- PSM_IDTOINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105275"
---
# <a name="psm_idtoindex-message"></a><span data-ttu-id="8fe88-105">PSM \_ IDTOINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="8fe88-105">PSM\_IDTOINDEX message</span></span>

<span data-ttu-id="8fe88-106">取得屬性工作表頁面的資源識別碼，並傳回其以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="8fe88-106">Takes the resource ID of a property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="8fe88-107">您可以明確地傳送此訊息，或使用 [**PropSheet \_ IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) 宏。</span><span class="sxs-lookup"><span data-stu-id="8fe88-107">You can send this message explicitly or use the [**PropSheet\_IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fe88-108">參數</span><span class="sxs-lookup"><span data-stu-id="8fe88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe88-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8fe88-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fe88-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="8fe88-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8fe88-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8fe88-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8fe88-112">頁面的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8fe88-112">Resource ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe88-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fe88-113">Return value</span></span>

<span data-ttu-id="8fe88-114">如果成功，則傳回 *lParam* 所指定之屬性工作表頁面的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="8fe88-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="8fe88-115">否則，它會傳回 -1。</span><span class="sxs-lookup"><span data-stu-id="8fe88-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe88-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fe88-116">Requirements</span></span>



| <span data-ttu-id="8fe88-117">需求</span><span class="sxs-lookup"><span data-stu-id="8fe88-117">Requirement</span></span> | <span data-ttu-id="8fe88-118">值</span><span class="sxs-lookup"><span data-stu-id="8fe88-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe88-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fe88-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe88-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fe88-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8fe88-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fe88-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe88-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fe88-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8fe88-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8fe88-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fe88-124"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8fe88-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






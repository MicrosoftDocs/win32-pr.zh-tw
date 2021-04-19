---
title: 'PSM_PAGETOINDEX 訊息 (Prsht.idl .h) '
description: 取得屬性工作表頁面的 HPROPSHEETPAGE 控制碼，並傳回其以零為基底的索引。 您可以明確地傳送此訊息，或使用 PropSheet \_ PageToIndex 宏。
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- PSM_PAGETOINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106978595"
---
# <a name="psm_pagetoindex-message"></a><span data-ttu-id="93e59-105">PSM \_ PAGETOINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="93e59-105">PSM\_PAGETOINDEX message</span></span>

<span data-ttu-id="93e59-106">取得屬性工作表頁面的 HPROPSHEETPAGE 控制碼，並傳回其以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="93e59-106">Takes the HPROPSHEETPAGE handle of the property sheet page and returns its zero-based index.</span></span> <span data-ttu-id="93e59-107">您可以明確地傳送此訊息，或使用 [**PropSheet \_ PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) 宏。</span><span class="sxs-lookup"><span data-stu-id="93e59-107">You can send this message explicitly or use the [**PropSheet\_PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="93e59-108">參數</span><span class="sxs-lookup"><span data-stu-id="93e59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e59-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93e59-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93e59-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="93e59-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="93e59-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93e59-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93e59-112">屬性工作表頁面的 HPROPSHEETPAGE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="93e59-112">HPROPSHEETPAGE handle to the property sheet page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e59-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="93e59-113">Return value</span></span>

<span data-ttu-id="93e59-114">如果成功，則傳回 *lParam* 所指定之屬性工作表頁面的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="93e59-114">Returns the zero-based index of the property sheet page specified by *lParam* if successful.</span></span> <span data-ttu-id="93e59-115">否則，它會傳回 -1。</span><span class="sxs-lookup"><span data-stu-id="93e59-115">Otherwise, it returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e59-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="93e59-116">Requirements</span></span>



| <span data-ttu-id="93e59-117">需求</span><span class="sxs-lookup"><span data-stu-id="93e59-117">Requirement</span></span> | <span data-ttu-id="93e59-118">值</span><span class="sxs-lookup"><span data-stu-id="93e59-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93e59-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93e59-119">Minimum supported client</span></span><br/> | <span data-ttu-id="93e59-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93e59-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="93e59-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93e59-121">Minimum supported server</span></span><br/> | <span data-ttu-id="93e59-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93e59-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="93e59-123">標頭</span><span class="sxs-lookup"><span data-stu-id="93e59-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="93e59-124"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="93e59-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






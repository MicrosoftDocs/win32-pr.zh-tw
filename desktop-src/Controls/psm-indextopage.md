---
title: 'PSM_INDEXTOPAGE 訊息 (Prsht.idl .h) '
description: 取得屬性工作表頁面的索引，並傳回其 HPROPSHEETPAGE 控制碼。 您可以明確地傳送此訊息，或使用 PropSheet \_ IndexToPage 宏。
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- PSM_INDEXTOPAGE message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466324"
---
# <a name="psm_indextopage-message"></a><span data-ttu-id="4038b-105">PSM \_ INDEXTOPAGE 訊息</span><span class="sxs-lookup"><span data-stu-id="4038b-105">PSM\_INDEXTOPAGE message</span></span>

<span data-ttu-id="4038b-106">取得屬性工作表頁面的索引，並傳回其 HPROPSHEETPAGE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="4038b-106">Takes the index of a property sheet page and returns its HPROPSHEETPAGE handle.</span></span> <span data-ttu-id="4038b-107">您可以明確地傳送此訊息，或使用 [**PropSheet \_ IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) 宏。</span><span class="sxs-lookup"><span data-stu-id="4038b-107">You can send this message explicitly or use the [**PropSheet\_IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4038b-108">參數</span><span class="sxs-lookup"><span data-stu-id="4038b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4038b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4038b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4038b-110">以零為基底的頁面索引。</span><span class="sxs-lookup"><span data-stu-id="4038b-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="4038b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4038b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4038b-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4038b-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4038b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4038b-113">Return value</span></span>

<span data-ttu-id="4038b-114">如果成功，則傳回 *wParam* 所指定之屬性工作表頁面的 HPROPSHEETPAGE 控制碼。</span><span class="sxs-lookup"><span data-stu-id="4038b-114">Returns the HPROPSHEETPAGE handle of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="4038b-115">否則，它會傳回零。</span><span class="sxs-lookup"><span data-stu-id="4038b-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4038b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4038b-116">Requirements</span></span>



| <span data-ttu-id="4038b-117">需求</span><span class="sxs-lookup"><span data-stu-id="4038b-117">Requirement</span></span> | <span data-ttu-id="4038b-118">值</span><span class="sxs-lookup"><span data-stu-id="4038b-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4038b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4038b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4038b-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4038b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4038b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4038b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4038b-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4038b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4038b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4038b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4038b-124"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4038b-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






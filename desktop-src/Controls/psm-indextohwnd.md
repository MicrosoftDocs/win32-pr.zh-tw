---
title: 'PSM_INDEXTOHWND 訊息 (Prsht.idl .h) '
description: 取得屬性工作表頁面的索引，並傳回其視窗控制碼。 您可以明確地傳送此訊息，或使用 PropSheet \_ IndexToHwnd 宏。
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- PSM_INDEXTOHWND message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105263"
---
# <a name="psm_indextohwnd-message"></a><span data-ttu-id="af1b5-105">PSM \_ INDEXTOHWND 訊息</span><span class="sxs-lookup"><span data-stu-id="af1b5-105">PSM\_INDEXTOHWND message</span></span>

<span data-ttu-id="af1b5-106">取得屬性工作表頁面的索引，並傳回其視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="af1b5-106">Takes the index of a property sheet page and returns its window handle.</span></span> <span data-ttu-id="af1b5-107">您可以明確地傳送此訊息，或使用 [**PropSheet \_ IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) 宏。</span><span class="sxs-lookup"><span data-stu-id="af1b5-107">You can send this message explicitly or use the [**PropSheet\_IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="af1b5-108">參數</span><span class="sxs-lookup"><span data-stu-id="af1b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af1b5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af1b5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af1b5-110">以零為基底的頁面索引。</span><span class="sxs-lookup"><span data-stu-id="af1b5-110">Zero-based index of the page.</span></span>

</dd> <dt>

<span data-ttu-id="af1b5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af1b5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af1b5-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="af1b5-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af1b5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="af1b5-113">Return value</span></span>

<span data-ttu-id="af1b5-114">如果成功，則傳回 *wParam* 所指定之屬性工作表頁面的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="af1b5-114">Returns the handle to the window of the property sheet page specified by *wParam* if successful.</span></span> <span data-ttu-id="af1b5-115">否則，它會傳回零。</span><span class="sxs-lookup"><span data-stu-id="af1b5-115">Otherwise, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="af1b5-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="af1b5-116">Requirements</span></span>



| <span data-ttu-id="af1b5-117">需求</span><span class="sxs-lookup"><span data-stu-id="af1b5-117">Requirement</span></span> | <span data-ttu-id="af1b5-118">值</span><span class="sxs-lookup"><span data-stu-id="af1b5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af1b5-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af1b5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="af1b5-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af1b5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="af1b5-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af1b5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="af1b5-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af1b5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="af1b5-123">標頭</span><span class="sxs-lookup"><span data-stu-id="af1b5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="af1b5-124"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="af1b5-124"><dt>Prsht.h</dt></span></span> </dl> |



 

 






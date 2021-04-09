---
title: 'PSM_SETNEXTTEXT 訊息 (Prsht.idl .h) '
description: 設定 wizard 中 [下一步] 按鈕的文字。 您可以使用 PropSheet SetNextText 宏明確地傳送此訊息 \_ 。
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- PSM_SETNEXTTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d781a8d76fca5c1e74bcda452b6ab7e03a32aacc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685556"
---
# <a name="psm_setnexttext-message"></a><span data-ttu-id="76caa-105">PSM \_ SETNEXTTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="76caa-105">PSM\_SETNEXTTEXT message</span></span>

<span data-ttu-id="76caa-106">設定 wizard 中 [ **下一步** ] 按鈕的文字。</span><span class="sxs-lookup"><span data-stu-id="76caa-106">Sets the text of the **Next** button in a wizard.</span></span> <span data-ttu-id="76caa-107">您可以使用 [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="76caa-107">You can send this message explicitly or by using the [**PropSheet\_SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="76caa-108">參數</span><span class="sxs-lookup"><span data-stu-id="76caa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76caa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76caa-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76caa-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="76caa-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="76caa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76caa-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76caa-112">包含文字之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="76caa-112">Pointer to a buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76caa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="76caa-113">Return value</span></span>

<span data-ttu-id="76caa-114">沒有有意義的傳回值。</span><span class="sxs-lookup"><span data-stu-id="76caa-114">No meaningful return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="76caa-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="76caa-115">Requirements</span></span>



| <span data-ttu-id="76caa-116">需求</span><span class="sxs-lookup"><span data-stu-id="76caa-116">Requirement</span></span> | <span data-ttu-id="76caa-117">值</span><span class="sxs-lookup"><span data-stu-id="76caa-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76caa-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76caa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76caa-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76caa-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="76caa-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76caa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76caa-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76caa-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="76caa-122">標頭</span><span class="sxs-lookup"><span data-stu-id="76caa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="76caa-123"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="76caa-123"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="76caa-124">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="76caa-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="76caa-125">**PSM \_SETNEXTTEXTW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="76caa-125">**PSM\_SETNEXTTEXTW** (Unicode)</span></span><br/>                                         |



 

 






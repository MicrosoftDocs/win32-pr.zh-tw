---
title: 'PGM_GETBORDER 訊息 (Commctrl .h) '
description: 抓取呼機控制項目前的框線大小。 您可以明確地傳送此訊息，或使用呼叫器 \_ GetBorder 宏。
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- PGM_GETBORDER message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001311"
---
# <a name="pgm_getborder-message"></a><span data-ttu-id="15ea4-105">PGM \_ GETBORDER 訊息</span><span class="sxs-lookup"><span data-stu-id="15ea4-105">PGM\_GETBORDER message</span></span>

<span data-ttu-id="15ea4-106">抓取呼機控制項目前的框線大小。</span><span class="sxs-lookup"><span data-stu-id="15ea4-106">Retrieves the current border size for the pager control.</span></span> <span data-ttu-id="15ea4-107">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) 宏。</span><span class="sxs-lookup"><span data-stu-id="15ea4-107">You can send this message explicitly or use the [**Pager\_GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="15ea4-108">參數</span><span class="sxs-lookup"><span data-stu-id="15ea4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15ea4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15ea4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="15ea4-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="15ea4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="15ea4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15ea4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="15ea4-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="15ea4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15ea4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="15ea4-113">Return value</span></span>

<span data-ttu-id="15ea4-114">傳回包含目前框線大小的 INT 值（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="15ea4-114">Returns an INT value that contains the current border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="15ea4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="15ea4-115">Requirements</span></span>



| <span data-ttu-id="15ea4-116">需求</span><span class="sxs-lookup"><span data-stu-id="15ea4-116">Requirement</span></span> | <span data-ttu-id="15ea4-117">值</span><span class="sxs-lookup"><span data-stu-id="15ea4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15ea4-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15ea4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="15ea4-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15ea4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="15ea4-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15ea4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="15ea4-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15ea4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="15ea4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="15ea4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="15ea4-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="15ea4-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15ea4-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15ea4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ea4-125">**PGM \_ SETBORDER**</span><span class="sxs-lookup"><span data-stu-id="15ea4-125">**PGM\_SETBORDER**</span></span>](pgm-setborder.md)
</dt> </dl>

 

 






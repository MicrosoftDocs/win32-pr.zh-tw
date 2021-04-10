---
title: 'HDM_GETBITMAPMARGIN 訊息 (Commctrl .h) '
description: 取得標題控制項之點陣圖邊界的寬度。 您可以明確地傳送此訊息，或使用標頭 \_ GetBitmapMargin 宏。
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- HDM_GETBITMAPMARGIN message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c3f0fced77edd3f149009e1b3c2bb1eb75182c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934416"
---
# <a name="hdm_getbitmapmargin-message"></a><span data-ttu-id="7104c-105">HDM \_ GETBITMAPMARGIN 訊息</span><span class="sxs-lookup"><span data-stu-id="7104c-105">HDM\_GETBITMAPMARGIN message</span></span>

<span data-ttu-id="7104c-106">取得標題控制項之點陣圖邊界的寬度。</span><span class="sxs-lookup"><span data-stu-id="7104c-106">Gets the width of the bitmap margin for a header control.</span></span> <span data-ttu-id="7104c-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) 宏。</span><span class="sxs-lookup"><span data-stu-id="7104c-107">You can send this message explicitly or use the [**Header\_GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7104c-108">參數</span><span class="sxs-lookup"><span data-stu-id="7104c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7104c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7104c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7104c-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7104c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7104c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7104c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7104c-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="7104c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7104c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7104c-113">Return value</span></span>

<span data-ttu-id="7104c-114">傳回點陣圖邊界的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7104c-114">Returns the width of the bitmap margin in pixels.</span></span> <span data-ttu-id="7104c-115">如果之前未指定點陣圖邊界，則會傳回預設值 3 \* [**GETSYSTEMMETRICS**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ CXEDGE) 。</span><span class="sxs-lookup"><span data-stu-id="7104c-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM\_CXEDGE) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7104c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7104c-116">Requirements</span></span>



| <span data-ttu-id="7104c-117">需求</span><span class="sxs-lookup"><span data-stu-id="7104c-117">Requirement</span></span> | <span data-ttu-id="7104c-118">值</span><span class="sxs-lookup"><span data-stu-id="7104c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7104c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7104c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7104c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7104c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7104c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7104c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7104c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7104c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7104c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7104c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7104c-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7104c-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7104c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7104c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7104c-126">**HDM \_ SETBITMAPMARGIN**</span><span class="sxs-lookup"><span data-stu-id="7104c-126">**HDM\_SETBITMAPMARGIN**</span></span>](hdm-setbitmapmargin.md)
</dt> </dl>

 


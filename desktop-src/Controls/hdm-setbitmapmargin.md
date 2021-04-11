---
title: 'HDM_SETBITMAPMARGIN 訊息 (Commctrl .h) '
description: 在現有的標題控制項中，設定點陣圖的邊界寬度（以圖元為單位）。 您可以明確地傳送此訊息，或使用標頭 \_ SetBitmapMargin 宏。
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- HDM_SETBITMAPMARGIN message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844040"
---
# <a name="hdm_setbitmapmargin-message"></a><span data-ttu-id="4429c-105">HDM \_ SETBITMAPMARGIN 訊息</span><span class="sxs-lookup"><span data-stu-id="4429c-105">HDM\_SETBITMAPMARGIN message</span></span>

<span data-ttu-id="4429c-106">在現有的標題控制項中，設定點陣圖的邊界寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4429c-106">Sets the width of the margin, specified in pixels, of a bitmap in an existing header control.</span></span> <span data-ttu-id="4429c-107">您可以明確地傳送此訊息，或使用 [**標頭 \_ SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) 宏。</span><span class="sxs-lookup"><span data-stu-id="4429c-107">You can send this message explicitly or use the [**Header\_SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4429c-108">參數</span><span class="sxs-lookup"><span data-stu-id="4429c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4429c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4429c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4429c-110">在現有的標題控制項內圍住點陣圖之邊界的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4429c-110">The width, specified in pixels, of the margin that surrounds a bitmap within an existing header control.</span></span>

</dd> <dt>

<span data-ttu-id="4429c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4429c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4429c-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="4429c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4429c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4429c-113">Return value</span></span>

<span data-ttu-id="4429c-114">傳回點陣圖邊界的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="4429c-114">Returns the width of the bitmap margin, in pixels.</span></span> <span data-ttu-id="4429c-115">如果之前未指定點陣圖邊界，則會傳回預設值 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*) 。</span><span class="sxs-lookup"><span data-stu-id="4429c-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM\_CXEDGE*) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="4429c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4429c-116">Requirements</span></span>



| <span data-ttu-id="4429c-117">需求</span><span class="sxs-lookup"><span data-stu-id="4429c-117">Requirement</span></span> | <span data-ttu-id="4429c-118">值</span><span class="sxs-lookup"><span data-stu-id="4429c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4429c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4429c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4429c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4429c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4429c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4429c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4429c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4429c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4429c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4429c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4429c-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4429c-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4429c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4429c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4429c-126">**HDM \_ GETBITMAPMARGIN**</span><span class="sxs-lookup"><span data-stu-id="4429c-126">**HDM\_GETBITMAPMARGIN**</span></span>](hdm-getbitmapmargin.md)
</dt> </dl>

 


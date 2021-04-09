---
title: 'PGM_SETBORDER 訊息 (Commctrl .h) '
description: 設定呼機控制項的目前框線大小。 您可以明確地傳送此訊息，或使用呼叫器 \_ SetBorder 宏。
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- PGM_SETBORDER message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024992"
---
# <a name="pgm_setborder-message"></a><span data-ttu-id="33a3e-105">PGM \_ SETBORDER 訊息</span><span class="sxs-lookup"><span data-stu-id="33a3e-105">PGM\_SETBORDER message</span></span>

<span data-ttu-id="33a3e-106">設定呼機控制項的目前框線大小。</span><span class="sxs-lookup"><span data-stu-id="33a3e-106">Sets the current border size for the pager control.</span></span> <span data-ttu-id="33a3e-107">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) 宏。</span><span class="sxs-lookup"><span data-stu-id="33a3e-107">You can send this message explicitly or use the [**Pager\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="33a3e-108">參數</span><span class="sxs-lookup"><span data-stu-id="33a3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33a3e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33a3e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="33a3e-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="33a3e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="33a3e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33a3e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33a3e-112">框線的新大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="33a3e-112">New size of the border, in pixels.</span></span> <span data-ttu-id="33a3e-113">此值不應大於呼機按鈕或小於零。</span><span class="sxs-lookup"><span data-stu-id="33a3e-113">This value should not be larger than the pager button or less than zero.</span></span> <span data-ttu-id="33a3e-114">如果 *lParam* 太大，框線將會繪製成與按鈕相同的大小。</span><span class="sxs-lookup"><span data-stu-id="33a3e-114">If *lParam* is too large, the border will be drawn the same size as the button.</span></span> <span data-ttu-id="33a3e-115">如果 *lParam* 為負數，則框線大小將設定為零。</span><span class="sxs-lookup"><span data-stu-id="33a3e-115">If *lParam* is negative, the border size will be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33a3e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="33a3e-116">Return value</span></span>

<span data-ttu-id="33a3e-117">傳回包含先前框線大小的 INT 值（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="33a3e-117">Returns an INT value that contains the previous border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a3e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="33a3e-118">Requirements</span></span>



| <span data-ttu-id="33a3e-119">需求</span><span class="sxs-lookup"><span data-stu-id="33a3e-119">Requirement</span></span> | <span data-ttu-id="33a3e-120">值</span><span class="sxs-lookup"><span data-stu-id="33a3e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33a3e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33a3e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33a3e-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33a3e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33a3e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33a3e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33a3e-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33a3e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33a3e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="33a3e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="33a3e-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="33a3e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






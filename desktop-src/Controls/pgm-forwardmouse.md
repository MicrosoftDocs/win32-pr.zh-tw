---
title: 'PGM_FORWARDMOUSE 訊息 (Commctrl .h) '
description: 啟用或停用呼機控制項的滑鼠轉送。 啟用滑鼠轉寄時，分頁控制項會將 WM \_ MOUSEMOVE 訊息轉送至包含的視窗。 您可以明確地傳送此訊息，或使用呼叫器 \_ ForwardMouse 宏。
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- PGM_FORWARDMOUSE message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967746"
---
# <a name="pgm_forwardmouse-message"></a><span data-ttu-id="e365a-106">PGM \_ FORWARDMOUSE 訊息</span><span class="sxs-lookup"><span data-stu-id="e365a-106">PGM\_FORWARDMOUSE message</span></span>

<span data-ttu-id="e365a-107">啟用或停用呼機控制項的滑鼠轉送。</span><span class="sxs-lookup"><span data-stu-id="e365a-107">Enables or disables mouse forwarding for the pager control.</span></span> <span data-ttu-id="e365a-108">啟用滑鼠轉寄時，分頁控制項會將 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) 訊息轉送至包含的視窗。</span><span class="sxs-lookup"><span data-stu-id="e365a-108">When mouse forwarding is enabled, the pager control forwards [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to the contained window.</span></span> <span data-ttu-id="e365a-109">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) 宏。</span><span class="sxs-lookup"><span data-stu-id="e365a-109">You can send this message explicitly or use the [**Pager\_ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e365a-110">參數</span><span class="sxs-lookup"><span data-stu-id="e365a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e365a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e365a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e365a-112">**布林** 值，決定是否啟用或停用滑鼠轉送。</span><span class="sxs-lookup"><span data-stu-id="e365a-112">**BOOL** value that determines if mouse forwarding is enabled or disabled.</span></span> <span data-ttu-id="e365a-113">如果此值為非零值，則會啟用滑鼠轉送。</span><span class="sxs-lookup"><span data-stu-id="e365a-113">If this value is nonzero, mouse forwarding is enabled.</span></span> <span data-ttu-id="e365a-114">如果此值為零，則會停用滑鼠轉送。</span><span class="sxs-lookup"><span data-stu-id="e365a-114">If this value is zero, mouse forwarding is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="e365a-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e365a-115">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e365a-116">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e365a-116">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e365a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="e365a-117">Return value</span></span>

<span data-ttu-id="e365a-118">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="e365a-118">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e365a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e365a-119">Requirements</span></span>



| <span data-ttu-id="e365a-120">需求</span><span class="sxs-lookup"><span data-stu-id="e365a-120">Requirement</span></span> | <span data-ttu-id="e365a-121">值</span><span class="sxs-lookup"><span data-stu-id="e365a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e365a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e365a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e365a-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e365a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e365a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e365a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e365a-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e365a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e365a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e365a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e365a-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e365a-127"><dt>Commctrl.h</dt></span></span> </dl> |



 


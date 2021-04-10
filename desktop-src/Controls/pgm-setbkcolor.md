---
title: 'PGM_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定呼機控制項目前的背景色彩。 您可以明確地傳送此訊息，或使用呼叫器 \_ SetBkColor 宏。
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- PGM_SETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9e8dc1c0cad3e60bdde3f3c05d77d8c57b98ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094428"
---
# <a name="pgm_setbkcolor-message"></a><span data-ttu-id="790ec-105">PGM \_ SETBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="790ec-105">PGM\_SETBKCOLOR message</span></span>

<span data-ttu-id="790ec-106">設定呼機控制項目前的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="790ec-106">Sets the current background color for the pager control.</span></span> <span data-ttu-id="790ec-107">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) 宏。</span><span class="sxs-lookup"><span data-stu-id="790ec-107">You can send this message explicitly or use the [**Pager\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="790ec-108">參數</span><span class="sxs-lookup"><span data-stu-id="790ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="790ec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="790ec-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="790ec-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="790ec-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="790ec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="790ec-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="790ec-112">**COLORREF** 值，其中包含分頁控制項的新背景色彩。</span><span class="sxs-lookup"><span data-stu-id="790ec-112">**COLORREF** value that contains the new background color of the pager control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="790ec-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="790ec-113">Return value</span></span>

<span data-ttu-id="790ec-114">傳回包含先前背景色彩的 **COLORREF** 值。</span><span class="sxs-lookup"><span data-stu-id="790ec-114">Returns a **COLORREF** value that contains the previous background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="790ec-115">備註</span><span class="sxs-lookup"><span data-stu-id="790ec-115">Remarks</span></span>

<span data-ttu-id="790ec-116">根據預設，分頁控制項會使用系統按鈕的臉部色彩做為背景色彩。</span><span class="sxs-lookup"><span data-stu-id="790ec-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="790ec-117">這種色彩可透過呼叫 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 和 color BTNFACE 來抓取 \_ 。</span><span class="sxs-lookup"><span data-stu-id="790ec-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="790ec-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="790ec-118">Requirements</span></span>



| <span data-ttu-id="790ec-119">需求</span><span class="sxs-lookup"><span data-stu-id="790ec-119">Requirement</span></span> | <span data-ttu-id="790ec-120">值</span><span class="sxs-lookup"><span data-stu-id="790ec-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="790ec-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="790ec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="790ec-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="790ec-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="790ec-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="790ec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="790ec-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="790ec-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="790ec-125">標頭</span><span class="sxs-lookup"><span data-stu-id="790ec-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="790ec-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="790ec-126"><dt>Commctrl.h</dt></span></span> </dl> |



 


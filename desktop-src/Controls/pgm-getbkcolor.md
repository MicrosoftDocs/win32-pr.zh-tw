---
title: 'PGM_GETBKCOLOR 訊息 (Commctrl .h) '
description: 抓取呼機控制項目前的背景色彩。 您可以明確地傳送此訊息，或使用呼叫器 \_ GetBkColor 宏。
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- PGM_GETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b58b139dd1caafcdefc6893e2b8a5e3312d3e28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686164"
---
# <a name="pgm_getbkcolor-message"></a><span data-ttu-id="ca937-105">PGM \_ GETBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="ca937-105">PGM\_GETBKCOLOR message</span></span>

<span data-ttu-id="ca937-106">抓取呼機控制項目前的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="ca937-106">Retrieves the current background color for the pager control.</span></span> <span data-ttu-id="ca937-107">您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) 宏。</span><span class="sxs-lookup"><span data-stu-id="ca937-107">You can send this message explicitly or use the [**Pager\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca937-108">參數</span><span class="sxs-lookup"><span data-stu-id="ca937-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca937-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca937-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ca937-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ca937-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ca937-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca937-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ca937-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ca937-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca937-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ca937-113">Return value</span></span>

<span data-ttu-id="ca937-114">傳回 **COLORREF** 值，其中包含目前的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="ca937-114">Returns a **COLORREF** value that contains the current background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca937-115">備註</span><span class="sxs-lookup"><span data-stu-id="ca937-115">Remarks</span></span>

<span data-ttu-id="ca937-116">根據預設，分頁控制項會使用系統按鈕的臉部色彩做為背景色彩。</span><span class="sxs-lookup"><span data-stu-id="ca937-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="ca937-117">這種色彩可透過呼叫 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 和 color BTNFACE 來抓取 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ca937-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca937-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca937-118">Requirements</span></span>



| <span data-ttu-id="ca937-119">需求</span><span class="sxs-lookup"><span data-stu-id="ca937-119">Requirement</span></span> | <span data-ttu-id="ca937-120">值</span><span class="sxs-lookup"><span data-stu-id="ca937-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca937-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca937-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ca937-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca937-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca937-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca937-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ca937-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca937-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca937-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ca937-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca937-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca937-126"><dt>Commctrl.h</dt></span></span> </dl> |



 


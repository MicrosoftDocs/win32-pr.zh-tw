---
title: 'SB_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定狀態列中的背景色彩。
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- SB_SETBKCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385065"
---
# <a name="sb_setbkcolor-message"></a><span data-ttu-id="e53f2-104">SB \_ SETBKCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="e53f2-104">SB\_SETBKCOLOR message</span></span>

<span data-ttu-id="e53f2-105">設定狀態列中的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="e53f2-105">Sets the background color in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e53f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="e53f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e53f2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e53f2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e53f2-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e53f2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e53f2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e53f2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e53f2-110">[**COLORREF**](/windows/desktop/gdi/colorref) 值，指定新的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="e53f2-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that specifies the new background color.</span></span> <span data-ttu-id="e53f2-111">指定 CLR \_ 預設值，使狀態列使用其預設背景色彩。</span><span class="sxs-lookup"><span data-stu-id="e53f2-111">Specify the CLR\_DEFAULT value to cause the status bar to use its default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e53f2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e53f2-112">Return value</span></span>

<span data-ttu-id="e53f2-113">傳回先前的背景色彩，或 \_ 如果背景色彩為預設色彩，則為 CLR 預設值。</span><span class="sxs-lookup"><span data-stu-id="e53f2-113">Returns the previous background color, or CLR\_DEFAULT if the background color is the default color.</span></span>

## <a name="requirements"></a><span data-ttu-id="e53f2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e53f2-114">Requirements</span></span>



| <span data-ttu-id="e53f2-115">需求</span><span class="sxs-lookup"><span data-stu-id="e53f2-115">Requirement</span></span> | <span data-ttu-id="e53f2-116">值</span><span class="sxs-lookup"><span data-stu-id="e53f2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e53f2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e53f2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e53f2-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e53f2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e53f2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e53f2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e53f2-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e53f2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e53f2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e53f2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e53f2-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e53f2-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


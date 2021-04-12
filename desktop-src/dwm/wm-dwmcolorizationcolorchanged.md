---
title: 'WM_DWMCOLORIZATIONCOLORCHANGED 訊息 (Winuser .h) '
description: 通知所有最上層視窗的顏色標示色彩已變更。
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- WM_DWMCOLORIZATIONCOLORCHANGED 訊息桌面視窗管理員
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103943"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a><span data-ttu-id="e4f25-104">WM \_ DWMCOLORIZATIONCOLORCHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="e4f25-104">WM\_DWMCOLORIZATIONCOLORCHANGED message</span></span>

<span data-ttu-id="e4f25-105">通知所有最上層視窗的顏色標示色彩已變更。</span><span class="sxs-lookup"><span data-stu-id="e4f25-105">Informs all top-level windows that the colorization color has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4f25-106">參數</span><span class="sxs-lookup"><span data-stu-id="e4f25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4f25-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4f25-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4f25-108">指定新的顏色標示色彩。</span><span class="sxs-lookup"><span data-stu-id="e4f25-108">Specifies the new colorization color.</span></span> <span data-ttu-id="e4f25-109">色彩格式為0xAARRGGBB。</span><span class="sxs-lookup"><span data-stu-id="e4f25-109">The color format is 0xAARRGGBB.</span></span>

</dd> <dt>

<span data-ttu-id="e4f25-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4f25-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4f25-111">指定新的色彩是否與不透明度混合。</span><span class="sxs-lookup"><span data-stu-id="e4f25-111">Specifies whether the new color is blended with opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4f25-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4f25-112">Return value</span></span>

<span data-ttu-id="e4f25-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e4f25-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4f25-114">備註</span><span class="sxs-lookup"><span data-stu-id="e4f25-114">Remarks</span></span>

<span data-ttu-id="e4f25-115">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="e4f25-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="e4f25-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) 用來判斷目前的色彩值。</span><span class="sxs-lookup"><span data-stu-id="e4f25-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) is used to determine the current color value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f25-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4f25-117">Requirements</span></span>



| <span data-ttu-id="e4f25-118">需求</span><span class="sxs-lookup"><span data-stu-id="e4f25-118">Requirement</span></span> | <span data-ttu-id="e4f25-119">值</span><span class="sxs-lookup"><span data-stu-id="e4f25-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f25-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4f25-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f25-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4f25-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e4f25-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4f25-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f25-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4f25-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e4f25-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e4f25-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4f25-125"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="e4f25-125"><dt>Winuser.h</dt></span></span> </dl> |



 


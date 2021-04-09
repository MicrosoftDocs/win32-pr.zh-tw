---
title: 'SB_SETMINHEIGHT 訊息 (Commctrl .h) '
description: 設定狀態視窗之繪圖區域的最小高度。
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- SB_SETMINHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934793"
---
# <a name="sb_setminheight-message"></a><span data-ttu-id="910de-104">SB \_ SETMINHEIGHT 訊息</span><span class="sxs-lookup"><span data-stu-id="910de-104">SB\_SETMINHEIGHT message</span></span>

<span data-ttu-id="910de-105">設定狀態視窗之繪圖區域的最小高度。</span><span class="sxs-lookup"><span data-stu-id="910de-105">Sets the minimum height of a status window's drawing area.</span></span>

## <a name="parameters"></a><span data-ttu-id="910de-106">參數</span><span class="sxs-lookup"><span data-stu-id="910de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="910de-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="910de-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="910de-108">視窗的最小高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="910de-108">Minimum height, in pixels, of the window.</span></span>

</dd> <dt>

<span data-ttu-id="910de-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="910de-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="910de-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="910de-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="910de-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="910de-111">Return value</span></span>

<span data-ttu-id="910de-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="910de-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="910de-113">備註</span><span class="sxs-lookup"><span data-stu-id="910de-113">Remarks</span></span>

<span data-ttu-id="910de-114">最小高度是 *wParam* 和狀態視窗垂直框線寬度（以圖元為單位）的總和。</span><span class="sxs-lookup"><span data-stu-id="910de-114">The minimum height is the sum of *wParam* and twice the width, in pixels, of the vertical border of the status window.</span></span> <span data-ttu-id="910de-115">應用程式必須將 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息傳送至狀態視窗，以重繪視窗。</span><span class="sxs-lookup"><span data-stu-id="910de-115">An application must send the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to the status window to redraw the window.</span></span> <span data-ttu-id="910de-116">**WM \_ 大小** 訊息的 *wParam* 和 *lParam* 參數應設為零。</span><span class="sxs-lookup"><span data-stu-id="910de-116">The *wParam* and *lParam* parameters of the **WM\_SIZE** message should be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="910de-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="910de-117">Requirements</span></span>



| <span data-ttu-id="910de-118">需求</span><span class="sxs-lookup"><span data-stu-id="910de-118">Requirement</span></span> | <span data-ttu-id="910de-119">值</span><span class="sxs-lookup"><span data-stu-id="910de-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="910de-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="910de-120">Minimum supported client</span></span><br/> | <span data-ttu-id="910de-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="910de-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="910de-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="910de-122">Minimum supported server</span></span><br/> | <span data-ttu-id="910de-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="910de-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="910de-124">標頭</span><span class="sxs-lookup"><span data-stu-id="910de-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="910de-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="910de-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


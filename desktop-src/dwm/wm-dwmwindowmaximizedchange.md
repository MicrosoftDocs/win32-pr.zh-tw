---
title: 'WM_DWMWINDOWMAXIMIZEDCHANGE 訊息 (Winuser .h) '
description: 當桌面視窗管理員 (DWM) 撰寫的視窗最大化時傳送。
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- WM_DWMWINDOWMAXIMIZEDCHANGE 訊息桌面視窗管理員
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384733"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a><span data-ttu-id="6649a-104">WM \_ DWMWINDOWMAXIMIZEDCHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="6649a-104">WM\_DWMWINDOWMAXIMIZEDCHANGE message</span></span>

<span data-ttu-id="6649a-105">當桌面視窗管理員 (DWM) 撰寫的視窗最大化時傳送。</span><span class="sxs-lookup"><span data-stu-id="6649a-105">Sent when a Desktop Window Manager (DWM) composed window is maximized.</span></span>

## <a name="parameters"></a><span data-ttu-id="6649a-106">參數</span><span class="sxs-lookup"><span data-stu-id="6649a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6649a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6649a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6649a-108">設定為 true 以指定視窗已最大化。</span><span class="sxs-lookup"><span data-stu-id="6649a-108">Set to true to specify that the window has been maximized.</span></span>

</dd> <dt>

<span data-ttu-id="6649a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6649a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6649a-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="6649a-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6649a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6649a-111">Return value</span></span>

<span data-ttu-id="6649a-112">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6649a-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6649a-113">備註</span><span class="sxs-lookup"><span data-stu-id="6649a-113">Remarks</span></span>

<span data-ttu-id="6649a-114">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="6649a-114">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6649a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6649a-115">Requirements</span></span>



| <span data-ttu-id="6649a-116">需求</span><span class="sxs-lookup"><span data-stu-id="6649a-116">Requirement</span></span> | <span data-ttu-id="6649a-117">值</span><span class="sxs-lookup"><span data-stu-id="6649a-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6649a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6649a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6649a-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6649a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6649a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6649a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6649a-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6649a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6649a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6649a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6649a-123"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="6649a-123"><dt>Winuser.h</dt></span></span> </dl> |



 


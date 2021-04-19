---
title: 'WM_DWMCOMPOSITIONCHANGED 訊息 (Winuser .h) '
description: 通知已啟用或停用桌面視窗管理員 (DWM) 組合的所有最上層視窗。
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- WM_DWMCOMPOSITIONCHANGED 訊息桌面視窗管理員
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967542"
---
# <a name="wm_dwmcompositionchanged-message"></a><span data-ttu-id="944e4-104">WM \_ DWMCOMPOSITIONCHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="944e4-104">WM\_DWMCOMPOSITIONCHANGED message</span></span>

<span data-ttu-id="944e4-105">通知已啟用或停用桌面視窗管理員 (DWM) 組合的所有最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="944e4-105">Informs all top-level windows that Desktop Window Manager (DWM) composition has been enabled or disabled.</span></span>

> [!Note]  
> <span data-ttu-id="944e4-106">從 Windows 8，一律會啟用 DWM 組合，因此不論影片模式變更為何，都不會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="944e4-106">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="944e4-107">參數</span><span class="sxs-lookup"><span data-stu-id="944e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="944e4-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="944e4-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="944e4-109">未使用。</span><span class="sxs-lookup"><span data-stu-id="944e4-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="944e4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="944e4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="944e4-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="944e4-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="944e4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="944e4-112">Return value</span></span>

<span data-ttu-id="944e4-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="944e4-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="944e4-114">備註</span><span class="sxs-lookup"><span data-stu-id="944e4-114">Remarks</span></span>

<span data-ttu-id="944e4-115">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="944e4-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="944e4-116">[**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)函數可以用來判斷目前的組合狀態。</span><span class="sxs-lookup"><span data-stu-id="944e4-116">The [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) function can be used to determine the current composition state.</span></span>

## <a name="requirements"></a><span data-ttu-id="944e4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="944e4-117">Requirements</span></span>



| <span data-ttu-id="944e4-118">需求</span><span class="sxs-lookup"><span data-stu-id="944e4-118">Requirement</span></span> | <span data-ttu-id="944e4-119">值</span><span class="sxs-lookup"><span data-stu-id="944e4-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="944e4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="944e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="944e4-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="944e4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="944e4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="944e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="944e4-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="944e4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="944e4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="944e4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="944e4-125"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="944e4-125"><dt>Winuser.h</dt></span></span> </dl> |



 


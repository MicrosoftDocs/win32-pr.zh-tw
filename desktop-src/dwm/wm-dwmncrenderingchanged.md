---
title: 'WM_DWMNCRENDERINGCHANGED 訊息 (Winuser .h) '
description: 當非工作區轉譯原則變更時傳送。
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- WM_DWMNCRENDERINGCHANGED 訊息桌面視窗管理員
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac32704ea240ccfc4d4de913b940e098ff8f4de4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934458"
---
# <a name="wm_dwmncrenderingchanged-message"></a><span data-ttu-id="a92b2-104">WM \_ DWMNCRENDERINGCHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="a92b2-104">WM\_DWMNCRENDERINGCHANGED message</span></span>

<span data-ttu-id="a92b2-105">當非工作區轉譯原則變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="a92b2-105">Sent when the non-client area rendering policy has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="a92b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="a92b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a92b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a92b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a92b2-108">指定是否針對視窗的非工作區啟用 DWM 轉譯。</span><span class="sxs-lookup"><span data-stu-id="a92b2-108">Specifies whether DWM rendering is enabled for the non-client area of the window.</span></span> <span data-ttu-id="a92b2-109">如果已啟用，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a92b2-109">**TRUE** if enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a92b2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a92b2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a92b2-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="a92b2-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a92b2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a92b2-112">Return value</span></span>

<span data-ttu-id="a92b2-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="a92b2-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a92b2-114">備註</span><span class="sxs-lookup"><span data-stu-id="a92b2-114">Remarks</span></span>

<span data-ttu-id="a92b2-115">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="a92b2-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="a92b2-116">[**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute)和 [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute)函數可用來取得或設定非用戶端轉譯原則。</span><span class="sxs-lookup"><span data-stu-id="a92b2-116">The [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions are used to get or set the non-client rendering policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="a92b2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a92b2-117">Requirements</span></span>



| <span data-ttu-id="a92b2-118">需求</span><span class="sxs-lookup"><span data-stu-id="a92b2-118">Requirement</span></span> | <span data-ttu-id="a92b2-119">值</span><span class="sxs-lookup"><span data-stu-id="a92b2-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a92b2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a92b2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a92b2-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a92b2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a92b2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a92b2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a92b2-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a92b2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a92b2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a92b2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a92b2-125"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="a92b2-125"><dt>Winuser.h</dt></span></span> </dl> |



 


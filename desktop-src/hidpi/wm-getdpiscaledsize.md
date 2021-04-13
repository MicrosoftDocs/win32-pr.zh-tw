---
title: 'WM_GETDPISCALEDSIZE 訊息 (Winuser .h) '
description: 這則訊息會告知作業系統，視窗將會調整大小為預設值以外的維度。
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE 訊息高 DPI
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465401"
---
# <a name="wm_getdpiscaledsize-message"></a><span data-ttu-id="76d91-104">WM \_ GETDPISCALEDSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="76d91-104">WM\_GETDPISCALEDSIZE message</span></span>

<span data-ttu-id="76d91-105">這則訊息會告知作業系統，視窗將會調整大小為預設值以外的維度。</span><span class="sxs-lookup"><span data-stu-id="76d91-105">This message tells the operating system that the window will be sized to dimensions other than the default.</span></span>

<span data-ttu-id="76d91-106">在傳送 [**WM \_ DPICHANGED**](wm-dpichanged.md)訊息之前，會將此訊息傳送至具有每個監視器 v2 [DPI \_ 感知 \_ 內容](dpi-awareness-context.md)的最上層視窗，並允許視窗計算其所需的大小以進行暫止的 DPI 變更。</span><span class="sxs-lookup"><span data-stu-id="76d91-106">This message is sent to top-level windows with a [DPI\_AWARENESS\_CONTEXT](dpi-awareness-context.md) of Per Monitor v2 before a [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent, and allows the window to compute its desired size for the pending DPI change.</span></span> <span data-ttu-id="76d91-107">因為線性 DPI 縮放比例是預設行為，所以這只適用于視窗想要以非線性方式調整的情節。</span><span class="sxs-lookup"><span data-stu-id="76d91-107">As linear DPI scaling is the default behavior, this is only useful in scenarios where the window wants to scale non-linearly.</span></span> <span data-ttu-id="76d91-108">如果應用程式回應此訊息，則產生的大小將會是傳送至 **WM \_ DPICHANGED** 的候選矩形。</span><span class="sxs-lookup"><span data-stu-id="76d91-108">If the application responds to this message, the resulting size will be the candidate rectangle send to **WM\_DPICHANGED**.</span></span>

<span data-ttu-id="76d91-109">您可以使用此訊息來改變以 [**WM \_ DPICHANGED**](wm-dpichanged.md)提供的矩形大小。</span><span class="sxs-lookup"><span data-stu-id="76d91-109">Use this message to alter the size of the rect that is provided with [**WM\_DPICHANGED**](wm-dpichanged.md).</span></span>


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a><span data-ttu-id="76d91-110">參數</span><span class="sxs-lookup"><span data-stu-id="76d91-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d91-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76d91-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76d91-112">WPARAM 包含 DPI 值。</span><span class="sxs-lookup"><span data-stu-id="76d91-112">The WPARAM contains a DPI value.</span></span> <span data-ttu-id="76d91-113">應用程式所設定的縮放視窗大小必須計算，就像視窗要切換到這個 DPI 一樣。</span><span class="sxs-lookup"><span data-stu-id="76d91-113">The scaled window size that the application would set needs to be computed as if the window were to switch to this DPI.</span></span>

</dd> <dt>

<span data-ttu-id="76d91-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76d91-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76d91-115">LPARAM 是大小結構的 in/out 指標。</span><span class="sxs-lookup"><span data-stu-id="76d91-115">The LPARAM is an in/out pointer to a SIZE struct.</span></span> <span data-ttu-id="76d91-116">\_LPARAM 中的 in \_ 值是使用者起始的移動或 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)呼叫之後的視窗暫止大小。</span><span class="sxs-lookup"><span data-stu-id="76d91-116">The \_In\_ value in the LPARAM is the pending size of the window after a user-initiated move or a call to [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="76d91-117">如果正在調整視窗的大小，此大小與接收此訊息時的視窗目前大小不一定相同。</span><span class="sxs-lookup"><span data-stu-id="76d91-117">If the window is being resized, this size is not necessarily the same as the window's current size at the time this message is received.</span></span>

<span data-ttu-id="76d91-118">\_ \_ 應用程式應將 LPARAM 中的 Out 值寫入至應用程式，以指定對應到 WPARAM 中所提供之 DPI 值的所需調整視窗大小。</span><span class="sxs-lookup"><span data-stu-id="76d91-118">The \_Out\_ value in the LPARAM should be written to by the application to specify the desired scaled window size corresponding to the provided DPI value in the WPARAM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d91-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="76d91-119">Return value</span></span>

<span data-ttu-id="76d91-120">函數會傳回 BOOL。</span><span class="sxs-lookup"><span data-stu-id="76d91-120">The function returns a BOOL.</span></span> <span data-ttu-id="76d91-121">傳回 TRUE 表示已計算新的大小。</span><span class="sxs-lookup"><span data-stu-id="76d91-121">Returning TRUE indicates that a new size has been computed.</span></span> <span data-ttu-id="76d91-122">傳回 FALSE 表示將不會處理訊息，而預設的線性 DPI 縮放比例將會套用至視窗。</span><span class="sxs-lookup"><span data-stu-id="76d91-122">Returning FALSE indicates that the message will not be handled, and the default linear DPI scaling will apply to the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="76d91-123">備註</span><span class="sxs-lookup"><span data-stu-id="76d91-123">Remarks</span></span>

<span data-ttu-id="76d91-124">此訊息只會傳送至具有每個監視器 v2 之 DPI 感知內容的最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="76d91-124">This message is only sent to top-level windows which have a DPI awareness context of Per Monitor v2.</span></span>

<span data-ttu-id="76d91-125">此事件是加速非線性調整的必要專案，可確保 windows 的位置在與游標之間的關聯性和跨監視器來回移動時保持不變。</span><span class="sxs-lookup"><span data-stu-id="76d91-125">This event is necessary to facilitate graceful non-linear scaling, and ensures that the windows's position remains constant in relationship to the cursor and when moving back and forth across monitors.</span></span>

<span data-ttu-id="76d91-126">此訊息在 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)中沒有特定的預設處理方式。</span><span class="sxs-lookup"><span data-stu-id="76d91-126">There is no specific default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="76d91-127">針對它未明確處理的所有訊息， [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) 會針對此訊息傳回零。</span><span class="sxs-lookup"><span data-stu-id="76d91-127">As for all messages it does not explicitly handle, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will return zero for this message.</span></span> <span data-ttu-id="76d91-128">如上面所述，此傳回會告知系統使用預設線性行為。</span><span class="sxs-lookup"><span data-stu-id="76d91-128">As noted above, this return tells the system to use the default linear behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="76d91-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="76d91-129">Requirements</span></span>



| <span data-ttu-id="76d91-130">需求</span><span class="sxs-lookup"><span data-stu-id="76d91-130">Requirement</span></span> | <span data-ttu-id="76d91-131">值</span><span class="sxs-lookup"><span data-stu-id="76d91-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76d91-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76d91-132">Minimum supported client</span></span><br/> | <span data-ttu-id="76d91-133">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76d91-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="76d91-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76d91-134">Minimum supported server</span></span><br/> | <span data-ttu-id="76d91-135">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76d91-135">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="76d91-136">標頭</span><span class="sxs-lookup"><span data-stu-id="76d91-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="76d91-137"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="76d91-137"><dt>Winuser.h</dt></span></span> </dl> |



 


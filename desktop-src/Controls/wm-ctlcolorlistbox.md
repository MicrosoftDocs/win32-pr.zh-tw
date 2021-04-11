---
title: 'WM_CTLCOLORLISTBOX 訊息 (Winuser .h) '
description: 在系統繪製清單方塊之前，傳送至清單方塊的父視窗。 藉由回應此訊息，父視窗可以使用指定的顯示裝置內容控制碼，來設定清單方塊的文字和背景色彩。
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- WM_CTLCOLORLISTBOX message Windows 控制項
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949af76bd05aa9ad3a3e720c89be33cfe76ed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094496"
---
# <a name="wm_ctlcolorlistbox-message"></a><span data-ttu-id="44605-105">WM \_ CTLCOLORLISTBOX 訊息</span><span class="sxs-lookup"><span data-stu-id="44605-105">WM\_CTLCOLORLISTBOX message</span></span>

<span data-ttu-id="44605-106">在系統繪製清單方塊之前，傳送至清單方塊的父視窗。</span><span class="sxs-lookup"><span data-stu-id="44605-106">Sent to the parent window of a list box before the system draws the list box.</span></span> <span data-ttu-id="44605-107">藉由回應此訊息，父視窗可以使用指定的顯示裝置內容控制碼，來設定清單方塊的文字和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="44605-107">By responding to this message, the parent window can set the text and background colors of the list box by using the specified display device context handle.</span></span>


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="44605-108">參數</span><span class="sxs-lookup"><span data-stu-id="44605-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44605-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44605-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44605-110">清單方塊的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="44605-110">Handle to the device context for the list box.</span></span>

</dd> <dt>

<span data-ttu-id="44605-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44605-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44605-112">清單方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="44605-112">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44605-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="44605-113">Return value</span></span>

<span data-ttu-id="44605-114">如果應用程式處理此訊息，則必須將控制碼傳回給筆刷。</span><span class="sxs-lookup"><span data-stu-id="44605-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="44605-115">系統會使用筆刷來繪製清單方塊的背景。</span><span class="sxs-lookup"><span data-stu-id="44605-115">The system uses the brush to paint the background of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="44605-116">備註</span><span class="sxs-lookup"><span data-stu-id="44605-116">Remarks</span></span>

<span data-ttu-id="44605-117">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取清單方塊的預設系統色彩。</span><span class="sxs-lookup"><span data-stu-id="44605-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the list box.</span></span>

<span data-ttu-id="44605-118">線上程之間永遠不會傳送 **WM \_ CTLCOLORLISTBOX** 訊息。</span><span class="sxs-lookup"><span data-stu-id="44605-118">The **WM\_CTLCOLORLISTBOX** message is never sent between threads.</span></span> <span data-ttu-id="44605-119">它只會在一個執行緒內傳送。</span><span class="sxs-lookup"><span data-stu-id="44605-119">It is sent only within one thread.</span></span>

<span data-ttu-id="44605-120">如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **INT \_ PTR** 並直接傳回值。</span><span class="sxs-lookup"><span data-stu-id="44605-120">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="44605-121">如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。</span><span class="sxs-lookup"><span data-stu-id="44605-121">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="44605-122">[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 **DWL \_ MSGRESULT** 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="44605-122">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="44605-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="44605-123">Requirements</span></span>



| <span data-ttu-id="44605-124">需求</span><span class="sxs-lookup"><span data-stu-id="44605-124">Requirement</span></span> | <span data-ttu-id="44605-125">值</span><span class="sxs-lookup"><span data-stu-id="44605-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44605-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44605-126">Minimum supported client</span></span><br/> | <span data-ttu-id="44605-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44605-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="44605-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44605-128">Minimum supported server</span></span><br/> | <span data-ttu-id="44605-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44605-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44605-130">標頭</span><span class="sxs-lookup"><span data-stu-id="44605-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="44605-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="44605-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44605-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44605-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="44605-133">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="44605-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="44605-134">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="44605-134">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="44605-135">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="44605-135">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="44605-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="44605-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 


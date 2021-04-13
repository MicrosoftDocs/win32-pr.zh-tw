---
title: 'WM_DWMSENDICONICLIVEPREVIEWBITMAP 訊息 (Dwmapi.dll .h) '
description: 指示視窗提供靜態點陣圖作為即時預覽 (也稱為該視窗的查看預覽) 。
ms.assetid: 24bf3b42-a850-4aa5-966a-29baab6b4d21
keywords:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP 訊息桌面視窗管理員
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICLIVEPREVIEWBITMAP
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f73076ab313da66171bc8265f7f4e7d068f93e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465497"
---
# <a name="wm_dwmsendiconiclivepreviewbitmap-message"></a><span data-ttu-id="fdce4-104">WM \_ DWMSENDICONICLIVEPREVIEWBITMAP 訊息</span><span class="sxs-lookup"><span data-stu-id="fdce4-104">WM\_DWMSENDICONICLIVEPREVIEWBITMAP message</span></span>

<span data-ttu-id="fdce4-105">指示視窗提供靜態點陣圖作為 *即時預覽* (也稱為該視窗的 *查看預覽*) 。</span><span class="sxs-lookup"><span data-stu-id="fdce4-105">Instructs a window to provide a static bitmap to use as a *live preview* (also known as a *Peek preview*) of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="fdce4-106">參數</span><span class="sxs-lookup"><span data-stu-id="fdce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdce4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdce4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdce4-108">未使用。</span><span class="sxs-lookup"><span data-stu-id="fdce4-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="fdce4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdce4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdce4-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="fdce4-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdce4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdce4-111">Return value</span></span>

<span data-ttu-id="fdce4-112">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="fdce4-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdce4-113">備註</span><span class="sxs-lookup"><span data-stu-id="fdce4-113">Remarks</span></span>

<span data-ttu-id="fdce4-114">當使用者將滑鼠指標移至工作列中視窗的縮圖上，或在 ALT + TAB 視窗中提供縮圖焦點時，會出現一個 *即時預覽* (也稱為 [ *查看預覽* ]) 。</span><span class="sxs-lookup"><span data-stu-id="fdce4-114">A *live preview* (also known as a *Peek preview*) of a window appears when a user moves the mouse pointer over the window's thumbnail in the taskbar or gives the thumbnail focus in the ALT+TAB window.</span></span> <span data-ttu-id="fdce4-115">此視圖是視窗的完整大小預覽，可以是即時快照或 iconic 標記法。</span><span class="sxs-lookup"><span data-stu-id="fdce4-115">This view is a full-sized preview of the window and can be a live snapshot or an iconic representation.</span></span>

<span data-ttu-id="fdce4-116">當下列所有情況都成立時，桌面視窗管理員 (DWM) 會將此訊息傳送至視窗：</span><span class="sxs-lookup"><span data-stu-id="fdce4-116">Desktop Window Manager (DWM) sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="fdce4-117">已在視窗上叫用即時預覽。</span><span class="sxs-lookup"><span data-stu-id="fdce4-117">Live preview has been invoked on the window.</span></span>
-   <span data-ttu-id="fdce4-118">DWMWA 已在視窗上設定 [**\_ \_ ICONIC \_ BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) 屬性。</span><span class="sxs-lookup"><span data-stu-id="fdce4-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="fdce4-119">Iconic 標記法是此視窗唯一存在的標記法。</span><span class="sxs-lookup"><span data-stu-id="fdce4-119">An iconic representation is the only one that exists for this window.</span></span>

<span data-ttu-id="fdce4-120">接收此訊息的視窗應該會產生完整縮放點陣圖以回應。</span><span class="sxs-lookup"><span data-stu-id="fdce4-120">The window that receives this message should respond by generating a full-scale bitmap.</span></span> <span data-ttu-id="fdce4-121">然後，此視窗會呼叫 [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) 函式來設定即時預覽。</span><span class="sxs-lookup"><span data-stu-id="fdce4-121">The window then calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function to set the live preview.</span></span> <span data-ttu-id="fdce4-122">如果視窗未在指定的時間內設定點陣圖，DWM 會針對視窗使用自己的預設 iconic 標記法。</span><span class="sxs-lookup"><span data-stu-id="fdce4-122">If the window does not set a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

## <a name="examples"></a><span data-ttu-id="fdce4-123">範例</span><span class="sxs-lookup"><span data-stu-id="fdce4-123">Examples</span></span>

<span data-ttu-id="fdce4-124">下列範例示範對 **WM \_ DWMSENDICONICLIVEPREVIEWBITMAP** 訊息的回應。</span><span class="sxs-lookup"><span data-stu-id="fdce4-124">The following example demonstrates a response to the **WM\_DWMSENDICONICLIVEPREVIEWBITMAP** message.</span></span> <span data-ttu-id="fdce4-125">此範例會使用自訂、裝置獨立點陣圖的控制碼來呼叫 [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) 函式，以作為視窗的標記法。</span><span class="sxs-lookup"><span data-stu-id="fdce4-125">The example calls the [**DwmSetIconicLivePreviewBitmap**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function with a handle to a customized, device-independent bitmap to use as the window's representation.</span></span>


```C++
        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="fdce4-126">如需完整的程式碼，請參閱 [自訂 Iconic 縮圖和即時預覽點陣圖](dwm-sample-customizethumbnail.md) 範例。</span><span class="sxs-lookup"><span data-stu-id="fdce4-126">For the complete code, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdce4-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdce4-127">Requirements</span></span>



| <span data-ttu-id="fdce4-128">需求</span><span class="sxs-lookup"><span data-stu-id="fdce4-128">Requirement</span></span> | <span data-ttu-id="fdce4-129">值</span><span class="sxs-lookup"><span data-stu-id="fdce4-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fdce4-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdce4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fdce4-131">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdce4-131">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fdce4-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdce4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fdce4-133">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdce4-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fdce4-134">標頭</span><span class="sxs-lookup"><span data-stu-id="fdce4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdce4-135"><dt>Dwmapi.dll。h</dt></span><span class="sxs-lookup"><span data-stu-id="fdce4-135"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdce4-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdce4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdce4-137">**WM \_ DWMSENDICONICTHUMBNAIL**</span><span class="sxs-lookup"><span data-stu-id="fdce4-137">**WM\_DWMSENDICONICTHUMBNAIL**</span></span>](wm-dwmsendiconicthumbnail.md)
</dt> <dt>

[<span data-ttu-id="fdce4-138">**DwmInvalidateIconicBitmaps**</span><span class="sxs-lookup"><span data-stu-id="fdce4-138">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> </dl>

 

 






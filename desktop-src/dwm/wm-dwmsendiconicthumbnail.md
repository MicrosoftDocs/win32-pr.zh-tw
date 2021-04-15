---
title: 'WM_DWMSENDICONICTHUMBNAIL 訊息 (Dwmapi.dll .h) '
description: 指示視窗提供靜態點陣圖，以用來做為該視窗的縮圖標記法。
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- WM_DWMSENDICONICTHUMBNAIL 訊息桌面視窗管理員
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466673"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a><span data-ttu-id="aaa67-104">WM \_ DWMSENDICONICTHUMBNAIL 訊息</span><span class="sxs-lookup"><span data-stu-id="aaa67-104">WM\_DWMSENDICONICTHUMBNAIL message</span></span>

<span data-ttu-id="aaa67-105">指示視窗提供靜態點陣圖，以用來做為該視窗的縮圖標記法。</span><span class="sxs-lookup"><span data-stu-id="aaa67-105">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="aaa67-106">參數</span><span class="sxs-lookup"><span data-stu-id="aaa67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaa67-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aaa67-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaa67-108">未使用。</span><span class="sxs-lookup"><span data-stu-id="aaa67-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="aaa67-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aaa67-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aaa67-110">此值的 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 是縮圖的最大 x 座標。</span><span class="sxs-lookup"><span data-stu-id="aaa67-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this value is the maximum x-coordinate of the thumbnail.</span></span> <span data-ttu-id="aaa67-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是最大的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="aaa67-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum y-coordinate.</span></span> <span data-ttu-id="aaa67-112">如果縮圖的維度超過其中一或兩個值，則 DWM 不接受縮圖。</span><span class="sxs-lookup"><span data-stu-id="aaa67-112">If a thumbnail has a dimension that exceeds one or both of these values, the DWM does not accept the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaa67-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="aaa67-113">Return value</span></span>

<span data-ttu-id="aaa67-114">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="aaa67-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaa67-115">備註</span><span class="sxs-lookup"><span data-stu-id="aaa67-115">Remarks</span></span>

<span data-ttu-id="aaa67-116">如果下列所有情況都成立，則 DWM 會將此訊息傳送至視窗：</span><span class="sxs-lookup"><span data-stu-id="aaa67-116">DWM sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="aaa67-117">DWM 會顯示視窗的 iconic 標記法。</span><span class="sxs-lookup"><span data-stu-id="aaa67-117">DWM is displaying an iconic representation of the window.</span></span>
-   <span data-ttu-id="aaa67-118">DWMWA 已在視窗上設定 [**\_ \_ ICONIC \_ BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) 屬性。</span><span class="sxs-lookup"><span data-stu-id="aaa67-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="aaa67-119">視窗未設定快取點陣圖。</span><span class="sxs-lookup"><span data-stu-id="aaa67-119">The window did not set a cached bitmap.</span></span>
-   <span data-ttu-id="aaa67-120">快取中有另一個點陣圖的空間。</span><span class="sxs-lookup"><span data-stu-id="aaa67-120">There is room in the cache for another bitmap.</span></span>

<span data-ttu-id="aaa67-121">接收此訊息的視窗應該會產生不超過訊息參數所要求大小的點陣圖，以回應。</span><span class="sxs-lookup"><span data-stu-id="aaa67-121">The window that receives this message should respond by generating a bitmap that is not larger than the size that is requested in the message parameters.</span></span> <span data-ttu-id="aaa67-122">然後，此視窗會呼叫 [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) 函式來覆寫預設的縮圖。</span><span class="sxs-lookup"><span data-stu-id="aaa67-122">The window then calls the [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function to override the default thumbnail.</span></span> <span data-ttu-id="aaa67-123">如果視窗未在指定的時間內提供點陣圖，DWM 會針對視窗使用自己的預設 iconic 標記法。</span><span class="sxs-lookup"><span data-stu-id="aaa67-123">If the window does not supply a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

<span data-ttu-id="aaa67-124">視窗必須屬於呼叫進程。</span><span class="sxs-lookup"><span data-stu-id="aaa67-124">The window must belong to the calling process.</span></span>

## <a name="examples"></a><span data-ttu-id="aaa67-125">範例</span><span class="sxs-lookup"><span data-stu-id="aaa67-125">Examples</span></span>

<span data-ttu-id="aaa67-126">下列程式碼範例顯示如何回應 **WM \_ DWMSENDICONICTHUMBNAIL** 訊息。</span><span class="sxs-lookup"><span data-stu-id="aaa67-126">The following code example shows how to respond to the **WM\_DWMSENDICONICTHUMBNAIL** message.</span></span> <span data-ttu-id="aaa67-127">此範例會使用自訂、裝置獨立點陣圖的控制碼來呼叫 [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail)，以做為 windows 的表示。</span><span class="sxs-lookup"><span data-stu-id="aaa67-127">The example calls [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), with a handle to a customized, device-indepedent bitmap to use as the windows' representation.</span></span>


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="aaa67-128">如需完整範例，請參閱 [自訂 Iconic 縮圖和即時預覽點陣圖](dwm-sample-customizethumbnail.md) 範例。</span><span class="sxs-lookup"><span data-stu-id="aaa67-128">For the complete example, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaa67-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="aaa67-129">Requirements</span></span>



| <span data-ttu-id="aaa67-130">需求</span><span class="sxs-lookup"><span data-stu-id="aaa67-130">Requirement</span></span> | <span data-ttu-id="aaa67-131">值</span><span class="sxs-lookup"><span data-stu-id="aaa67-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa67-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aaa67-132">Minimum supported client</span></span><br/> | <span data-ttu-id="aaa67-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aaa67-133">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aaa67-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aaa67-134">Minimum supported server</span></span><br/> | <span data-ttu-id="aaa67-135">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aaa67-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aaa67-136">標頭</span><span class="sxs-lookup"><span data-stu-id="aaa67-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaa67-137"><dt>Dwmapi.dll。h</dt></span><span class="sxs-lookup"><span data-stu-id="aaa67-137"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaa67-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aaa67-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaa67-139">**DwmInvalidateIconicBitmaps**</span><span class="sxs-lookup"><span data-stu-id="aaa67-139">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[<span data-ttu-id="aaa67-140">**WM \_ DWMSENDICONICLIVEPREVIEWBITMAP**</span><span class="sxs-lookup"><span data-stu-id="aaa67-140">**WM\_DWMSENDICONICLIVEPREVIEWBITMAP**</span></span>](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 


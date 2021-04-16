---
title: DWM 縮圖總覽
description: 桌面視窗管理員 (DWM) 可顯示應用程式視窗的縮圖表示。
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- 桌面視窗管理員 (DWM) 、縮圖
- DWM (桌面視窗管理員) 、縮圖
- 桌面視窗管理員 (DWM) 、縮圖關聯性
- DWM (桌面視窗管理員) 、縮圖關聯性
- 縮圖
- 縮圖關聯性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104571291"
---
# <a name="dwm-thumbnail-overview"></a><span data-ttu-id="446af-109">DWM 縮圖總覽</span><span class="sxs-lookup"><span data-stu-id="446af-109">DWM Thumbnail Overview</span></span>

<span data-ttu-id="446af-110">桌面視窗管理員 (DWM) 可顯示應用程式視窗的縮圖表示。</span><span class="sxs-lookup"><span data-stu-id="446af-110">Desktop Window Manager (DWM) enables the display of thumbnail representations of application windows.</span></span> <span data-ttu-id="446af-111">這些不是視窗的靜態快照集，而是縮圖來源視窗與接收即時縮圖轉譯之目的地視窗上的位置之間的動態、固定連接。</span><span class="sxs-lookup"><span data-stu-id="446af-111">These are not static snapshots of a window, but are instead dynamic, constant connections between a thumbnail source window and a location on a destination window that receives the live thumbnail rendering.</span></span> <span data-ttu-id="446af-112">這可讓您快速查看執行中的應用程式，方法是將滑鼠停留在工作列上的應用程式上，或使用 ALT 鍵的按鍵手勢來查看並快速切換至應用程式。</span><span class="sxs-lookup"><span data-stu-id="446af-112">This allows a quick view of running applications by hovering over the application on the taskbar or using the ALT-TAB key gesture to see and quickly switch to an application.</span></span>

<span data-ttu-id="446af-113">下圖說明當您將滑鼠停留在工作列上的應用程式上時，所看到的 Windows Vista 即時縮圖。</span><span class="sxs-lookup"><span data-stu-id="446af-113">The following image illustrates the Windows Vista live thumbnail seen when you hover over the application on the taskbar.</span></span>

![顯示將滑鼠停留在工作列上的應用程式上時，所看到的 D W 圖的螢幕擷取畫面。](images/dwm-livethumbnail.png)

<span data-ttu-id="446af-115">下圖說明 DWM 啟用的 Windows Vista 翻轉 (ALT-TAB) 。</span><span class="sxs-lookup"><span data-stu-id="446af-115">The following image illustrates the Windows Vista Flip (ALT-TAB) enabled by DWM.</span></span>

![啟用 dwm 的 alt 鍵的螢幕擷取畫面](images/dwm-flip.png)

> [!Note]  
> <span data-ttu-id="446af-117">DWM 縮圖不能讓開發人員建立像是 Windows Vista Flip3D (WINKEY]) 功能的應用程式。</span><span class="sxs-lookup"><span data-stu-id="446af-117">DWM thumbnails do not enable developers to create applications like the Windows Vista Flip3D (WINKEY-TAB) feature.</span></span> <span data-ttu-id="446af-118">縮圖會直接轉譯至2D 中的目的地視窗。</span><span class="sxs-lookup"><span data-stu-id="446af-118">Thumbnails are rendered directly to the destination window in 2-D.</span></span>

 

## <a name="dwm-thumbnail-relationships"></a><span data-ttu-id="446af-119">DWM 縮圖關聯性</span><span class="sxs-lookup"><span data-stu-id="446af-119">DWM Thumbnail Relationships</span></span>

<span data-ttu-id="446af-120">若要在您的應用程式中顯示縮圖，您必須先建立來源視窗與目的地視窗之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="446af-120">To display thumbnails in your application, you must first establish a relationship between a source window and a destination window.</span></span> <span data-ttu-id="446af-121">這是藉由呼叫 [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) 函數來完成。</span><span class="sxs-lookup"><span data-stu-id="446af-121">This is done by calling the [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) function.</span></span>

<span data-ttu-id="446af-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) 不會轉譯目的地視窗上的縮圖，而只會建立關聯性並提供縮圖控制碼。</span><span class="sxs-lookup"><span data-stu-id="446af-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) does not render a thumbnail on the destination window but merely creates the relationship and provides the thumbnail handle.</span></span> <span data-ttu-id="446af-123">在設定了 [**DWM \_ 縮圖 \_ 屬性**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) 並呼叫 [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) 函式之後，會轉譯縮圖。</span><span class="sxs-lookup"><span data-stu-id="446af-123">The thumbnail is rendered after the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) have been set and the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function has been called.</span></span> <span data-ttu-id="446af-124">後續的 **DwmUpdateThumbnailProperties** 呼叫會以一組新的屬性來更新縮圖。</span><span class="sxs-lookup"><span data-stu-id="446af-124">Subsequent calls to **DwmUpdateThumbnailProperties** update the thumbnail with a new set of properties.</span></span> <span data-ttu-id="446af-125">DWM 也提供 helper 函數 [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) ，以從縮圖取得來源視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="446af-125">The DWM also provides the helper function [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) to obtain the size of the source window from the thumbnail.</span></span>

<span data-ttu-id="446af-126">若要結束縮圖的關聯性，請呼叫 [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) 函數。</span><span class="sxs-lookup"><span data-stu-id="446af-126">To end a thumbnail relationship, call the [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) function.</span></span>

<span data-ttu-id="446af-127">下列範例示範如何使用 Windows 桌面建立 releationship，並將它顯示在應用程式中。</span><span class="sxs-lookup"><span data-stu-id="446af-127">The following example demonstrates how to create a releationship with the Windows desktop and display it in an application.</span></span>


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="446af-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="446af-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="446af-129">桌面視窗管理員概觀</span><span class="sxs-lookup"><span data-stu-id="446af-129">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="446af-130">Enable and Control DWM Composition (啟用並控制 DWM 組合)</span><span class="sxs-lookup"><span data-stu-id="446af-130">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="446af-131">效能考慮和最佳作法</span><span class="sxs-lookup"><span data-stu-id="446af-131">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 





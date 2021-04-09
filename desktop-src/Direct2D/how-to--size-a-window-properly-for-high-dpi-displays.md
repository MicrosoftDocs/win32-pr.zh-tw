---
title: 在高 DPI 顯示器上適當顯示
description: 描述如何建立在高 DPI 顯示器上適當顯示的視窗。
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b3e82951dfa77e6f61c661b87064dad5cb9f08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933521"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a><span data-ttu-id="9d48c-103">在高 DPI 顯示器上適當顯示</span><span class="sxs-lookup"><span data-stu-id="9d48c-103">Displaying properly on a high-DPI display</span></span>

<span data-ttu-id="9d48c-104">雖然 Direct2D 能為您解決許多高 DPI 問題，但您應該採取兩個步驟，以確保應用程式在高 DPI 顯示器上正常運作：</span><span class="sxs-lookup"><span data-stu-id="9d48c-104">Although Direct2D addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="9d48c-105">步驟1：建立 Windows 時使用系統 DPI</span><span class="sxs-lookup"><span data-stu-id="9d48c-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
-   [<span data-ttu-id="9d48c-106">步驟2：宣告應用程式為 DPI 感知</span><span class="sxs-lookup"><span data-stu-id="9d48c-106">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="9d48c-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="9d48c-107">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="9d48c-108">步驟1：建立 Windows 時使用系統 DPI</span><span class="sxs-lookup"><span data-stu-id="9d48c-108">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="9d48c-109">[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)介面提供用來取得系統 DPI 的 [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi)方法。</span><span class="sxs-lookup"><span data-stu-id="9d48c-109">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="9d48c-110">它會以每英寸的點（DPI)  (DPI）提供顯示的水準和垂直尺寸。</span><span class="sxs-lookup"><span data-stu-id="9d48c-110">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="9d48c-111">若要使用這些值來設定視窗的寬度，請使用下列公式：</span><span class="sxs-lookup"><span data-stu-id="9d48c-111">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="9d48c-112"><*水準* >  \* DPI  <*寬度*（以圖元為單位）>/<*預設水準 DPI*></span><span class="sxs-lookup"><span data-stu-id="9d48c-112"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="9d48c-113">...其中， *水準 DPI* 是 [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 所擷取的值，而 *預設的水準 DPI* 為96。</span><span class="sxs-lookup"><span data-stu-id="9d48c-113">...where *horizontal DPI* is the value retrived by [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="9d48c-114">公式類似于垂直大小：</span><span class="sxs-lookup"><span data-stu-id="9d48c-114">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="9d48c-115"><*垂直* >  \* DPI  <*高度*（以圖元為單位）>/<*預設垂直 DPI*></span><span class="sxs-lookup"><span data-stu-id="9d48c-115"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="9d48c-116">...其中， *垂直 DPI* 是 [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 方法所抓取的值，而 *預設的垂直 DPI* 為96。</span><span class="sxs-lookup"><span data-stu-id="9d48c-116">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="9d48c-117">下列程式碼會使用 [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 方法來取出系統 DPI，然後建立640×480視窗，並調整為系統 DPI。</span><span class="sxs-lookup"><span data-stu-id="9d48c-117">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to retrieve the system DPI and then creates a 640 × 480 window, scaled to the system DPI.</span></span>


```C++
        // Because the CreateWindow function takes its size in pixels,
        // obtain the system DPI and use it to scale the window size.
        FLOAT dpiX, dpiY;

        // The factory returns the current system DPI. This is also the value it will use
        // to create its own windows.
        m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


        // Create the window.
        m_hwnd = CreateWindow(
            L"D2DDemoApp",
            L"Direct2D Demo App",
            WS_OVERLAPPEDWINDOW,
            CW_USEDEFAULT,
            CW_USEDEFAULT,
            static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
            static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
            NULL,
            NULL,
            HINST_THISCOMPONENT,
            this
            );
```



> [!Note]
>
> <span data-ttu-id="9d48c-118">從 Windows 8 開始，您可以使用 [**Windows：： Graphics：:D isplay：:D isplayproperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) 類別來取得系統 DPI。</span><span class="sxs-lookup"><span data-stu-id="9d48c-118">Starting with Windows 8, you can use the [**Windows::Graphics::Display::DisplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) class to get the system DPI.</span></span>

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="9d48c-119">步驟2：宣告應用程式是 DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="9d48c-119">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="9d48c-120">當應用程式宣告本身為 DPI 感知時，它會指定應用程式在 DPI 設定上的運作方式，最高可達 200 DPI。</span><span class="sxs-lookup"><span data-stu-id="9d48c-120">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="9d48c-121">在 Windows Vista 和 Windows 7 中，啟用 DPI 虛擬化時，不會調整非 DPI 感知的應用程式，而應用程式會從系統 Api （例如 [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函式）接收虛擬化資料。</span><span class="sxs-lookup"><span data-stu-id="9d48c-121">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="9d48c-122">若要宣告您的應用程式為 DPI 感知，請完成下列步驟。</span><span class="sxs-lookup"><span data-stu-id="9d48c-122">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="9d48c-123">建立名為 DeclareDPIAware 的檔案。</span><span class="sxs-lookup"><span data-stu-id="9d48c-123">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="9d48c-124">將下列 xml 複製到檔案中，並加以儲存：</span><span class="sxs-lookup"><span data-stu-id="9d48c-124">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="9d48c-125">在專案的 vcproj 檔案中，于 VisualStudioProject/Configuration 下的每個設定元素內新增下列專案：</span><span class="sxs-lookup"><span data-stu-id="9d48c-125">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="9d48c-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="9d48c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d48c-127">Direct2D 和高 DPI</span><span class="sxs-lookup"><span data-stu-id="9d48c-127">Direct2D and High-DPI</span></span>](direct2d-and-high-dpi.md)
</dt> </dl>

 

 
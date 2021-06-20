---
title: '如何確保您的應用程式在高 DPI 顯示器上正確顯示 (DirectWrite) '
description: 描述如何確保您的應用程式建立在高 DPI 顯示器上正確顯示的視窗。
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71166d312fe666644c683fe2ece7dd3ced59f765
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406421"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a>如何確保您的應用程式在高 DPI 顯示器上正確顯示

雖然 [DirectWrite](direct-write-portal.md) 能為您解決許多高 DPI 問題，但您應該採取兩個步驟，以確保應用程式在高 DPI 顯示器上正常運作：

-   [步驟1：建立 Windows 時使用系統 DPI](#step-1-use-the-system-dpi-when-creating-windows)
    -   [Direct2D](#direct2d)
    -   [GDI](#gdi)
-   [步驟2：宣告應用程式為 DPI 感知](#step-2-declare-that-the-application-is-dpi-aware)
-   [相關主題](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>步驟1：建立 Windows 時使用系統 DPI

這可以透過使用 [Direct2D](../direct2d/direct2d-portal.md) 或使用 [GDI](../gdi/windows-gdi.md)來完成。

### <a name="direct2d"></a>Direct2D

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)介面提供用來取得系統 DPI 的 [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi)方法。 它會以每英寸的點（DPI)  (DPI）提供顯示的水準和垂直尺寸。 若要使用這些值來設定視窗的寬度，請使用下列公式：

<*水準* >  \* DPI  <*寬度*（以圖元為單位）>/<*預設水準 DPI*>

...其中， *水準 DPI* 是 GetDpi 所擷取的值，而 *預設的水準 DPI* 為96。 公式類似于垂直大小：

<*垂直* >  \* DPI  <*高度*（以圖元為單位）>/<*預設垂直 DPI*>

...其中， *垂直 DPI* 是 [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 方法所抓取的值，而 *預設的垂直 DPI* 為96。

下列程式碼會使用 [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 方法來建立 640 x 480 視窗，並調整為系統 DPI。  (在下列程式碼中， *m \_ SpD2DFactory* 是 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 實例的智慧型指標。 ) 


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



### <a name="gdi"></a>GDI

[GDI](interoperating-with-gdi.md) 提供用來抓取裝置資訊的 [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) 函式。 您可以藉由傳遞 *LOGPIXELSX* 和 *LOGPIXELSY* 索引值來取出 DPI 資訊。 判斷視窗水準和垂直大小的公式與上述的 [Direct2D](../direct2d/direct2d-portal.md) 範例相同。

下列程式碼會使用 [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) 函式來建立 640 x 480 視窗，並調整為系統 DPI。


```C++
FLOAT dpiX, dpiY;

HDC screen = GetDC(0);
dpiX = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSX));
dpiY = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSY));
ReleaseDC(0, screen);

hWnd = CreateWindow(
         TEXT("DirectWriteApp"),
         TEXT("DirectWrite Demo App"),
         WS_OVERLAPPEDWINDOW,
         CW_USEDEFAULT,
         CW_USEDEFAULT,
         static_cast<INT>(dpiX * 640.f / 96.f),
         static_cast<INT>(dpiY * 480.f / 96.f),
         NULL,
         NULL,
         hInstance,
         NULL
         );
```



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>步驟2：宣告應用程式是 DPI-Aware

當應用程式宣告本身為 DPI 感知時，它會指定應用程式在 DPI 設定上的運作方式，最高可達 200 DPI。 在 Windows Vista 和 Windows 7 中，啟用 DPI 虛擬化時，不會調整非 DPI 感知的應用程式，而應用程式會從系統 Api （例如 [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) 函式）接收虛擬化資料。 若要宣告您的應用程式為 DPI 感知，請完成下列步驟。

1.  建立名為 DeclareDPIAware 的檔案。
2.  將下列 xml 複製到檔案中，並加以儲存：
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  在專案的 vcproj 檔案中，于 VisualStudioProject/Configuration 下的每個設定元素內新增下列專案：
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 和高 DPI](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 
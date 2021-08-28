---
title: 在高 DPI 顯示器上適當顯示
description: 描述為應用程式建立可在高 DPI 顯示器上正確顯示之視窗的步驟。
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d8ebc6a7621623307d9b2cfd953a5fa3f3387fbacb3faeb345375d925044cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259958"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a>在高 DPI 顯示器上適當顯示

雖然 Direct2D 能為您解決許多高 DPI 問題，但您應該採取兩個步驟，以確保應用程式在高 DPI 顯示器上正常運作：

-   [步驟1：建立 Windows 時使用系統 DPI](#step-1-use-the-system-dpi-when-creating-windows)
-   [步驟2：宣告應用程式為 DPI 感知](#step-2-declare-that-the-application-is-dpi-aware)
-   [相關主題](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>步驟1：建立 Windows 時使用系統 DPI

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)介面提供用來取得系統 DPI 的 [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi)方法。 它會以每英寸的點（DPI)  (DPI）提供顯示的水準和垂直尺寸。 若要使用這些值來設定視窗的寬度，請使用下列公式：

<*水準* >  \* DPI  <*寬度*（以圖元為單位）>/<*預設水準 DPI*>

...其中， *水準 DPI* 是 [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 所擷取的值，而 *預設的水準 DPI* 為96。 公式類似于垂直大小：

<*垂直* >  \* DPI  <*高度*（以圖元為單位）>/<*預設垂直 DPI*>

...其中， *垂直 DPI* 是 [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 方法所抓取的值，而 *預設的垂直 DPI* 為96。

下列程式碼會使用 [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) 方法來取出系統 DPI，然後建立640×480視窗，並調整為系統 DPI。


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
> 從 Windows 8 開始，您可以使用 [**Windows：： Graphics：:D isplay：:D isplayproperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties)類別來取得系統 DPI。

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>步驟2：宣告應用程式是 DPI-Aware

當應用程式宣告本身為 DPI 感知時，它會指定應用程式在 DPI 設定上的運作方式，最高可達 200 DPI。 在 Windows Vista 和 Windows 7 中，啟用 DPI 虛擬化時，不會調整非 DPI 感知的應用程式，而應用程式會從系統 api （例如 [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)函式）接收虛擬化資料。 若要宣告您的應用程式為 DPI 感知，請完成下列步驟。

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

[Direct2D 和高 DPI](direct2d-and-high-dpi.md)
</dt> </dl>

 

 
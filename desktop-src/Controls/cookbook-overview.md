---
title: 啟用視覺化樣式
description: 本主題說明如何設定您的應用程式，以確保通用控制項會顯示在使用者的慣用視覺效果樣式中。
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39339c0535767011a59730534486604389f62468
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933678"
---
# <a name="enabling-visual-styles"></a>啟用視覺化樣式

本主題說明如何設定您的應用程式，以確保通用控制項會顯示在使用者的慣用視覺效果樣式中。

本主題包含下列各節。

-   [使用資訊清單或指示詞，以確保視覺效果樣式可以套用至應用程式](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [在只使用標準延伸模組的應用程式中使用 ComCtl32.dll 第6版](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [在主控台中使用 Comctl32.dll 第6版或 RunDll32.exe執行的 DLL ](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [將視覺化樣式支援新增至延伸模組、外掛程式、MMC 嵌入式管理單元或進入進程的 DLL](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [關閉視覺化樣式](#turning-off-visual-styles)
-   [使用視覺效果樣式搭配 HTML 內容](#using-visual-styles-with-html-content)
-   [未套用視覺化樣式時](#when-visual-styles-are-not-applied)
-   [讓您的應用程式與舊版 Windows 相容](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [相關主題](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a>使用資訊清單或指示詞，以確保視覺效果樣式可以套用至應用程式

若要讓您的應用程式使用視覺化樣式，您必須使用 ComCtl32.dll 6 版或更新版本。 因為第6版無法轉散發套件，只有當您的應用程式是在包含它的 Windows 版本上執行時才可使用。 Windows 隨附第5版和第6版。 ComCtl32.dll 第6版包含使用者控制項和通用控制項。 根據預設，應用程式會使用 User32.dll 中定義的使用者控制項，以及 ComCtl32.dll 第5版中所定義的通用控制項。 如需 DLL 版本及其散發平臺清單，請參閱 [通用控制項版本](common-control-versions.md)。

如果您想要讓應用程式使用視覺化樣式，則必須加入應用程式資訊清單或編譯器指示詞，指出如果有的話，應使用 ComCtl32.dll 第6版。

應用程式資訊清單可讓應用程式指定所需的元件版本。 在 Microsoft Win32 中，元件是一組 Dll 以及這些 Dll 中包含的可擴充區分版本物件清單。

資訊清單是以 XML 撰寫的。 應用程式資訊清單檔的名稱是可執行檔的名稱，後面接著副檔名 .manifest;例如 MyApp.exe 的資訊清單。 下列範例資訊清單顯示第一個區段描述資訊清單本身。 下表顯示 [資訊清單描述] 區段中 **assemblyIdentity** 元素所設定的屬性。



| 屬性             | 描述                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| version               | 資訊清單的版本。 版本的格式必須是 (主要的.. n n n n. n n n n. n n n n. n n n <= 65535) 。 |
| processorArchitecture | 開發應用程式的處理器。                                                                          |
| NAME                  | 包括公司名稱、產品名稱和應用程式名稱。                                                                   |
| 類型                  | 應用程式的類型，例如 Win32。                                                                                    |



 

範例資訊清單也會提供應用程式的描述，並指定應用程式相依性。 下表顯示 [相依性] 區段中 **assemblyIdentity** 元素所設定的屬性。



| 屬性             | 描述                                      |
|-----------------------|--------------------------------------------------|
| type                  | 相依性元件的類型，例如 Win32。 |
| NAME                  | 元件的名稱。                           |
| version               | 元件的版本。                        |
| processorArchitecture | 設計元件的處理器。    |
| publicKeyToken        | 與此元件搭配使用的金鑰 token。              |
| 語言              | 元件的語言。                       |



 

以下是資訊清單檔案的範例。

> [!IMPORTANT]
> 如果您的應用程式是以32位 Windows 平臺為目標，請將 **processorArchitecture** 專案設定為 **"X86"** ，如果您的應用程式是以64位 windows 平臺為目標，則設定為 **"amd64"** 。 您也可以指定 **" \* "**，以確保所有平臺皆為目標，如下列範例所示。

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



如果您使用 Microsoft Visual C++ 2005 或更新版本，您可以將下列編譯器指示詞新增至您的原始程式碼，而不是以手動方式建立資訊清單。 為了方便閱讀，此指示詞分成數行。


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



下列主題描述將視覺效果樣式套用至不同應用程式類型的步驟。 請注意，資訊清單格式在每個案例中都相同。

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a>在只使用標準延伸模組的應用程式中使用 ComCtl32.dll 第6版

以下是未使用協力廠商擴充功能的應用程式範例。

-   Calculator
-   新接龍
-   踩地雷
-   [記事本]
-   接龍

**建立資訊清單，並讓您的應用程式使用視覺化樣式。**

1.  連結至 Comctl32.dll .lib 並呼叫 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)。
2.  將名為 YourApp.exe 的檔案新增至具有 XML 資訊清單格式的來源樹狀結構。
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  將資訊清單新增至您應用程式的資源檔，如下所示：
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > 當您將前一個專案加入至資源時，您必須將它格式化為一行。 或者，您可以將 XML 資訊清單檔案放在與應用程式可執行檔相同的目錄中。 作業系統會先從檔案系統載入資訊清單，然後檢查可執行檔的資源區段。 檔案系統版本優先。

     

當您建立應用程式時，資訊清單會新增為二進位資源。

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a>在主控台中使用 Comctl32.dll 第6版或 RunDll32.exe 執行的 DLL

**建立資訊清單，並讓您的應用程式使用視覺化樣式。**

1.  連結至 Comctl32.dll .lib 並呼叫 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)。
2.  將名為 YourApp.cpl 的檔案新增至具有 XML 資訊清單格式的來源樹狀結構。
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  將資訊清單新增至您應用程式的資源檔，作為資源識別碼123。

> [!Note]  
> 當您撰寫主控台的應用程式時，請將它放在適當的類別中。 主控台現在支援主控台應用程式的分類。 這表示主控台的應用程式可以被指派識別碼，並區分為工作區域，例如新增或移除程式、外觀和主題，或日期、時間、語言和地區選項。

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a>將視覺化樣式支援新增至延伸模組、外掛程式、MMC 嵌入式管理單元或進入進程的 DLL

視覺化樣式的支援可新增至延伸模組、外掛程式、MMC 嵌入式管理單元，或進入進程的 DLL。 例如，使用下列步驟來新增 Microsoft Management Console (MMC) 嵌入式管理單元的視覺化樣式支援。

1.  使用-DISOLATION 感知啟用旗標編譯您的嵌入式管理單元， \_ \_ 或在 \# 包含 "windows .h" 語句之前插入下列語句。

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    如需啟用隔離感知的詳細資訊 \_ \_ ，請參閱 [隔離元件](/windows/desktop/SbsCs/isolating-components)。

2.  在嵌入式管理單元來源中包含通用控制標頭檔。
    ```C++
    #include <commctrl.h>
    ```

    

3.  將名為 YourApp 的檔案新增至使用 XML 資訊清單格式的來源樹狀結構。
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  將資訊清單新增至嵌入式管理單元的資源檔。 如需將資訊清單新增至資源檔的詳細資訊，請參閱 [在使用延伸模組、外掛程式或 DLL 的應用程式中使用 comctl32.dll 第6版](/previous-versions//ms649781(v=vs.85)) 。

## <a name="turning-off-visual-styles"></a>關閉視覺化樣式

您可以藉由呼叫 [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) 函式來關閉控制項或視窗中所有控制項的視覺化樣式，如下所示：


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



在上述範例中， *hwnd* 是停用視覺化樣式的視窗控制碼。 在呼叫之後，控制項不會呈現視覺化樣式。

## <a name="using-visual-styles-with-html-content"></a>使用視覺效果樣式搭配 HTML 內容

修改階層式樣式表 (CSS) 屬性（例如背景或框線）的 HTML 頁面未套用視覺效果樣式。 它們會顯示指定的 CSS 屬性。 當指定為內容的一部分時，大部分的 CSS 屬性會套用至已套用視覺化樣式的元素。

根據預設，視覺效果樣式會套用至 Microsoft Internet Explorer 6 和更新版本中所顯示頁面上的內部 HTML 控制項。 若要關閉 HTML 網頁的視覺化樣式，請將中繼標記新增至 <head> ＞一節探討各類型資料來源的重新整理。 這項技術也適用于封裝為 HTML 應用程式 (Hta) 的內容。 若要關閉視覺化樣式，中繼標記必須如下所示：


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> 如果瀏覽器設定和標記設定不一致，則頁面不會套用視覺化樣式。 例如，如果中繼標籤設定為 [否]，而瀏覽器設定為啟用視覺化樣式，則視覺效果樣式不會套用至頁面。 但是，如果瀏覽器或中繼標籤設定為 [是]，而未指定其他專案，則會套用視覺化樣式。

 

視覺化樣式可能會變更內容的版面配置。 此外，如果您在內部 HTML 控制項（例如按鈕的寬度）上設定某些屬性，您可能會發現按鈕上的標籤在某些視覺效果樣式下無法閱讀。

您必須使用視覺化樣式來徹底測試您的內容，以判斷套用視覺效果樣式對您的內容和配置是否有負面影響。

## <a name="when-visual-styles-are-not-applied"></a>未套用視覺化樣式時

若要避免將視覺效果樣式套用至最上層視窗，請為視窗提供非 null 區域 (**SetWindowRgn**) 。 系統會假設具有非 Null 區域的視窗是未使用視覺化樣式的特製化視窗。 與非視覺效果樣式的最上層視窗相關聯的子視窗仍可能套用視覺化樣式，即使父視窗沒有。

如果您想要停用應用程式中所有視窗的視覺化樣式，請呼叫 [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) ，不要通過 STAP \_ 允許非工作區 \_ 旗標。 如果應用程式未呼叫 **SetThemeAppProperties**，則假設的旗標值為 STAP \_ 允許非工作 \_ \| STAP \_ 允許 \_ 控制項 \| STAP \_ 允許 \_ WEBCONTENT。 假設的值會使非工作區、控制項和 web 內容套用視覺化樣式。

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a>讓您的應用程式與舊版 Windows 相容

許多視覺化樣式架構的設計目的，是為了讓您在不支援變更控制面板的舊版 Windows 上繼續交付您的產品。 當您為一個以上的作業系統傳送應用程式時，請注意下列事項：

-   在 Windows 8 之前的 Windows 版本中，當高對比開啟時，視覺化樣式會關閉。 為了支援高對比，支援視覺效果樣式的繼承應用程式必須提供個別的程式碼路徑，才能適當地以高對比繪製 UI 元素。 在 Windows 8 中，高對比是視覺化樣式的一部分;不過，Windows 8 的應用程式 (其中一個應用程式資訊清單的 [相容性] 區段中包含 Windows 8 GUID) 仍然需要提供個別的程式碼路徑，以便在先前的 Windows 7 上正確呈現。
-   如果您使用 ComCtl32.dll 第6版中的功能（例如圖格視圖或連結控制項），就必須處理使用者電腦上無法使用這些控制項的情況。 ComCtl32.dll 第6版無法轉散發。
-   測試您的應用程式，以確定您未先檢查目前的版本，而不依賴 ComCtl32.dll 版本6的功能。
-   請勿連結至 UxTheme .lib。
-   當視覺效果樣式未如預期般運作時，為實例撰寫錯誤處理常式代碼。
-   在較舊版本中安裝應用程式的資訊清單不會影響控制項的呈現。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[視覺化樣式](themes-overview.md)
</dt> </dl>

 

 
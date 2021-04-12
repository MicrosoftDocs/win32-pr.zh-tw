---
title: 建立功能區應用程式
description: Windows 功能區架構是由兩個不同但相依的開發平臺所組成，以 Extensible Application Markup Language (XAML) 來宣告控制項和其視覺化配置，以及 c + + 元件物件模型 (COM) 型介面集，以定義命令功能和應用程式攔截。 在功能區架構架構中的這一項工作，需要使用架構所提供之豐富 UI 功能的開發人員，必須設計和描述標記中的 UI，然後使用功能區架構 COM 介面將架構連接到主應用程式。
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Windows 功能區，建立應用程式
- 功能區，建立應用程式
- Windows 功能區，藍圖
- 功能區，藍圖
- Windows 功能區，標記
- 功能區，標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376161"
---
# <a name="creating-a-ribbon-application"></a>建立功能區應用程式

Windows 功能區架構是由兩個不同但相依的開發平臺所組成：根據 Extensible Application Markup Language 的標記語言 (XAML) 來宣告控制項及其視覺配置，以及 c + + 元件物件模型 (COM) 型介面集，以定義命令功能和應用程式勾點。 在功能區架構架構中的這一項工作，需要使用架構所提供之豐富 UI 功能的開發人員，必須設計和描述標記中的 UI，然後使用功能區架構 COM 介面將架構連接到主應用程式。

-   [功能區藍圖](#ribbon-roadmap)
-   [寫入標記](#write-the-markup)
    -   [編譯標記](#compile-the-markup)
-   [建立應用程式](#build-the-application)
    -   [初始化功能區](#initialize-the-ribbon)
    -   [將標記連結至應用程式](#link-the-markup-to-the-application)
    -   [編譯應用程式](#link-the-markup-to-the-application)
-   [執行時間更新和執行次數](#run-time-updates-and-executions)
-   [OLE 支援](#ole-support)
-   [相關主題](#related-topics)

## <a name="ribbon-roadmap"></a>功能區藍圖

功能區應用程式的視覺效果（例如顯示的控制項和放置的位置）會在標記中宣告 (請參閱 [使用功能區標記宣告命令和控制項](windowsribbon-schema.md)) 。 應用程式命令邏輯（例如按下按鈕時所發生的動作）會在程式碼中執行。

執行功能區並將其併入 Windows 應用程式的程式需要四個基本工作：寫入標記、編譯標記、撰寫程式碼，以及編譯和連結整個應用程式。

下圖說明一般功能區執行的工作流程。

![顯示一般功能區執行工作流程的圖表。](images/overviews/ribbonroadmap.png)

下列各節將更詳細地說明此程式。

## <a name="write-the-markup"></a>寫入標記

設計功能區 UI 之後，應用程式開發人員的第一個工作就是使用功能區標記來描述 UI。

> [!IMPORTANT]
> 功能區架構標記架構檔案（UICC .xsd）是與適用于 Windows 7 和 .NET Framework 4.0 的 Microsoft Windows 軟體開發套件 (SDK) 一併安裝。 使用標準安裝路徑時，檔案位於% ProgramFiles% \\ Microsoft sdk \\ Windows \\ \[ 版本號碼 Bin 資料夾中， \] \\ 可供許多 XML 編輯器參考，以提供提示和自動完成。

 

功能區控制項、功能區命令 (控制項獨立的元素，這些專案會提供功能區控制項) 的基本功能，而且所有控制項版面配置和視覺關聯性都會在標記中宣告。 功能區標記的結構強調功能區控制項和命令與兩個主要節點階層之間的差異： [命令和資源](windowsribbon-reference-elements-command.md) 樹狀結構，以及 [視圖](windowsribbon-reference-elements-view.md) 樹狀結構。

功能區公開的所有容器和動作都會在 [ [命令和資源](windowsribbon-reference-elements-command.md) ] 樹狀結構中宣告。 每個命令專案都會與 UI 設計所需的一組資源相關聯。

建立應用程式的命令之後，您可以在 [ [Views](windowsribbon-reference-elements-view.md) ] 樹狀結構中宣告控制項，然後將每個控制項系結至命令以公開命令功能。 功能區架構會根據此處所宣告的控制項階層，判斷控制項的實際位置。

下列程式碼範例說明如何宣告按鈕控制項、標示為 Exit 應用程式，並將它與 Exit 命令相關聯。


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> 雖然您可以針對功能區標記檔案使用任何副檔名，但在檔中使用的是建議的副檔名。

 

### <a name="compile-the-markup"></a>編譯標記

建立功能區標記檔案之後，必須將它編譯成二進位格式，方法是使用 Windows 軟體發展工具組 (SDK) 隨附的功能區標記編譯器、UI 命令編譯器 (UICC) 。 主機應用程式在功能區架構初始化期間，會將這個二進位檔案的參考傳遞給 [**IUIFramework：： LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) 方法。

UICC 可以直接從命令列視窗執行，或新增為 Visual Studio 中的「自訂群組建步驟」。

下圖顯示 Windows 7 SDK CMD Shell 視窗中的 UICC 標記編譯器。

![在命令列視窗中顯示 uicc.exe 的螢幕擷取畫面。](images/overviews/screenshot-intentcl-commandline.png)

下圖顯示在 Visual Studio 中新增為自訂群組建步驟的 UICC。

![顯示在 visual studio 中新增為自訂群組建步驟 uicc.exe 的螢幕擷取畫面。](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

UICC 會產生三個檔案：標記的二進位版本 (. bml) 、識別碼定義標頭 ( .h 檔) 將標記專案公開給功能區主應用程式，以及 ( .rc 檔的 [資源定義腳本](../menurc/about-resource-files.md) ，) 在編譯時期將功能區影像和字串資源連結至主應用程式。

如需編譯功能區架構標記的詳細資訊，請參閱 [編譯功能區標記](windowsribbon-intentcl.md)。

## <a name="build-the-application"></a>建置應用程式

功能區應用程式的初步 UI 在標記中設計和實行之後，必須撰寫程式碼來初始化架構、取用標記，然後將標記中宣告的命令系結至應用程式中適當的命令處理常式。

> [!IMPORTANT]
>
> 由於功能區架構是以 COM 為基礎，建議功能區專案使用 \_ \_ uuidof () 運算子來參考功能區架構介面 (iid) 的 guid。 在無法使用 uuidof () 運算子的情況下（ \_ \_ 例如使用非 Microsoft 編譯器或主應用程式是以 C 為基礎的應用程式），iid 必須由應用程式定義，因為它們不包含在 uuid 中。
>
> 如果 Iid 是由應用程式定義，則必須使用 UIRibbon 中指定的 Guid。
>
> UIRibbon 隨附于 [Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windows/bb980924.aspx) 的一部分，可在% ProgramFiles% \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 包含的標準安裝路徑中找到。

 

### <a name="initialize-the-ribbon"></a>初始化功能區

下圖說明執行簡單功能區應用程式所需的步驟。

![此圖顯示執行簡單功能區執行所需的步驟。](images/overviews/initializationsteps.png)

下列步驟詳細說明如何執行簡單的功能區應用程式。

1.  CoCreateInstance

    應用程式會使用功能區架構類別識別碼來呼叫標準 COM CoCreateInstance 函數，以取得架構的指標。

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  Initialize (hwnd，IUIApplication \*) 

    應用程式會呼叫 [**IUIFramework：： Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize)，傳遞兩個參數：最上層視窗的控制碼，其中將包含功能區和可讓架構對應用程式進行回呼的 [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) 實作為指標。

    > \[!重要\]  
    > 功能區架構會初始化為單一執行緒的單元 (STA) 。

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  LoadUI (實例，CoNtext.resourcename) 

    應用程式會呼叫 [**IUIFramework：： LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) 來系結標記資源。 此函數的第一個參數是功能區應用程式實例的控制碼。 第二個參數是先前編譯之二進位標記資源的名稱。 藉由將二進位標記傳遞給功能區架構，應用程式就會通知功能區結構應該是什麼，以及控制項的相片順序。 它也會提供架構資訊清單，以公開 (（例如貼上、剪下、尋找) ），當架構在執行時間進行與命令相關的回呼時，就會使用這些資訊清單。

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  [**IUIApplication：： OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) 回呼

    完成步驟1到3之後，功能區架構會知道要在功能區中公開哪些命令。 不過，在功能區完全正常運作之前，架構仍然需要兩件事：在執行命令時告訴應用程式，以及在執行時間取得命令資源或屬性的方式。 例如，如果下拉式方塊會出現在 UI 中，則架構必須要求要用來填入下拉式方塊的專案。

    這兩項功能是透過 [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) 介面處理。 具體來說，針對二進位標記中宣告的每個命令 (查看上述) 的步驟3，架構會呼叫 [**IUIApplication：： OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) ，向應用程式要求該命令的 **IUICommandHandler** 物件。

    > [!Note]  
    > [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)介面允許將命令處理常式系結至一或多個命令。

     

若要執行 [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) 方法 stub （可傳回 E >notimpl），至少需要應用程式， \_ 如下列範例所示。


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a>將標記連結至應用程式

此時，標記資源檔必須連結至主應用程式，方法是包含對標記資源定義檔的參考， (其中包含應用程式資源檔中) 標記標頭檔的參考。 例如，名為 RibbonApp 的應用程式與名為 ribbonUI 的資源檔，需要 RibbonApp .rc 檔中的下列程式列。


```C++
#include "ribbonUI.rc"
```



根據所使用的編譯器和連結器，資源定義腳本可能也需要編譯，才能編譯功能區應用程式。 [資源編譯器 (RC) ](../menurc/using-rc-the-rc-command-line-.md)命令列工具隨附 Microsoft Visual Studio 和 Windows SDK 可用於這項工作。

### <a name="compile-the-application"></a>編譯應用程式

功能區應用程式一經編譯，就可以執行並測試 UI。 如果 UI 需要調整，而且在核心應用程式程式碼中沒有任何相關聯的命令處理常式變更，請修改標記原始程式檔、使用 UICC.exe 重新編譯標記，然後連結新的標記資源檔。 當應用程式重新開機時，就會顯示修改過的 UI。

這一切都可以在不觸及核心應用程式程式碼的情況下使用，這是比標準應用程式開發和散發更大的改進。

## <a name="run-time-updates-and-executions"></a>執行時間更新和執行次數

功能區架構的執行時間通訊結構是以推送和提取或雙向呼叫端（model）為基礎。

此模型可讓架構在執行命令時通知應用程式，並允許架構和應用程式查詢、更新和使屬性值和功能區資源失效。 這項功能是透過一些介面和方法提供。

架構會透過 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 回呼方法，從功能區應用程式提取更新的屬性資訊。 命令識別碼和屬性索引鍵（可識別要更新的命令屬性）會傳遞至方法，該方法會將該屬性索引鍵的值傳回或推送至架構。

當執行命令時，架構會呼叫 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) ，同時識別命令識別碼和發生 ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)) 的執行類型。 這是應用程式為命令指定執行邏輯的位置。

下圖說明在架構和應用程式之間執行命令的執行時間通訊。

![此圖顯示功能區架構與主應用程式之間的執行時間通訊範例。](images/overviews/updatesandexecutions.png)

> [!Note]  
> 最初在應用程式中顯示功能區時，不需要執行 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 和 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 函式。 不過，若要確保應用程式在使用者執行命令時正確運作，就必須使用這些方法。

 

## <a name="ole-support"></a>OLE 支援

功能區應用程式可以設定為 OLE 伺服器，以支援就地 OLE 啟用。

在 OLE 伺服器應用程式中建立的物件會在插入 (貼上或放置) 至 OLE 用戶端應用程式 (或容器) 時，維持與伺服器應用程式的關聯。 在就地 OLE 啟用中，按兩下用戶端應用程式中的物件會開啟伺服器應用程式的專用實例，並載入物件進行編輯。 當伺服器應用程式關閉時，對物件所做的所有變更都會反映在用戶端應用程式中。

> [!Note]  
> 功能區架構不支援就地 OLE 啟用。 在以功能區為基礎的 OLE 伺服器中建立的物件，無法從 OLE 用戶端應用程式中進行編輯。 需要伺服器應用程式的外部專用實例。


## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用功能區標記宣告命令和控制項](./windowsribbon-schema.md)
</dt> <dt>

[功能區使用者體驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[功能區設計流程](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 





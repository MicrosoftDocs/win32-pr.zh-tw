---
title: 遷移至 Windows 功能區架構
description: 依賴傳統功能表、工具列和對話方塊的應用程式可以遷移至 Windows 功能區架構命令系統的豐富、動態和內容導向的 UI。
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Windows功能區，遷移至
- 功能區，遷移至
- 遷移至 Windows 功能區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a011e9b5dad52f6f71fab272f0fded39ec59eb71cc7311ab9cf5ffccb4dfbca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841118"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a>遷移至 Windows 功能區架構

依賴傳統功能表、工具列和對話方塊的應用程式可以遷移至 Windows 功能區架構命令系統的豐富、動態和內容導向的 UI。 這是將應用程式現代化和讓起死回生的簡單且有效的方式，同時也改善了其功能的協助工具、可用性及可探索性。

## <a name="introduction"></a>簡介

一般情況下，將現有的應用程式遷移至功能區架構包含下列各項：

-   設計功能區配置和控制組織來公開現有應用程式的功能，並有足夠的彈性可支援新的功能。
-   調整現有應用程式的程式碼。
-   將現有的應用程式資源遷移 (的字串和影像) 至功能區架構。

> [!Note]  
> 應檢查 [功能區使用者經驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx) ，以判斷應用程式是否適合功能區 UI。

 

## <a name="design-the-ribbon-layout"></a>設計功能區版面配置

您可以藉由執行下列步驟來識別可能的功能區 UI 設計和控制項版面配置：

1.  取得所有現有功能的清查。
2.  將此功能轉譯成功能區命令。
3.  將命令組織成邏輯群組。

### <a name="take-inventory"></a>進行清查

在功能區架構中，操作工作區或檔之狀態的應用程式所公開的功能會被視為命令。 什麼構成命令可能會有所不同，並取決於現有應用程式的本質和網域。

下表列出假設文字編輯應用程式的一組基本命令：



| 符號           | ID     | 描述               |
|------------------|--------|---------------------------|
| 新增識別碼檔案 \_ \_    | 0xE100 | 新檔              |
| 儲存識別碼檔案 \_ \_   | 0xE103 | 儲存檔             |
| 識別碼檔案的 \_ \_ SAVEAS | 0xE104 | 另存新檔 .。。 (對話方塊)        |
| 識別碼 \_ 檔案 \_ 開啟   | 0xE101 | 開啟 ... (] 對話方塊)           |
| 識別碼 \_ 檔案 \_ 結束   | 0xE102 | 結束應用程式      |
| 識別碼 \_ 編輯 \_ 復原   | 0xE12B | 復原                      |
| 識別碼 \_ 編輯 \_ 剪下    | 0xE123 | 剪下選取的文字         |
| 識別碼 \_ 編輯 \_ 複本   | 0xE122 | 複製選取的文字        |
| 識別碼 \_ 編輯 \_ 貼上  | 0xE125 | 貼上剪貼簿中的文字 |
| 識別碼 \_ 編輯 \_ 清除  | 0xE120 | 刪除選取的文字      |
| 識別碼 \_ 視圖 \_ 縮放   | 1242   | 縮放 ... (] 對話方塊)           |



 

在建立命令的清查時，查看現有的功能表和工具列。 請考慮使用者可以與工作區互動的所有方法。 雖然並非每個命令都適合包含在功能區中，但此練習可能很容易公開先前以 UI 層級遮蔽的命令。

### <a name="translate"></a>翻譯

並非每個命令都必須在功能區 UI 中表示。 例如，輸入文字、變更選取範圍、捲軸，或使用滑鼠來移動插入點都符合假設的文字編輯器中的命令，不過，它們不適合在命令列中公開，因為每一個都牽涉到與應用程式 UI 的直接互動。

相反地，某些功能可能不會被視為傳統上的命令。 例如，您可以在內容區或 [應用程式模式](ribbon-applicationmodes.md)中，以一組微調控制項的形式呈現印表機頁面邊界調整，而不是隱藏在對話方塊中。

> [!Note]  
> 記下每個命令可能指派的數值識別碼。 某些 UI 架構（例如，Microsoft Foundation class (MFC) ）會定義命令的識別碼，例如 [檔案] 和 [編輯] 功能表， (0xE100 至 0xE200) 。

 

### <a name="organize"></a>組織

在嘗試組織命令清查之前，您應該先檢查 [功能區使用者經驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx) ，以瞭解執行功能區 UI 時的最佳做法。

一般情況下，下列規則可套用至功能區命令組織：

-   在檔案或整體應用程式上操作的命令，最有可能屬於 [應用程式功能表](windowsribbon-controls-applicationmenu.md)。
-   常用) 的命令（例如 [剪下]、[複製] 和 [貼上] (）通常會放在預設的 [首頁] 索引標籤上。在更複雜的應用程式中，它們可能會在功能區 UI 中的其他位置重複。
-   重要或經常使用的命令可能會在 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md)中包含預設值。

功能區架構也透過 CoNtextPopup 視圖提供 CoNtextMenu 和浮動工具列控制項。 這些功能並非強制性的，但如果您的應用程式有一或多個現有的內容功能表，則遷移它們所包含的命令可能會允許重複使用現有的程式碼基底，並自動系結至現有的資源。

因為每個應用程式都不同，請閱讀指導方針，並嘗試將它們套用到最大限度的範圍。 功能區架構的其中一個目標是要提供熟悉且一致的使用者體驗，如果新的應用程式設計盡可能地鏡像現有的功能區應用程式，此目標將更能實現。

## <a name="adapt-your-code"></a>調整您的程式碼

一旦將功能區命令識別和組織成邏輯群組之後，將功能區架構併入現有的應用程式程式碼時所牽涉到的步驟數目，將視原始應用程式的複雜度而定。 一般而言，有三個基本步驟：

-   根據命令組織和版面配置規格來建立功能區標記。
-   以功能區功能取代舊版功能表和工具列功能。
-   執行 IUICommandHandler 介面卡。

### <a name="create-the-markup"></a>建立標記

命令清單以及其組織和配置是透過功能 [區標記編譯器](windowsribbon-intentcl.md)所使用的功能區標記檔案來宣告。

> [!Note]  
> 調整現有應用程式所需的許多步驟，類似于啟動新的功能區應用程式所需的步驟。 如需詳細資訊，請參閱建立新功能區應用程式逐步解說的 [功能區應用程式](windowsribbon-stepbystep.md) 教學課程。

 

功能區標記有兩個主要區段。 第一個區段是命令的資訊清單和其相關聯的資源， (字串和影像) 。 第二個區段指定功能區上控制項的結構和位置。

簡單文字編輯器的標記看起來可能如下列範例所示：

> [!Note]  
> 本文稍後會討論映射和字串資源。

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



為了避免重新定義 UI 架構（例如 MFC）所定義的符號，上述範例會針對每個命令使用稍微不同的符號名稱， (識別碼檔案 \_ \_ NEW 與 ID \_ CMD \_ NEW) 。 不過，指派給每個命令的數值識別碼必須保持不變。

若要將標記檔案整合至應用程式，請設定自訂的組建步驟來執行功能區標記編譯器，UICC.exe。 接著會將產生的標頭和資源檔合併到現有的專案中。 如果範例文字編輯器功能區應用程式命名為 "RibbonPad"，則需要類似如下的自訂群組建命令列：


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



標記編譯器會建立二進位檔案、標頭 (H) 檔案和資源 (RC) 檔。 由於現有的應用程式可能有現有的 RC 檔案，因此請在該 RC 檔案中包含產生的 H 和 RC 檔案，如下列範例所示：


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a>取代舊版功能表和工具列

使用繼承應用程式中的功能區來取代標準功能表和工具列需要下列各項：

1.  從應用程式的資源檔中移除工具列和功能表資源參考。
2.  刪除所有工具列和功能表列初始化程式碼。
3.  刪除用來將工具列或功能表列附加至應用程式最上層視窗的任何程式碼。
4.  具現化功能區架構。
5.  將功能區附加至應用程式的最上層視窗。
6.  載入編譯的標記。

> [!IMPORTANT]
> 您應保留現有的狀態列和鍵盤快速鍵表，因為功能區架構不會取代這些功能。

 

下列範例示範如何使用 [**IUIFramework：： initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize)初始化架構：


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



下列範例示範如何使用 [**IUIFramework：： LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) 載入已編譯的標記：


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



上述的 CApplication 類別，必須將一組元件物件模型 (由功能區架構定義的 COM) 介面： [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) 和 [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)。

[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) 會提供架構和應用程式之間的主要回呼介面 (例如，功能區的高度會透過 [**IUIApplication：： OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) 進行通訊，而提供個別命令的回呼以回應 [**IUIApplication：： OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)。

**秘訣：** 某些應用程式架構（例如 MFC）要求在轉譯應用程式的檔空間時，將功能區列的高度列入考慮。 在這些情況下，加入隱藏視窗以重迭功能區列，並強制檔空間為所需的高度是必要的。 如需此方法的範例，其中會根據 [**IUIRibbon：： GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) 方法所傳回的功能區高度來呼叫配置函數，請參閱 [HTMLEditRibbon 範例](windowsribbon-htmleditribbonsample.md)。

下列程式碼範例示範 [**IUIApplication：： OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) 實作為：


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a>執行 IUICommandHandler 介面卡

視原始應用程式的設計而定，您可以更輕鬆地使用多個命令處理常式，或叫用現有應用程式命令邏輯的單一橋接命令處理常式。 許多應用程式都使用 WM \_ 命令訊息來達到這個目的，因為這樣就足以提供單一的全用途命令處理常式，只需將 WM 的 \_ 命令訊息轉寄到最上層視窗。

不過，這種方法需要特殊的命令處理，例如 **Exit** 或 **Close**。 因為功能區在處理視窗訊息時無法終結，所以必須 \_ 將 WM 關閉訊息張貼至應用程式的 UI 執行緒，而且不應該以同步方式處理，如下列範例所示：


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a>正在遷移資源

在定義命令的資訊清單之後，就會宣告功能區的結構，並調整應用程式程式碼以裝載功能區架構，最後一個步驟就是每個命令的字串和影像資源規格。

> [!Note]  
> 字串和影像資源通常會在標記檔案中提供。 不過，您可以藉由執行 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 回呼方法，以程式設計方式產生或取代它們。

 

### <a name="string-resources"></a>字串資源

[**LabelTitle**](windowsribbon-element-command-labeltitle.md) 是針對命令所定義最常見的字串屬性。 這些會轉譯為索引標籤、群組和個別控制項的文字標籤。 舊版功能表項目中的標籤字串通常可以重複使用於 **LabelTitle** ，而不需要太多編輯。

但是，下列慣例在功能區的出現時已經變更：

-   您不再需要省略號 ( ... ) 尾碼（用來指出對話方塊啟動命令）。
-   [& 符號 (&]) 仍可用來指出出現在功能表中之命令的鍵盤快速鍵，但架構所支援的 [**命令提示**](windowsribbon-element-command-keytip.md) 字元屬性滿足類似的目的。

回頭參考文字編輯器範例，可以指定下列 LabelTitle 和快速鍵的字串：



| 符號           | 原始字串 | LabelTitle 字串 | Keytip 字串 |
|------------------|-----------------|-------------------|---------------|
| 新增識別碼檔案 \_ \_    | &新的            | &新的              | N             |
| 儲存識別碼檔案 \_ \_   | &儲存           | &儲存             | S             |
| 識別碼檔案的 \_ \_ SAVEAS | 將 &另存為 .。。       | 將 &另存為          | A             |
| 識別碼 \_ 檔案 \_ 開啟   | &開啟 .。。          | &amp;Open             | O             |
| 識別碼 \_ 檔案 \_ 結束   | 結束(&X)           | 結束(&X)             | X             |
| 識別碼 \_ 編輯 \_ 復原   | &復原           | 復原              | Z             |
| 識別碼 \_ 編輯 \_ 剪下    | Cu&t            | Cu&t              | X             |
| 識別碼 \_ 編輯 \_ 複本   | &複製           | &複製             | C             |
| 識別碼 \_ 編輯 \_ 貼上  | &貼上          | &貼上            | V             |
| 識別碼 \_ 編輯 \_ 清除  | &刪除         | &刪除           | D             |
| 識別碼 \_ 視圖 \_ 縮放   | &縮放 .。。          | Zoom              | Z             |



 

以下是應該在大部分命令上設定的其他字串屬性清單：

-   [**LabelDescription**](windowsribbon-element-command-labeldescription.md)
-   [**TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
-   [**TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)

您現在可以使用指定的所有字串和影像資源來宣告索引標籤、群組和其他功能區 UI 功能。

下列功能區標記範例示範各種字串資源：


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a>影像資源

功能區架構支援影像格式，可提供比上一個功能表和工具列元件所支援的影像格式更豐富的外觀和風格。

針對 Windows 8 和更新版本，功能區架構支援下列圖形格式：32位 ARGB 點陣圖 (BMP) 檔和可移植網狀圖形 (PNG) 具有透明度的檔。

針對 Windows 7 及更早版本，影像資源必須符合 Windows 中所使用的標準 BMP 圖形格式。

> [!Note]  
> 現有的影像檔案可以轉換成任何格式。 但是，如果影像檔案不支援消除鋸齒和透明度，結果可能會小於滿意。

 

在功能區架構中，無法指定影像資源的單一預設大小。 不過，若要 [支援控制項](windowsribbon-templates.md) 的調適型配置，可 (大型和小型) 以兩種大小來指定影像。 功能區架構中的所有影像都會根據每英寸的點來調整， (DPI) 解析度解析度的顯示，以及與此 DPI 設定相依的精確呈現大小。 如需詳細資訊，請參閱 [指定功能區影像資源](windowsribbon-imageformats.md) 。

下列範例示範如何在標記中參考一組 DPI 特定的影像：


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[指定功能區影像資源](windowsribbon-imageformats.md)
</dt> </dl>

 

 
---
title: 保存功能區狀態
description: Windows Ribon framework (功能區) 可讓您在應用程式會話之間保留各種使用者設定和喜好設定的狀態。
ms.assetid: f59e36be-8e3d-454a-b93c-9fc5fc5ecb47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a3b704151b657bdfe95845c8473a0fd197e87b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315763"
---
# <a name="persisting-ribbon-state"></a>保存功能區狀態

Windows Ribon framework (功能區) 可讓您在應用程式會話之間保留各種使用者設定和喜好設定的狀態。

-   [簡介](#introduction)
-   [可預測的體驗](#a-predictable-experience)
-   [儲存功能區設定](#save-ribbon-settings)
-   [載入功能區設定](#load-ribbon-settings)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

使用者可以在執行時間自訂功能區的各個層面，包括設定和互動喜好設定，以改善可用性和生產力。 功能區架構可透過在 [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) 介面的執行中定義的兩種方法，提供在應用程式會話之間保留這些設定的功能： [**IUIRibbon：： LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) 和 [**IUIRibbon：： SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)。

## <a name="a-predictable-experience"></a>可預測的體驗

[功能區使用者經驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx)會建議您盡可能提供可預測的使用者體驗，功能區應用程式應該會在應用程式關閉時，從最後選取的索引標籤) 保留功能區的狀態 (。 如此一來，當相同的應用程式啟動時，就可以還原前一個會話的設定和自訂，而且使用者可以使用與其留下的相同方式來繼續與應用程式互動。

可在執行時間修改並在應用程式會話之間保留的功能區設定會列在命令內容功能表中。 包括：

-   由使用者新增至 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md) 命令清單的命令。 由 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件透過 [UI \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) 屬性索引鍵來指定。

    下列螢幕擷取畫面顯示 [ **新增至快速存取] 工具列** 內容功能表命令。

    ![microsoft 油漆功能區中命令內容功能表的螢幕擷取畫面。](images/controls/qat-contextmenu-add.png)

-   慣用的 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md) 停駐狀態。 由 [ui \_ PKEY \_ QuickAccessToolbarDock](windowsribbon-reference-properties-uipkey-quickaccesstoolbardock.md)屬性索引鍵的 [**ui \_ CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock)值所指定。

    這個螢幕擷取畫面會在其預設應用程式標題列位置顯示 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md) ，並在功能區內容功能表命令 **下方顯示快速存取工具列** 。

    ![microsoft 油漆功能區中命令內容功能表的螢幕擷取畫面。](images/controls/qat-contextmenu-add.png)

    這個螢幕擷取畫面會顯示功能區下方的 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md) 。

    ![快速存取工具列上停駐于功能區下方的螢幕擷取畫面。](images/controls/qat-dockbottom.png)

-   功能區最小化狀態，如 [UI \_ PKEY \_ 最小化](windowsribbon-reference-properties-uipkey-minimized.md) 屬性索引鍵的布林值所指定。

    > [!Note]  
    > 功能區最小化狀態不等於功能區折迭狀態。 處於折迭狀態時，功能區會完全隱藏，而且無法與互動。 如果應用程式視窗的大小縮小（水準或垂直）至功能區遮蔽應用程式工作區的點，則架構會自動叫用此狀態。 當應用程式視窗的大小增加時，架構會還原功能區。

     

    這個螢幕擷取畫面會顯示 [功能區] 內容功能表命令的 **最小化** 。

    ![microsoft 油漆功能區中命令內容功能表的螢幕擷取畫面。](images/controls/qat-contextmenu-add.png)

    這個螢幕擷取畫面顯示最小化的功能區。

    ![最小化 microsoft 油漆功能區的螢幕擷取畫面。](images/properties/ui-pkey-minimized.png)

## <a name="save-ribbon-settings"></a>儲存功能區設定

[**IUIRibbon：： SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)方法會將持續性功能區狀態的二進位表示寫入 (上一節中所述的) 至 [IStream](/windows/win32/api/objidl/nn-objidl-istream)物件。 然後，應用程式會將 IStream 物件的內容儲存到檔案或 Windows 登錄中。

下列範例示範使用 [**IUIRibbon：： SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)方法將功能區狀態寫入 [IStream](/windows/win32/api/objidl/nn-objidl-istream)物件時所需的基本程式碼。


```C++
// pRibbon        - Pointer to the IUIRibbon interface
// ppStatusStream - Pointer to the location of a newly created IStream object
HRESULT CApplication::SaveRibbonStatusToStream(
                        __in IUIRibbon *pRibbon, 
                        __out IStream **ppStatusStream)
{
  HRESULT hr = E_FAIL; 

  *ppStatusStream = NULL;
  IStream* pStream;
  if (SUCCEEDED(hr = CreateStreamOnHGlobal(
                       NULL,  // Internally allocate a new shared memory.
                       FALSE, // Free hGlobal after IStream object released.
                       &pStream)))
  {
    if (SUCCEEDED(hr = pRibbon->SaveSettingsToStream(*ppStatusStream)))
    {                  
      pStream->AddRef();
      *ppStatusStream = pStream;
    }
    pStream->Release();
  }
  return hr;
}
```



## <a name="load-ribbon-settings"></a>載入功能區設定

[**IUIRibbon：： LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)方法可用來透過 [**IUIRibbon：： SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream)方法，取得儲存為 [IStream](/windows/win32/api/objidl/nn-objidl-istream)物件的持續性功能區狀態資訊。 當應用程式初始化時，IStream 物件中的資訊會套用至功能區 UI。

下列範例示範使用 [**IUIRibbon：： LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream)方法從 [IStream](/windows/win32/api/objidl/nn-objidl-istream)物件載入功能區狀態所需的基本程式碼。


```C++
// pRibbon       - Pointer to the IUIRibbon interface
// pStatusStream - Pointer to the IStream object that contains the Ribbon state information
HRESULT CApplication::LoadRibbonStatusFromStream(
                        __in IUIRibbon *pRibbon, 
                        __in IStream *pStatusStream)
{     
  HRESULT hr = E_FAIL;
  if (pStatusStream)
  {
    // Set the stream position to the beginning first.
    LARGE_INTEGER liStart = {0, 0};
    ULARGE_INTEGER ulActual;
    pStatusStream->Seek(liStart, STREAM_SEEK_SET, &ulActual);
    hr = pRibbon->LoadSettingsFromStream(pStatusStream);
  }
  return hr;
}
```



為了達到最佳效能， [**IUIRibbon：： LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) 方法應該在 framework 初始化階段期間從 [**IUIApplication：： OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) 回呼函式中呼叫，如下列範例所示。


```C++
IFACEMETHODIMP CMyRibbonApplication::OnViewChanged(
                                       UINT nViewID, 
                                       __in UI_VIEWTYPE typeID, 
                                       __in IUnknown* pView, 
                                       UI_VIEWVERB verb, 
                                       INT iReasonCode)
{
  HRESULT hr = E_NOTIMPL;
  if (UI_VIEWVERB_CREATE == verb)
  {
    IUIRibbon* pRibbon = NULL;
    hr = pView->QueryInterface(IID_PPV_ARGS(&pRibbon));

    if (SUCCEEDED(hr))
    {
      hr = _LoadRibbonSettings(pRibbon);
      pRibbon->Release();
    }
  }
  return hr;
}

HRESULT CMyRibbonApplication::_LoadRibbonSettings(IUIRibbon* pRibbon)
{
  ...
  pRibbon->LoadSettingsFromStream(pStream);
  ...
}
```



相同功能區架構應用程式的多個實例可以個別管理每個功能區狀態為個別的 [istream](/windows/win32/api/objidl/nn-objidl-istream) 物件，或透過單一 istream 物件以群組的方式來管理。

在跨應用程式實例群組同步處理功能區狀態時，每個最上層視窗都必須接聽 [WM \_ 啟用](../inputdev/wm-activate.md) 通知。 停用的最上層視窗會使用 [**IUIRibbon：： SaveSettingsToStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) 方法來儲存其功能區狀態，而所啟動的最上層視窗會使用 [**IUIRibbon：： LoadSettingsFromStream**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) 方法載入其功能區狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 
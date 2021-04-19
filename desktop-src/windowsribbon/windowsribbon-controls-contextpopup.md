---
title: 內容快顯視窗
description: 內容快顯視窗是 Windows 功能區架構的 [CoNtextPopup] 視圖中的主要控制項。
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77441cc3cdcc9212d27d2230d76d2618f1831ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106988027"
---
# <a name="context-popup"></a>內容快顯視窗

內容快顯視窗是 Windows 功能區架構的 [ [**CoNtextPopup] 視圖**](windowsribbon-element-contextpopup.md) 中的主要控制項。 它是一個豐富的內容功能表系統，僅由架構公開為功能區實作為擴充功能，架構不會以獨立控制項的形式公開內容快顯視窗。

-   [內容快顯視窗的元件](#context-popup)
-   [執行內容快顯視窗](#implement-the-context-popup)
    -   [標記](#markup)
    -   [程式碼](#code)
-   [內容快顯功能表屬性](#context-popup-properties)
-   [相關主題](#related-topics)

## <a name="components-of-the-context-popup"></a>內容快顯視窗的元件

內容快顯視窗是內容功能表的邏輯容器，也是透過 [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 和 [**浮動工具列**](windowsribbon-element-minitoolbar.md) 標記元素分別公開的 Mini-Toolbar 子控制項：

-   [**CoNtextMenu**](windowsribbon-element-contextmenu.md)會公開命令和資源庫的功能表。
-   [**浮動工具列**](windowsribbon-element-minitoolbar.md)會公開各種命令、資源庫和複雜控制項（例如 [字型控制項](windowsribbon-controls-fontcontrol.md)和 [下拉式](windowsribbon-controls-combobox.md)方塊）的浮動工具列。

每個子控制項在內容快顯視窗中最多隻能出現一次。

下列螢幕擷取畫面說明內容快顯視窗及其組成子控制項。

![顯示功能區內容 ui 元件之標注的螢幕擷取畫面。](images/controls/contextpopup.png)

內容快顯視窗純粹是概念，而且不會公開任何 UI 功能，例如定位或調整大小。

> [!Note]  
> 在感興趣的物件上，以滑鼠右鍵按一下 (或透過鍵盤快速鍵 SHIFT + F10) ，通常會顯示內容快顯視窗。 不過，顯示內容快顯視窗所需的步驟是由應用程式所定義。

 

## <a name="implement-the-context-popup"></a>執行內容快顯視窗

以類似于其他 Windows 功能區架構控制項的方式，會透過標記元件來執行內容快顯視窗，該元件會指定其簡報詳細資料，以及控制其功能的程式碼元件。

下表列出每個內容快顯項目子控制項所支援的控制項。



| 控制                                                                  | Mini-Toolbar | 操作功能表 |
|--------------------------------------------------------------------------|--------------|--------------|
| [按鈕](windowsribbon-controls-button.md)                              | x            | x            |
| [核取方塊](windowsribbon-controls-checkbox.md)                         | x            | x            |
| [下拉式方塊](windowsribbon-controls-combobox.md)                         | x            |              |
| [下拉式按鈕](windowsribbon-controls-dropdownbutton.md)            | x            | x            |
| [下拉式色彩選擇器](windowsribbon-controls-dropdowncolorpicker.md) | x            | x            |
| [下拉式圖庫](windowsribbon-controls-dropdowngallery.md)          | x            | x            |
| [字型控制項](windowsribbon-controls-fontcontrol.md)                   | x            |              |
| [說明按鈕](windowsribbon-controls-helpbutton.md)                     |              |              |
| [功能區中的資源庫](windowsribbon-controls-inribbongallery.md)          |              |              |
| [Spinner](windowsribbon-controls-spinner.md)                            |              |              |
| [分割按鈕](windowsribbon-controls-splitbutton.md)                   | x            | x            |
| [分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md)    | x            | x            |
| [切換按鈕](windowsribbon-controls-togglebutton.md)                 | x            | x            |



 

### <a name="markup"></a>標記

每個內容快顯視窗子控制項都必須在標記中個別宣告。

### <a name="mini-toolbar"></a>Mini-Toolbar

將控制項新增至內容快顯視窗迷你工具列時，應考慮下列兩個建議：

-   控制項應可高度辨識，並提供明顯的功能。 熟悉的是關鍵，因為標籤和工具提示不會公開給 Mini-Toolbar 控制項。
-   控制項所公開的每個命令都應該顯示在功能區 UI 的其他位置。 Mini-Toolbar 不支援鍵盤流覽。

下列範例示範 [**浮動工具列**](windowsribbon-element-minitoolbar.md) 專案的基本標記，其中包含三個 [按鈕](windowsribbon-controls-button.md) 控制項。

> [!Note]  
> 針對迷你工具列中的每個控制項資料列指定一個 [**MenuGroup**](windowsribbon-element-menugroup.md) 元素。

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a>操作功能表

下列範例示範 [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 專案的基本標記，其中包含三個 [按鈕](windowsribbon-controls-button.md) 控制項。

> [!Note]  
> [**MenuGroup**](windowsribbon-element-menugroup.md)元素中的每一組控制項都會以內容功能表中的水準橫條分隔。

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



雖然內容快顯視窗最多可包含每個子控制項的其中一個，但功能區標記中的多個 [**CoNtextMenu**](windowsribbon-element-contextmenu.md) 和 [**浮動工具列**](windowsribbon-element-minitoolbar.md) 元素宣告是有效的。 如此一來，應用程式就可以根據應用程式所定義的準則（例如工作區內容）支援各種內容功能表和 Mini-Toolbar 控制群組合。

如需詳細資訊，請參閱 [**CoNtextMap**](windowsribbon-element-contextmap.md) 元素。

下列範例示範 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 元素的基本標記。


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a>程式碼

若要叫用內容快顯視窗，在功能區應用程式的最上層視窗收到 WM CONTEXTMENU 通知時，會呼叫 [**IUICoNtextualUI：： ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) 方法 \_ 。

此範例示範如何 \_ 在功能區應用程式的 WndProc () 方法中處理 WM CONTEXTMENU 通知。


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



下列範例會示範功能區應用程式如何使用 [**IUICoNtextualUI：： ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) 方法，在特定螢幕位置顯示內容快顯視窗。

GetCurrentCoNtext () 具有 `cmdContextMap` 上述標記範例中所定義的值。

g \_ pApplication 是 [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) 介面的參考。


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



您可以在關閉內容快顯視窗之前釋放 [**IUICoNtextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) 的參考，如上述範例所示。 不過，您必須在某個時間點釋放參考，以避免記憶體流失。

> [!Caution]  
> Mini-Toolbar 的內建淡化效果是以滑鼠指標的相近為基礎。 基於這個理由，建議您盡可能將 Mini-Toolbar 顯示為靠近滑鼠指標。 否則，由於衝突的顯示機制，Mini-Toolbar 可能不會如預期般呈現。

 

## <a name="context-popup-properties"></a>內容快顯功能表屬性

沒有與內容快顯功能表控制項相關聯的屬性索引鍵。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[CoNtextPopup 範例](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 
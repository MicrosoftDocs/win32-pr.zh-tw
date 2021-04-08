---
title: 使用主題子類別
description: 代表控制項的主題類別（例如 ComboBox、Edit、ExplorerBar、Rebar、Tab 和 Toolbar）可以子類別化，以提供該特定控制項的主題變化。
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672899"
---
# <a name="using-theme-subclasses"></a>使用主題子類別

代表控制項的主題類別（例如 ComboBox、Edit、ExplorerBar、Rebar、Tab 和 Toolbar）可以子類別化，以提供該特定控制項的主題變化。 例如， **按鈕** 類別會子類別化，以 `Start::Button` 提供套用至 [ **開始** ] 按鈕之主題的控制權。

> [!Note]  
> 當您建立子類別（如本主題中所討論的子類別）時，請特別小心。 因為子類別可能會在後續版本的 Windows 中改變或無法使用，所以您不建議使用它們。

 

## <a name="two-ways-to-use-a-theme-subclass"></a>使用主題子類別的兩種方式

應用程式可以使用下列其中一種方式的子類別化主題：

-   它可以使用 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) 函式搭配 `subclass::class` *pszClassList* 參數中的表單字串。
-   它可以使用 *pszSubAppName* 參數中的主題子類別名稱來呼叫 [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) 。

## <a name="using-theme-messages-that-set-visual-style"></a>使用設定視覺化樣式的主題訊息

某些控制項（例如 Rebar 和工具列）提供您可以傳送的特定訊息，指示控制項使用主題子類別。 針對這些控制項，在訊息的 *lParam* 參數中提供包含主題子類別名稱之緩衝區的指標。 使用一般 [**CCM \_ SETWINDOWTHEME**](ccm-setwindowtheme.md) 訊息，或使用如下表所示的特定變異。



| 控制    | 訊息                                             |
|------------|-----------------------------------------------------|
| 工具提示    | [**TTM \_ SETWINDOWTHEME**](ttm-setwindowtheme.md)   |
| 工具列    | [**TB \_ SETWINDOWTHEME**](tb-setwindowtheme.md)     |
| 鋼筋      | [**RB \_ SETWINDOWTHEME**](rb-setwindowtheme.md)     |
| ComboBoxEx | [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md) |



 

下表列出 Windows Vista 定義的一些子類別。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>類別</th>
<th>子</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ComboBox</td>
<td><ul>
<li>位址</li>
<li>AddressComposited</li>
<li>InactiveAddress</li>
<li>InactiveAddressComposited</li>
<li>MaxAddress</li>
<li>MaxAddressComposited</li>
<li>MaxInactiveAddress</li>
<li>MaxInactiveAddressComposited</li>
</ul></td>
</tr>
<tr class="even">
<td>編輯</td>
<td><ul>
<li>位址</li>
<li>AddressComposited</li>
<li>InactiveAddress</li>
<li>InactiveAddressComposited</li>
<li>InactiveSearchBoxEdit</li>
<li>InactiveSearchBoxEditComposited</li>
<li>MaxAddress</li>
<li>MaxAddressComposited</li>
<li>MaxInactiveAddress</li>
<li>MaxInactiveAddressComposited</li>
<li>MaxInactiveSearchBoxEdit</li>
<li>MaxInactiveSearchBoxEditComposited</li>
<li>MaxSearchBoxEdit</li>
<li>MaxSearchBoxEditComposited</li>
<li>SearchBoxEdit</li>
<li>SearchBoxEditComposited</li>
</ul></td>
</tr>
<tr class="odd">
<td>鋼筋</td>
<td><ul>
<li>BrowserTabBar</li>
<li>InactiveNavbar</li>
<li>InactiveNavbarComposited</li>
<li>MaxInactiveNavbar</li>
<li>MaxInactiveNavbarComposited</li>
<li>MaxNavbar</li>
<li>MaxNavbarComposited</li>
<li>瀏覽列</li>
<li>NavbarComposited</li>
<li>NavbarNonTopmost</li>
</ul></td>
</tr>
<tr class="even">
<td>索引標籤</td>
<td><ul>
<li>BrowserTab</li>
</ul></td>
</tr>
<tr class="odd">
<td>工具列</td>
<td><ul>
<li>Go</li>
<li>GoComposited</li>
<li>InactiveGo</li>
<li>InactiveGoComposited</li>
<li>MaxGo</li>
<li>MaxGoComposited</li>
<li>MaxInactiveGo</li>
<li>MaxInactiveGoComposited</li>
<li>SearchButton</li>
<li>SearchButtonComposited</li>
<li>出差</li>
<li>TravelComposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a>Internet Explorer 子類別

在 Windows Vista 中，即使類別本身不存在，Windows Internet Explorer 和 Windows 檔案總管內部特定類別的子類別也可以使用。 下表列出可用的子類別。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>AddressBand</td>
<td><ul>
<li>AB</li>
<li>ABGreen</li>
<li>ABGreenComposited</li>
<li>ABRed</li>
<li>ABRedComposited</li>
<li>ABYellow</li>
<li>ABYellowComposited</li>
</ul></td>
</tr>
<tr class="even">
<td>SearchBox</td>
<td><ul>
<li>InactiveSearchBox</li>
<li>InactiveSearchBoxComposited</li>
<li>MaxInactiveSearchBox</li>
<li>MaxInactiveSearchBoxComposited</li>
<li>MaxSearchBox</li>
<li>MaxSearchBoxComposited</li>
<li>SearchBoxComposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

下表顯示這些類別的詳細資訊。



| 控制     | 部分         | 狀態                                                 |
|-------------|--------------|--------------------------------------------------------|
| ADDRESSBAND | ABBACKGROUND | 一般 (0x1) 、經常性 (0x2) 、已停用 (0x3) 、焦點 (0x4)  |
| 搜尋方塊   | SBBACKGROUND | 一般 (0x1) 、經常性 (0x2) 、已停用 (0x3) 、焦點 (0x4)  |



 

 

 





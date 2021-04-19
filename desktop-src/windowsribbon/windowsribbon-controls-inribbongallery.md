---
title: In-Ribbon 資源庫
description: In-Ribbon 圖庫是一個控制項，可在功能區中顯示相關專案或命令的集合。 如果資源庫中有太多專案，則會提供展開箭號，以在展開的窗格中顯示集合的其餘部分。
ms.assetid: d608dd0d-a0af-49a6-a129-7115195c0df2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef644128204fa0b20284dbb63368ef530b0dd0b3
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106996170"
---
# <a name="in-ribbon-gallery"></a>In-Ribbon 資源庫

In-Ribbon 圖庫是一個控制項，可在功能區中顯示相關專案或命令的集合。 如果資源庫中有太多專案，則會提供展開箭號，以在展開的窗格中顯示集合的其餘部分。

-   [詳細資料](#details)
-   [功能區元件庫屬性](#in-ribbon-gallery-properties)
-   [相關主題](#related-topics)

## <a name="details"></a>詳細資料

下列螢幕擷取畫面說明 Microsoft 小畫家中的功能區 In-Ribbon 資源庫控制項。

![microsoft 油漆功能區中 inribbongallery 控制項的螢幕擷取畫面。](images/controls/inribbongallery.png)

## <a name="in-ribbon-gallery-properties"></a>In-Ribbon 資源庫屬性

功能區架構會為 In-Ribbon 資源庫控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

通常會在功能區 UI 中更新 In-Ribbon 資源庫屬性，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與 In-Ribbon 資源庫控制項相關聯的屬性索引鍵。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性索引鍵</th>
<th>備註</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>只能透過失效進行更新。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>只能透過失效進行更新。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>只能透過失效進行更新。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>只能透過失效進行更新。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a> (僅適用于專案資源庫) <br/></td>
<td>支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。
<blockquote>
[!Note]<br />
如果與控制項相關聯的命令透過呼叫 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework：： InvalidateUICommand</strong></a>而失效，則架構 <code>UI_INVALIDATIONS_VALUE</code> 會在傳遞做為 <em>旗標</em>的值時查詢此屬性。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>只能透過失效進行更新。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>只能透過失效進行更新。</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>只能透過失效進行更新。</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>只能透過失效進行更新。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**InRibbonGallery 元素**](windowsribbon-element-inribbongallery.md)
</dt> <dt>

[使用資源庫](ribbon-controls-galleries.md)
</dt> <dt>

[資源庫範例](windowsribbon-gallerysample.md)
</dt> </dl>


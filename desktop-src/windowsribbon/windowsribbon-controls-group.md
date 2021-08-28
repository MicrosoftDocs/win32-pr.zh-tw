---
title: '群組 (Windows 功能區架構) '
description: 群組會在索引標籤中組織相關的命令和控制項。
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c153f8cd9d1fc0d2d2bdbaabab0b2e15e099e50d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467415"
---
# <a name="group-windows-ribbon-framework"></a>群組 (Windows 功能區架構) 

群組會在索引標籤中組織相關[的命令和控制項。](windowsribbon-controls-tab.md)

-   [詳細資料](#details)
-   [群組屬性](#group-properties)
-   [相關主題](#related-topics)

## <a name="details"></a>詳細資料

下列螢幕擷取畫面說明功能區群組控制項。

![具有顯示群組之標注的螢幕擷取畫面。](images/controls/group.png)

## <a name="group-properties"></a>群組屬性

功能區架構會針對群組控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

一般而言，群組屬性會在功能區 UI 中更新，方法是透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與群組控制項相關聯的屬性索引鍵。




| 屬性索引鍵 | 備註 | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | 只能透過失效進行更新。<blockquote>[!Note]<br />架構要求群組控制項的 <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> 值的開頭必須是大寫字母 Z。如果 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler：： UpdateProperty</strong></a> 回呼方法中的應用程式所提供的值不是以字母 Z 開頭，則會忽略此值，而值會由架構產生。 Framework 值是字母 Z，後面接著以1開始的數值，並視需要順序遞增，以供後續的群組控制項 (Z1、Z2、...、Zx) 。</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | 只能透過失效進行更新。 | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**Group 元素**](windowsribbon-element-group.md)
</dt> </dl>


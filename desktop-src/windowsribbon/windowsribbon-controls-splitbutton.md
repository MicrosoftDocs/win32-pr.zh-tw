---
title: Split Button
description: '[分割] 按鈕是複合控制項，使用者可以選取系結至主要按鈕的預設值，或從下拉式清單中顯示的互斥值清單中，選取系結至次要按鈕的清單。'
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066a2275c49ad8d6dd32dd8ce4fd3d89956f204c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473754"
---
# <a name="split-button"></a>Split Button

[分割] 按鈕是複合控制項，使用者可以選取系結至主要按鈕的預設值，或從下拉式清單中顯示的互斥值清單中，選取系結至次要按鈕的清單。

-   [簡介](#introduction)
-   [分割按鈕屬性](#split-button-properties)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

如果有明顯的預設值可供使用，而且個別專案可以用影像、文字或兩者表示，則這個控制項非常適合用來公開密切相關的專案。

下列螢幕擷取畫面說明功能區分割按鈕。

![範例功能區中 splitbutton 控制項的螢幕擷取畫面。](images/controls/splitbutton.png)

## <a name="split-button-properties"></a>分割按鈕屬性

功能區架構會針對分割按鈕控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。

一般來說，在功能區 UI 中，會透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效，以更新分割按鈕屬性。 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。

[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。 例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。

> [!Note]  
> 在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。

 

下表列出與分割按鈕控制項相關聯的屬性索引鍵。




| 屬性索引鍵 | 備註 | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | 支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。<br /> 如果停用所有子專案，架構會將 <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> 設定為 false (0) 。 否則，如果已啟用一個或多個子專案，UI_PKEY_Enabled 會設定為 true (-1) 。<blockquote>[!Important]<br />在啟用或停用一個或多個子專案之後，分割按鈕控制項的 <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> 屬性應該會失效。 這可確保架構會查詢更新的屬性值，並在功能區 UI 中重新整理分割按鈕控制項的狀態。</blockquote><br /><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | 只能透過失效進行更新。 | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | 只能透過失效進行更新。 | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows功能區架構控制項程式庫](windowsribbon-controls-entry.md)
</dt> <dt>

[**SplitButton 標記元素**](windowsribbon-element-splitbutton.md)
</dt> </dl>

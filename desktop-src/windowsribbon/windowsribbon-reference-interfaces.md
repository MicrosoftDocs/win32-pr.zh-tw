---
title: '介面 (功能區架構) '
description: Windows 功能區架構介面的參考檔。
ms.assetid: d5fd6e4f-ca10-4010-aab4-d2728b0ac53c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c168a342b7f362d2d679d578a88011c9d14977
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093711"
---
# <a name="interfaces-ribbon-framework"></a>介面 (功能區架構) 

Windows 功能區架構介面的參考檔。

### <a name="interfaces"></a>介面



| 主題                                                                                  | 目錄                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)介面是由應用程式所執行，並定義功能區架構的回呼進入點方法。<br/>                                                                                                                                                                                                              |
| [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)                         | [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)介面是由功能區架構所執行。 **IUICollection** 介面會定義在執行時間動態操作集合型控制項（例如各種功能區資源 [庫](ribbon-controls-galleries.md)和快速存取工具列 (QAT) ）的方法。<br/>                                              |
| [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent)介面是由應用程式所執行，並定義在執行時間處理集合變更所需的方法。<br/>                                                                                                                                                                                |
| [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)介面是由應用程式所執行，並定義從功能區架構收集命令資訊和處理命令事件的方法。<br/>                                                                                                                                                              |
| [**IUICoNtextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)                     | [**IUICoNtextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)介面是由功能區架構所執行，並提供 [內容](windowsribbon-controls-contextpopup.md)快顯視圖的核心功能。<br/>                                                                                                                                                                       |
| [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                           | [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)介面是由功能區架構所執行，並定義提供架構核心功能的方法。<br/>                                                                                                                                                                                                     |
| [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                   | [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)介面是由應用程式所執行，並定義取得影像的方法，以便在功能區架構的功能區和內容彈出 UI 中顯示。<br/>                                                                                                                                                                          |
| [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)               | [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap) 是由功能區架構實作為的 factory 介面，可定義建立 [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) 物件的方法。<br/>                                                                                                                                                             |
| [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                                 | [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)介面是由功能區架構所執行，並提供指定功能區設定和屬性的能力。 <br/>                                                                                                                                                                                                               |
| [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)           | [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)是唯讀介面，可定義用來抓取屬性索引鍵所識別之值的方法。 這個介面是由功能區架構所執行，而且也會由主應用程式針對專案資源庫的 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)物件中的每個專案執行。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 功能區架構參考](windowsribbon-reference-entry.md)
</dt> </dl>

 


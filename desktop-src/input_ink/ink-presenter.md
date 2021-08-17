---
description: 筆跡呈現器 API 可以讓 Microsoft Win32 應用程式透過插入 App 之 DirectComposition 視覺化樹狀結構的 InkPresenter 物件，來管理筆跡輸入 (標準和已修改) 的輸入、處理及轉換。
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: 筆跡展示者
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ccd201f39cf232e91c65d8ef15c6ccc0e8202b231818aa50d34d70f780f2d9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977018"
---
# <a name="ink-presenter"></a>筆跡展示者

筆墨演講者 Api 可讓 Microsoft Win32 應用程式透過插入應用程式 [DirectComposition](../directcomp/directcomposition-portal.md)視覺化樹狀結構的 [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter)物件，來管理筆墨輸入的輸入、處理和轉譯 (標準和修改過的) 。

> [!Note]
>
> 標準筆墨輸入 (畫筆提示或橡皮擦提示/按鈕) 不會使用次要 affordance 來修改，例如畫筆圓筒按鈕、滑鼠右鍵或類似的按鈕。

通用 Windows 平臺 (UWP) 使用 Extensible Application Markup Language (XAML 的應用程式) 透過 [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)控制項提供這種功能，以及連接到 XAML [DirectComposition](../directcomp/directcomposition-portal.md)視覺化樹狀結構的 [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter)物件。 如需詳細資訊，請參閱 [畫筆和手寫筆互動](/windows/uwp/design/input/pen-and-stylus-interactions)。

[筆墨](ink-renderer.md)轉譯器的設計目的是要讓有興趣在 [](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) / 原生 Win32 應用程式中提供 XAML 架構 InkCanvas [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter)功能的通用 Windows 應用程式開發人員使用。

## <a name="in-this-section"></a>本節內容



| 主題                                                               | 描述                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [筆跡展示者類別](ink-presenter-classes.md)<br/>       | 本節所包含的主題會提供筆跡展示者類別的參考規格。 <br/>    |
| [筆跡展示者介面](ink-presenter-interfaces.md)<br/> | 本節所包含的主題會提供筆跡呈現介面的參考規格。 <br/> |



 

## <a name="related-topics"></a>相關主題

[筆跡展示者](ink-presenter.md)、[畫筆和手寫筆互動](/windows/uwp/design/input/pen-and-stylus-interactions)、[筆墨分析範例](/samples/microsoft/windows-universal-samples/inkanalysis/)、[簡單筆墨範例](/samples/microsoft/windows-universal-samples/simpleink/)、[複雜](/samples/microsoft/windows-universal-samples/complexink/)的筆墨範例

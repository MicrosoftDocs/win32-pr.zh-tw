---
description: 本節所包含的主題會提供筆跡呈現介面的參考規格。
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: 筆跡展示者介面
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 0c1fb4cab0b8387dec7c75087a72719f72fbc85dc2776a5e20fc6d638fb02d95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092388"
---
# <a name="ink-presenter-interfaces"></a>筆跡展示者介面

本節所包含的主題會提供 [筆跡呈現](ink-presenter.md) 介面的參考規格。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|---|---|
| [**IInkCommitRequestHandler**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | 啟用您的應用程式 (而不是 [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) 物件) ，以將所有暫止的 Microsoft DirectComposition 命令認可到應用程式的 [DirectComposition](../directcomp/directcomposition-portal.md) 視覺化樹狀結構。<br/>   |
| [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | 透過建立應用程式執行緒來啟用筆跡輸入、處理和轉譯，以裝載 [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) 物件，並將它插入應用程式的 [DirectComposition](../directcomp/directcomposition-portal.md) 視覺化樹狀結構中。 <br/> |
| [**IInkHostWorkItem**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | 表示要在 [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) 物件執行緒上執行的筆墨運算。<br/>                                                                                                                                                  |
| [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | 代表可以設定並插入至傳統 Windows 應用程式之 [DirectComposition](../directcomp/directcomposition-portal.md)視覺化樹狀結構的 [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) 。 <br/>                                        |

## <a name="related-topics"></a>相關主題

[筆跡展示者](ink-presenter.md)、[畫筆和手寫筆互動](/windows/uwp/design/input/pen-and-stylus-interactions)、[筆墨分析範例](/samples/microsoft/windows-universal-samples/inkanalysis/)、[簡單筆墨範例](/samples/microsoft/windows-universal-samples/simpleink/)、[複雜](/samples/microsoft/windows-universal-samples/complexink/)的筆墨範例

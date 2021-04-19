---
description: 從 Windows Vista 開始，TextInputPanel 會取代 PenInputPanel，以控制平板電腦輸入面板的螢幕外觀和行為。下列各節說明使用文字輸入面板應用程式開發介面來設計輸入面板的程式。TextInputPanel for PenInputPanelUsing 輸入面板的使用者 AutoCompleteEnabling 自訂筆墨的文字更正 CollectorsNote 文字輸入面板會在名為 TabTip.exe 的可執行檔中執行。 使用/SeekDesktop 參數執行 TabTip.exe 時，會嘗試在非標準的互動式桌面上執行較精簡的輸入面板功能版本，如同使用 CreateDesktop 所建立。 針對大部分建立的桌面，輸入面板會在此模式中自動執行。 此參數提供在不尋常的應用程式案例中啟動它，否則會導致自動啟動的方法。 如果輸入面板已在桌面上執行，此參數將不會有任何作用，而且 TabTip.exe 的實例將會立即結束。
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: 程式設計文字輸入面板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981678"
---
# <a name="programming-the-text-input-panel"></a>程式設計文字輸入面板

從 Windows Vista 開始， [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) 會取代 [**PenInputPanel**](peninputpanel-class.md) ，以控制平板電腦輸入面板的螢幕外觀和行為。

下列各節說明使用文字輸入面板應用程式開發介面來設計輸入面板的程式。

-   [適用于 PenInputPanel 使用者的 TextInputPanel](textinputpanel-for-users-of-peninputpanel.md)
-   [使用輸入面板自動完成](using-input-panel-autocomplete.md)
-   [啟用自訂筆墨收集器的文字更正](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> 文字輸入面板會實作為稱為 TabTip.exe 的可執行檔。 使用 */SeekDesktop* 參數執行 TabTip.exe 時，會嘗試在非標準的互動式桌面上執行較精簡的輸入面板功能版本，如同使用 [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)所建立。 針對大部分建立的桌面，輸入面板會在此模式中自動執行。 此參數提供在不尋常的應用程式案例中啟動它，否則會導致自動啟動的方法。 如果輸入面板已在桌面上執行，此參數將不會有任何作用，而且 TabTip.exe 的實例將會立即結束。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 PenInputPanel 類別來設計輸入面板](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 

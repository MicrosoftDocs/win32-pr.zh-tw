---
description: 以下是顯示和相關的文字處理方式選項，可支援精細的印刷效果或複雜的腳本： Text functionsEdit controlsRich edit controlsUniscribe
ms.assetid: 337bc798-e75d-4389-8fea-577eb82a0ed5
title: 複雜的腳本處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e4be6295bff949c8e29036ef3af496c673575e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977349"
---
# <a name="complex-script-processing"></a>複雜的腳本處理

以下是顯示和相關的文字處理方式的選項，可支援精細的印刷效果或複雜的腳本：

-   文字函數
-   編輯控制項
-   Rich edit 控制項
-   Uniscribe

您選擇的選項取決於下列因素：

-   文字或腳本的類型。
-   執行模型，例如，應用程式所中斷的文字配置和處理。
-   更新現有的應用程式，而不是建立新的應用程式。

一般情況下，執行相當簡單之腳本處理的應用程式可以選擇處理複雜字集的任何選項。 但是，若要完整控制複雜的腳本處理，建議使用 Uniscribe。

## <a name="complex-script-processing-using-text-functions"></a>使用文字函數處理複雜的腳本

使用的應用程式大多是純文字，也就是使用相同字樣、權數、色彩等的文字，在傳統上是使用標準文字函式（例如 [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta)、 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)、 [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta)、 [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)和 [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa)）來撰寫文字和測量的行長度。 這些函式支援處理複雜的腳本和精細的印刷樣式效果。 如需詳細資訊，請參閱字型 [和文字](../gdi/fonts-and-text.md)。

一般情況下，標準文字支援對處理複雜字集的應用程式而言是透明的。 不過，您應該留意一些特定規則，以便在撰寫支援精細印刷樣式和處理複雜字集的應用程式時：

-   您的應用程式應該將字元儲存在緩衝區中，並一次顯示整行文字，例如，在使用者輸入的每個字元上呼叫 [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) 。 這種機制可讓 advanced text 成形模組使用內容， [以正確地](uniscribe-glossary.md) 重新排列和產生字元。
-   應用程式應該使用 [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) 來判斷行長度，而不是從快取的字元寬度計算行長度，因為圖像的寬度可能會因內容而異。
-   應用程式應該選擇性地加入由右至左的讀取順序和靠右對齊的支援。
-   複雜字集或精細印刷所需的重新排列和內容處理，需要大幅增加簡單腳本的基本文字顯示處理。 因此，為了避免發生效能問題，您的應用程式在顯示結果並將控制權傳回給使用者之前，不應處理大量的文字。

## <a name="complex-script-processing-using-edit-controls"></a>使用編輯控制項的複雜字集處理

標準的 Windows 編輯控制項已經過擴充，可支援多語系文字和複雜的腳本。 延伸支援包括輸入和顯示，以及透過字元叢集的正確資料指標移動，例如泰文和梵文腳本。 如需詳細資訊，請參閱 [編輯控制項](../controls/edit-controls.md)。

## <a name="complex-script-processing-using-rich-edit-controls"></a>使用 Rich Edit 控制項進行複雜的腳本處理

Rich Edit 3.0 是更高層級的介面集合，利用 Uniscribe 來防止文字版面配置應用程式與特定腳本的複雜度。 Rich Edit 是讓應用程式顯示覆雜腳本的最簡單方式，即使它們的主要用途不一定是文字配置也是一樣。 Rich Edit 可提供快速、多功能的豐富 Unicode 多語系文字和簡單純文字編輯。 它包含廣泛的訊息和 COM 介面、文字編輯、格式化、換行、簡單的資料表配置、垂直文字配置、雙向文字配置、印度文和泰文支援、編輯使用者介面，就像 Microsoft Word 和 Text 物件模型介面一樣。

除了 Rich Edit 介面，應用程式還可以使用 Rich Edit [**TextOut**](/windows/win32/api/wingdi/nf-wingdi-textouta) 函式來自動剖析、成形、定位和分隔線條。 如需詳細資訊，請參閱 [Rich Edit 控制項](../controls/rich-edit-controls.md)。

## <a name="complex-script-processing-using-uniscribe"></a>使用 Uniscribe 進行複雜的腳本處理

[Uniscribe](uniscribe.md) 提供最廣泛的處理文字處理，包括精細的印刷效果和複雜的腳本。 它支援在阿拉伯文、梵文和泰文等腳本中找到的複雜規則。 它會處理由右至左撰寫的腳本，例如阿拉伯文和希伯來文，並支援混合腳本。 Uniscribe 也會公開 [OpenType](opentype-font-format.md) 字型功能，可供應用程式用來控制精細的印刷效果。 如需詳細資訊，請參閱 [處理複雜的腳本](processing-complex-scripts.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Uniscribe](about-uniscribe.md)
</dt> <dt>

[處理複雜的腳本](processing-complex-scripts.md)
</dt> </dl>

 

 

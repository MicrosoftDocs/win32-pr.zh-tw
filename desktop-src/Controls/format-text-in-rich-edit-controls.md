---
title: 如何格式化 Rich Edit 控制項中的文字
description: 應用程式可以將訊息傳送至 rich edit 控制項，以便格式化字元和段落，並取出格式資訊。
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103681604"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a>如何格式化 Rich Edit 控制項中的文字

應用程式可以將訊息傳送至 rich edit 控制項，以便格式化字元和段落，並取出格式資訊。 段落格式化屬性包括對齊、索引標籤、縮排、編號和簡單的資料表。 若為字元，您可以指定字型名稱、大小、色彩和效果，例如粗體、斜體和 protected。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="format-text-in-a-rich-edit-control"></a>格式化 Rich Edit 控制項中的文字

您可以使用 [**EM \_ SETPARAFORMAT**](em-setparaformat.md) 訊息來套用段落格式。 若要判斷所選取文字的目前段落格式，請使用 [**EM \_ GETPARAFORMAT**](em-getparaformat.md) 訊息。 [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)或 [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)結構會與這兩個訊息一起使用，以指定段落格式化屬性。

您可以使用 [**EM \_ SETCHARFORMAT**](em-setcharformat.md) 訊息來套用字元格式。 若要判斷所選取文字的目前字元格式，您可以使用 [**EM \_ GETCHARFORMAT**](em-getcharformat.md) 訊息。 [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)或 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)結構會與這兩個訊息一起使用，以指定字元屬性。

您也可以使用 [**em \_ SETCHARFORMAT**](em-setcharformat.md) 和 [**em \_ GETCHARFORMAT**](em-getcharformat.md) 訊息來設定和取出插入點的字元格式，也就是套用至任何後續插入字元的格式。 例如，如果應用程式將預設的字元格式設定為粗體，而使用者接著輸入字元，則該字元為粗體。

只有當目前的選取範圍是插入點) 時，才會將插入點的字元格式套用至新插入的文字 (。 否則，新的文字會假設它所取代之文字的字元格式。 如果選取範圍變更，則會變更預設的字元格式，以符合新選取範圍中的第一個字元。

受保護的字元效果是唯一的，因為它不會變更文字的外觀。 如果使用者嘗試修改受保護的文字，rich edit 控制項會將 [ \_ 受保護](en-protected.md) 的通知碼傳送給其父視窗，讓父視窗允許或防止變更。 若要接收此通知碼，您必須使用 [**EM \_ SETEVENTMASK**](em-seteventmask.md) 訊息來啟用它。

前景色彩一律是字元屬性。 在 Microsoft Rich Edit 1.0 中，背景色彩只是 Rich edit 控制項的屬性。 若要設定預設的背景色彩，請使用 [**EM \_ SETBKGNDCOLOR**](em-setbkgndcolor.md) 訊息。 請注意，Rich Edit 不支援 [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) 訊息。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





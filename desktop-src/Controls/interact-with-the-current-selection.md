---
title: 如何與目前的選取範圍互動
description: 使用者可以使用滑鼠或鍵盤選取 rich edit 控制項中的文字。
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec776ab0c8e07bb61dcc0e12d13af46b17d094a
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103681603"
---
# <a name="how-to-interact-with-the-current-selection"></a>如何與目前的選取範圍互動

使用者可以使用滑鼠或鍵盤選取 rich edit 控制項中的文字。 *目前的選取* 範圍是選定字元的範圍，或者，如果未選取任何字元，則為插入點的位置。 應用程式可以取得目前選取範圍的相關資訊、設定它、判斷其變更時間，以及顯示或隱藏選取專案反白顯示。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="interact-with-the-current-selection"></a>與目前的選取範圍互動

若要判斷 rich edit 控制項中目前的選取範圍，請使用 [**EM \_ EXGETSEL**](em-exgetsel.md) 訊息。 若要設定目前的選取範圍，請使用 [**EM \_ EXSETSEL**](em-exsetsel.md) 訊息。 [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)結構會與這兩個訊息一起使用，並指定字元範圍。 若要取得目前選取範圍內容的相關資訊，您可以使用 [**EM \_ SELECTIONTYPE**](em-selectiontype.md) 訊息。

應用程式可以藉由處理 [ \_ SELCHANGE](en-selchange.md) 通知程式碼，來偵測目前的選取專案變更的時間。 通知碼會指定 [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) 結構，其中包含新選取專案的相關資訊。 只有當您使用 [**EM \_ SETEVENTMASK**](em-seteventmask.md) 訊息來啟用時，rich edit 控制項才會傳送此通知碼。

根據預設，rich edit 控制項會在取得並失去焦點時，顯示並隱藏選取專案反白顯示。 您可以使用 [**EM \_ HIDESELECTION**](em-hideselection.md) 訊息，隨時顯示或隱藏選取專案反白顯示。 例如，應用程式可能會提供搜尋對話方塊來尋找 rich edit 控制項中的文字。 應用程式可能會在不關閉對話方塊的情況下選取相符的文字，在這種情況下，它必須使用 **EM \_ HIDESELECTION** 訊息來反白顯示選取範圍。

如同編輯控制項，您可以指定 [**ES \_ NOHIDESEL**](edit-control-styles.md) 視窗樣式，以防止 rich edit 控制項在失去焦點時隱藏選取專案反白顯示。

除了使用 [**em \_ EXGETSEL**](em-exgetsel.md) 和 [**em \_ EXSETSEL**](em-exsetsel.md) 訊息以外，您還可以使用 [**em \_ GETSEL**](em-getsel.md) 和 [**em \_ SETSEL**](em-setsel.md) 編輯控制訊息來取得和設定目前的選取範圍。 **EM \_ GETSEL** 訊息會將 2 16 位字元索引封裝至其32位的傳回值，因此只適用于完全落在第一個64k 內的選取專案。 但是，除非您使用 [**em \_ LIMITTEXT**](em-limittext.md) 或 [**em \_ EXLIMITTEXT**](em-exlimittext.md) 訊息來延長此限制，否則 rich Edit 控制項絕不會包含超過32k 個字元的文字。 對於延伸超過前 64 KB 文字的選項， **EM \_ GETSEL** 訊息會傳回–1。 在這種情況下，您仍然可以使用 *wParam* 和 *lParam* 中傳回的值來尋找選取專案的開頭和結尾字元。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





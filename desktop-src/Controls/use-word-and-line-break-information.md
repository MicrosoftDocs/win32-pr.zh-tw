---
title: 如何使用單字和換行資訊
description: Rich edit 控制項會呼叫稱為斷詞程式的函式，以找出單字之間的中斷，以及判斷它可以中斷行的位置。
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb90064e455bfeb8ee126e6107d75ef29b3a4f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106969939"
---
# <a name="how-to-use-word-and-line-break-information"></a>如何使用單字和換行資訊

Rich edit 控制項會呼叫稱為斷詞程式的函式，以找出單字之間的中斷，以及判斷它可以中斷行的位置。 控制項在執行自動換行作業時，以及處理 CTRL + 向左鍵和 CTRL + 向右鍵按鍵組合時，會使用這項資訊。 應用程式可以傳送訊息至 Rich Edit 控制項來取代預設斷字程序、擷取斷字資訊，以及決定指定的字元落在哪一行的位置。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-word-and-line-break-information"></a>使用單字和換行資訊

Rich edit 控制項的斷詞程式與編輯控制項的斷詞程式很類似，但有其他功能：這兩種控制項的斷詞程式都可以判斷字元是否為分隔符號，並可在指定的位置之前或之後找到最接近的單字分隔符號。 分隔符號是標示單字結尾的字元，例如空格。 通常，在編輯控制項中，只會在分隔符號後出現斷字。 不過，不同的規則適用于大部分的亞洲語言。

Rich edit 控制項的斷詞程式也會將字元分組到字元類別，每個字元類別都是由0x00 到0x0F 範圍中的值所識別。 在不同類別的分隔符號或字元之間進行中斷。 因此，有不同類別的英數位元和標點符號字元的斷詞程式，會在) 期間之前和之後的字串 "Win.doc (" 中找到兩個分行符號。

字元的類別可以與零或多個文字分隔旗標結合，以形成8位值。 執行自動換行作業時，rich edit 控制項會使用斷詞旗標來判斷它可以中斷的位置。 Rich Edit 會使用下列文字分隔旗標。



| 旗標            | 描述                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| WBF \_ >BREAKAFTER | 行可能會在字元之後中斷。                                                                                          |
| WBF \_ BREAKLINE  | 字元是分隔符號。 分隔符號標示單字的結尾。 行可能會在分隔符號之後中斷。                            |
| WBF \_ ISWHITE    | 字元是空白字元。 換行時，尾端的空白字元不會包含在行的長度中。 |



 

WBF \_ >breakafter 值是用來允許在未標示單字結尾的字元之後換行，例如連字號。

您可以使用 [**EM \_ SETWORDBREAKPROC**](em-setwordbreakproc.md) 訊息，將 rich edit 控制項的預設斷詞程式取代為您自己的程式。 如需有關斷詞程式的詳細資訊，請參閱 [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) 函數的描述。

> [!Note]  
> 由於多語系斷詞的複雜度，因此不建議 Microsoft Rich Edit 2.0 和更新版本使用此取代。

 

針對 Microsoft Rich Edit 1.0，您可以使用 [**EM \_ SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) 訊息，以 [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) 函式取代預設的擴充字組分隔程式。 此函式會提供文字的其他相關資訊，例如字元集。 您可以使用 [**EM \_ GETWORDBREAKPROCEX**](em-getwordbreakprocex.md) 訊息來取出目前擴充的斷詞程式的位址。 請注意，Microsoft Rich Edit 2.0 和更新版本不支援 *EditWordBreakProcEx*、 **Em \_ GETWORDBREAKPROCEX** 和 **EM \_ SETWORDBREAKPROCEX**。

您可以使用 [**EM \_ FINDWORDBREAK**](em-findwordbreak.md) 訊息來尋找斷詞，或判斷字元的類別和斷詞旗標。 接著，控制項會呼叫它的斷詞程式來取得要求的資訊。

若要判斷指定字元落在哪個行上，您可以使用 [**EM \_ EXLINEFROMCHAR**](em-exlinefromchar.md) 訊息。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 
---
title: 如何使用豐富的編輯文字作業
description: 應用程式可以傳送訊息，以在 rich edit 控制項中取得或尋找文字。 您可以取出選取的文字或指定的文字範圍。
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b54619e1ce5952b7c0d06527c6aca2402a4e714
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933660"
---
# <a name="how-to-use-rich-edit-text-operations"></a>如何使用豐富的編輯文字作業

應用程式可以傳送訊息，以在 rich edit 控制項中取得或尋找文字。 您可以取出選取的文字或指定的文字範圍。

若要在 rich edit 控制項中取得選取的文字，請使用 [**EM \_ GETSELTEXT**](em-getseltext.md) 訊息。 文字會複製到指定的字元陣列。 您必須確定陣列夠大，足以容納選取的文字加上終止的 null 字元。

若要取出指定的文字範圍，請使用 [**EM \_ GETTEXTRANGE**](em-gettextrange.md) 訊息。 與此訊息搭配使用的 [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) 結構會指定要取出的文字範圍，並指向接收文字的字元陣列。 同樣地，應用程式必須確定陣列夠大，足以容納指定的文字加上終止的 null 字元。

您可以使用 [**em \_ FINDTEXT**](em-findtext.md) 或 [**em \_ FINDTEXTEX**](em-findtextex.md) 訊息來搜尋 rich edit 控制項中的字串，或 Unicode 對等的 [**em \_ FINDTEXTW**](em-findtextw.md) 和 [**em \_ FINDTEXTEXW**](em-findtextexw.md)。 與 nonextended 版本搭配使用的 [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) 結構會指定要搜尋的文字範圍，以及要搜尋的字串。 擴充的版本會使用 [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) 結構，此結構會指定相同的資訊，同時也會接收所找到文字之字元範圍的開始和結束點。 您也可以指定這類選項，如同搜尋是否區分大小寫。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-a-rich-edit-text-operation"></a>使用 Rich Edit 文字操作

下列範例函式會在支援 Unicode 的 rich edit 控制項中，找到所選文字內的指定文字。 如果找到目標，則會變成新的選取專案。


```C++
BOOL FindTextInSelection(HWND hRich, WCHAR* target)
{
    CHARRANGE selectionRange;
    
    SendMessage(hRich, EM_EXGETSEL, 0, (LPARAM)&selectionRange);
    
    FINDTEXTEX ftex;
    
    ftex.lpstrText  = target;
    ftex.chrg.cpMin = selectionRange.cpMin;
    ftex.chrg.cpMax = selectionRange.cpMax;
    
    LRESULT lr = SendMessage(hRich, EM_FINDTEXTEXW, (WPARAM)FR_DOWN, (LPARAM) &ftex);
    
    if (lr >= 0)
    {
        LRESULT lr1 = SendMessage(hRich, EM_EXSETSEL, 0, (LPARAM)&ftex.chrgText);
        
        SendMessage(hRich, EM_HIDESELECTION, (LPARAM)FALSE, 0);
        
        return TRUE;
    }
    
    return FALSE;
    
}
```



## <a name="remarks"></a>備註

Microsoft Rich Edit 3.0 也支援 HexToUnicode 輸入方法編輯器 (IME) 函式，可讓使用者使用快速鍵在十六進位和 Unicode 之間進行轉換。 如需詳細資訊，請參閱 [HEXTOUNICODE IME](/windows/desktop/Intl/hextounicode-ime)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 
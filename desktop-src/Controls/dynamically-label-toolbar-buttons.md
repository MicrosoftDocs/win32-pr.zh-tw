---
title: 如何動態標記工具列按鈕
description: 您可以使用 TB SETBUTTONINFO 訊息，將文字指派給現有的按鈕 \_ 。
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063a3b8be8a23dc8cead219c53989a8ff1a40225dc8411f9e8a1b156b6bb55bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877438"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>如何動態標記工具列按鈕

您可以使用 [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) 訊息，將文字指派給現有的按鈕。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="dynamically-label-a-toolbar-button"></a>動態標示工具列按鈕

下列範例示範如何在先前的範例 **中，將** 第三個按鈕的文字變更 **為 [另存新** 檔]。


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a>備註

使用 [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) 來變更按鈕的文字，並不會影響在內部字串清單中指派給該按鈕的字串。

如果您將工具列按鈕字串加入至內部文字清單中，您就無法藉由呼叫 [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md)來取得該字串的索引，而必須改用 [**TB \_ GETBUTTON**](tb-getbutton.md) 訊息。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工具列控制項](using-toolbar-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 





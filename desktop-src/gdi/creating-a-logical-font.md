---
description: 您可以使用 [字型通用] 對話方塊來顯示可用的字型。
ms.assetid: 317ea311-0592-432a-87b5-58296de003aa
title: 建立邏輯字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4398f426ae2dd0f18c21409422dfbcb53f0e6ee8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972725"
---
# <a name="creating-a-logical-font"></a>建立邏輯字型

您可以使用 [ **字型** 通用] 對話方塊來顯示可用的字型。 當應用程式初始化 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的成員並呼叫 [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)函式之後，就會顯示 [ **ChooseFont** ] 對話方塊。 當使用者選取其中一個可用的字型，然後按下 [ **確定]** 按鈕之後， **ChooseFont** 函式會以相關資料初始化 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構。 然後，您的應用程式可以呼叫 [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta) 函式，並根據使用者的要求建立邏輯字型。 下列範例示範如何完成這項操作。


```C++
HFONT FAR PASCAL MyCreateFont( void ) 
{ 
    CHOOSEFONT cf; 
    LOGFONT lf; 
    HFONT hfont; 
 
    // Initialize members of the CHOOSEFONT structure.  
 
    cf.lStructSize = sizeof(CHOOSEFONT); 
    cf.hwndOwner = (HWND)NULL; 
    cf.hDC = (HDC)NULL; 
    cf.lpLogFont = &lf; 
    cf.iPointSize = 0; 
    cf.Flags = CF_SCREENFONTS; 
    cf.rgbColors = RGB(0,0,0); 
    cf.lCustData = 0L; 
    cf.lpfnHook = (LPCFHOOKPROC)NULL; 
    cf.lpTemplateName = (LPSTR)NULL; 
    cf.hInstance = (HINSTANCE) NULL; 
    cf.lpszStyle = (LPSTR)NULL; 
    cf.nFontType = SCREEN_FONTTYPE; 
    cf.nSizeMin = 0; 
    cf.nSizeMax = 0; 
 
    // Display the CHOOSEFONT common-dialog box.  
 
    ChooseFont(&cf); 
 
    // Create a logical font based on the user's  
    // selection and return a handle identifying  
    // that font.  
 
    hfont = CreateFontIndirect(cf.lpLogFont); 
    return (hfont); 
} 
```



 

 

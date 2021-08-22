---
description: 您可以使用 GetTextAlign 和 SetTextAlign 函數來查詢和設定裝置內容的文字對齊方式。
ms.assetid: 7fdfbadb-827a-4b42-9b9a-b9e46389e13c
title: 設定文字對齊方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78edffa9febaee0fd624cc97c4a908da349ad65526799e1c4bd3450137b62a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468418"
---
# <a name="setting-the-text-alignment"></a>設定文字對齊方式

您可以使用 [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) 和 [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) 函數來查詢和設定裝置內容的文字對齊方式。 文字對齊設定會決定文字相對於指定位置的位置。 文字可以對齊位置的右邊或左邊，也可以靠其置中;它也可以對齊在該點的上方或下方。

下列範例顯示的方法可判斷已設定的水準對齊旗標：


```C++
switch ((TA_LEFT | TA_RIGHT | TA_CENTER) & GetTextAlign(hdc)) 
{ 
    case TA_LEFT: 
       . 
       . 
       . 
    case TA_RIGHT: 
       . 
       . 
       . 
    case TA_CENTER: 
       . 
       . 
       . 
} 
```



呼叫文字輸出函式時，您也可以使用 [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) 函數來更新目前的位置。 例如，下列範例會使用 [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) 函數來更新呼叫 [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) 函數時的目前位置。 在此範例中， *cArial* 參數是指定 Arial 字型數目的整數。


```C++
UINT uAlignPrev; 
char szCount[8];
HRESULT hr;
size_t * pcch; 
 
uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
MoveToEx(hdc, 10, 50, (LPPOINT) NULL); 
TextOut(hdc, 0, 0, "Number of Arial fonts: ", 23); 
itoa(cArial, szCount, 10); 

hr = StringCchLength(szCount, 9, pcch);
if (FAILED(hr))
{
// TODO: write error handler 
}
 
TextOut(hdc, 0, 0, (LPSTR) szCount, *pcch); 
SetTextAlign(hdc, uAlignPrev); 
```



> [!Note]  
> 當您使用 ScriptStringOut 時，不應該使用 [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign)搭配 TA \_ UPDATECP，因為無法正確轉譯選取的文字。 [](/windows/win32/api/usp10/nf-usp10-scriptstringout) 如果您必須使用此旗標，您可以視需要取消設定和重設，以避免發生此問題。

 

 

 

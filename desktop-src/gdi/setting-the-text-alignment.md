---
description: 您可以使用 GetTextAlign 和 SetTextAlign 函數來查詢和設定裝置內容的文字對齊方式。
ms.assetid: 7fdfbadb-827a-4b42-9b9a-b9e46389e13c
title: 設定文字對齊方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538a8da060f9d854890ea004c855e2317986fd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973096"
---
# <a name="setting-the-text-alignment"></a><span data-ttu-id="1d062-103">設定文字對齊方式</span><span class="sxs-lookup"><span data-stu-id="1d062-103">Setting the Text Alignment</span></span>

<span data-ttu-id="1d062-104">您可以使用 [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) 和 [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) 函數來查詢和設定裝置內容的文字對齊方式。</span><span class="sxs-lookup"><span data-stu-id="1d062-104">You can query and set the text alignment for a device context by using the [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) and [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) functions.</span></span> <span data-ttu-id="1d062-105">文字對齊設定會決定文字相對於指定位置的位置。</span><span class="sxs-lookup"><span data-stu-id="1d062-105">The text-alignment settings determine how text is positioned relative to a specified location.</span></span> <span data-ttu-id="1d062-106">文字可以對齊位置的右邊或左邊，也可以靠其置中;它也可以對齊在該點的上方或下方。</span><span class="sxs-lookup"><span data-stu-id="1d062-106">Text can be aligned to the right or left of the position or centered over it; it can also be aligned above or below the point.</span></span>

<span data-ttu-id="1d062-107">下列範例顯示的方法可判斷已設定的水準對齊旗標：</span><span class="sxs-lookup"><span data-stu-id="1d062-107">The following example shows a method for determining which horizontal alignment flag is set:</span></span>


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



<span data-ttu-id="1d062-108">呼叫文字輸出函式時，您也可以使用 [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) 函數來更新目前的位置。</span><span class="sxs-lookup"><span data-stu-id="1d062-108">You can also use the [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) function to update the current position when a text-output function is called.</span></span> <span data-ttu-id="1d062-109">例如，下列範例會使用 [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) 函數來更新呼叫 [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) 函數時的目前位置。</span><span class="sxs-lookup"><span data-stu-id="1d062-109">For instance, the following example uses the [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) function to update the current position when the [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) function is called.</span></span> <span data-ttu-id="1d062-110">在此範例中， *cArial* 參數是指定 Arial 字型數目的整數。</span><span class="sxs-lookup"><span data-stu-id="1d062-110">In this example, the *cArial* parameter is an integer that specifies the number of Arial fonts.</span></span>


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
> <span data-ttu-id="1d062-111">當您使用 ScriptStringOut 時，不應該使用 [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign)搭配 TA \_ UPDATECP，因為無法正確轉譯選取的文字。 [](/windows/win32/api/usp10/nf-usp10-scriptstringout)</span><span class="sxs-lookup"><span data-stu-id="1d062-111">You should not use [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) with TA\_UPDATECP when you are using [**ScriptStringOut**](/windows/win32/api/usp10/nf-usp10-scriptstringout), because selected text is not rendered correctly.</span></span> <span data-ttu-id="1d062-112">如果您必須使用此旗標，您可以視需要取消設定和重設，以避免發生此問題。</span><span class="sxs-lookup"><span data-stu-id="1d062-112">If you must use this flag, you can unset and reset it as necessary to avoid the problem.</span></span>

 

 

 

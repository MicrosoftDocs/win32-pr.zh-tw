---
description: 本章節包含範例程式碼，示範如何產生由字元字串組成的剪輯路徑。 此範例會建立邏輯字型，並使用它在剪輯路徑內繪製字串，然後藉由繪製水準和垂直線來填滿路徑。
ms.assetid: c71727aa-f4a3-409e-b50f-709eb4dbdaab
title: 使用裁剪
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f54e4dee790d2891ebf36fb90ff9996b624d3c4d8d053fecae8397a38e043bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037486"
---
# <a name="using-clipping"></a>使用裁剪

本章節包含範例程式碼，示範如何產生由字元字串組成的剪輯路徑。 此範例會建立邏輯字型，並使用它在剪輯路徑內繪製字串，然後藉由繪製水準和垂直線來填滿路徑。


```C++
// DoClipPat - Draws a clip path using the specified string  
// Return value - TRUE if successful; FALSE otherwise  
// lplf - address of a LOGFONT structure that defines the font to  
//        use to draw the clip path  
// lpsz - address of a string to use for the clip path  
 
BOOL DoClipPath(LPLOGFONT lplf, LPSTR lpsz) 
{ 
    LOGFONT lf;           // logical font structure  
    HFONT hfont;          // new logical font handle  
    HFONT hfontOld;       // original logical font handle  
    HDC hdc;              // display DC handle  
    int nXStart, nYStart; // drawing coordinates  
    RECT rc;              // rectangle structure for painting window  
    SIZE sz;              // size structure that receives text extents  
    int nStrLen;          // length of the string  
    int i;                // loop counter  
        HRESULT hr;
        size_t * pcch;
 
    // Retrieve a cached DC for the window.  
 
    hdc = GetDC(hwnd); 
 
    // Erase the current window contents.  
 
    GetClientRect(hwnd, &rc); 
    FillRect(hdc, &rc, GetStockObject(WHITE_BRUSH)); 
 
    // Use the specified font to create a logical font and select it  
    // into the DC.  
 
    hfont = CreateFontIndirect(lplf); 
    if (hfont == NULL) 
        return FALSE; 
    hfontOld = SelectObject(hdc, hfont); 
 
    // Create a clip path.  
 
        hr = StringCchLength(lpsz, STRSAFE_MAX_CCH, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
        nStrLen = *pcch 
    BeginPath(hdc); 
        TextOut(hdc, nXStart, nYStart, lpsz, nStrLen); 
    EndPath(hdc); 
    SelectClipPath(hdc, RGN_DIFF); 
 
    // Retrieve the dimensions of the rectangle surrounding  
    // the text.  
 
    GetTextExtentPoint32(hdc, lpsz, nStrLen, &sz); 
 
    // Draw horizontal lines through the clip path.  
 
    for (i = nYStart + 1; i < (nYStart + sz.cy); i += 3) 
    { 
       MoveToEx(hdc, nXStart, i, (LPPOINT) NULL); 
       LineTo(hdc, (nXStart + sz.cx), i); 
    } 
 
    // Draw vertical lines through the clip path.  
 
    for (i = nXStart + 1; i < (nXStart + sz.cx); i += 3)
    { 
       MoveToEx(hdc, i, nYStart, (LPPOINT) NULL); 
       LineTo(hdc, i, (nYStart + sz.cy)); 
    } 
 
    // Select the original font into the DC and release the DC.  
 
    SelectObject(hdc, hfontOld); 
    DeleteObject(hfont); 
    ReleaseDC(hwnd, hdc); 
 
    return TRUE; 
} 
```



如需示範應用程式如何建立矩形裁剪區域的範例，請參閱 [區域](regions.md)。

 

 




---
description: 本章節包含的範例示範如何建立圖片，以及將對應的記錄儲存在中繼檔中的處理常式。
ms.assetid: 8be95fef-93dc-4c9c-a0d3-840918c00e43
title: 顯示圖片並將其儲存在增強的中繼檔中
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8eee65f2f82a7b8ccdad86e99987df6a06a4f5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691895"
---
# <a name="displaying-a-picture-and-storing-it-in-an-enhanced-metafile"></a><span data-ttu-id="c1586-103">顯示圖片並將其儲存在增強的中繼檔中</span><span class="sxs-lookup"><span data-stu-id="c1586-103">Displaying a Picture and Storing It in an Enhanced Metafile</span></span>

<span data-ttu-id="c1586-104">本章節包含的範例示範如何建立圖片，以及將對應的記錄儲存在中繼檔中的處理常式。</span><span class="sxs-lookup"><span data-stu-id="c1586-104">This section contains an example demonstrating the creation of a picture and the process of storing the corresponding records in a metafile.</span></span> <span data-ttu-id="c1586-105">此範例會將圖片繪製到顯示，或儲存在中繼檔中。</span><span class="sxs-lookup"><span data-stu-id="c1586-105">The example draws a picture to the display or stores it in a metafile.</span></span> <span data-ttu-id="c1586-106">如果有提供顯示裝置內容控制碼，它會使用各種 GDI 函式，將圖片繪製到螢幕。</span><span class="sxs-lookup"><span data-stu-id="c1586-106">If a display device context handle is given, it draws a picture to the screen using various GDI functions.</span></span> <span data-ttu-id="c1586-107">如果指定了增強的中繼檔裝置內容，它就會將相同的圖片儲存在增強的中繼檔中。</span><span class="sxs-lookup"><span data-stu-id="c1586-107">If an enhanced metafile device context is given, it stores the same picture in the enhanced metafile.</span></span>


```C++
void DrawOrStore(HWND hwnd, HDC hdcMeta, HDC hdcDisplay) 
{ 
 
RECT rect; 
HDC hDC; 
int fnMapModeOld; 
HBRUSH hbrOld; 
 
// Draw it to the display DC or store it in the metafile device context.  
 
if (hdcMeta) 
    hDC = hdcMeta; 
else 
    hDC = hdcDisplay; 
 
// Set the mapping mode in the device context.  
 
fnMapModeOld = SetMapMode(hDC, MM_LOENGLISH); 
 
// Find the midpoint of the client area.  
 
GetClientRect(hwnd, (LPRECT)&rect); 
DPtoLP(hDC, (LPPOINT)&rect, 2); 
 
// Select a gray brush.  
 
hbrOld = SelectObject(hDC, GetStockObject(GRAY_BRUSH)); 
 
// Draw a circle with a one inch radius.  
 
Ellipse(hDC, (rect.right/2 - 100), (rect.bottom/2 + 100), 
       (rect.right/2 + 100), (rect.bottom/2 - 100)); 
 
// Perform additional drawing here.  
 
 
 
// Set the device context back to its original state.  
 
SetMapMode(hDC, fnMapModeOld); 
SelectObject(hDC, hbrOld); 
} 
```



 

 




---
title: 如何繪製影像
description: 本主題將示範如何使用 ImageList \_ draw 函數來繪製影像。
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7b42e97ad9b7cab8693431654dc31b473267414f31ae5811f4f66a6663ce8e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878328"
---
# <a name="how-to-draw-an-image"></a>如何繪製影像

本主題將示範如何使用 [**ImageList \_ draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 函數來繪製影像。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示


若要繪製影像，請使用 [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 或 [**imagelist \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) 函數。 您可以指定影像清單的控制碼、要繪製之影像的索引、目的地裝置內容的控制碼、裝置內容中的位置，以及一或多個繪製樣式。

下列 c + + 程式碼範例中的使用者定義函數會使用 [**ImageList \_ draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 函式來繪製影像，並儲存影像周框的用戶端座標。 後續的函式會使用周框來判斷使用者是否已按一下影像。



```C++
// DrawTheImage - draws an image transparently and saves 
// the bounding rectangle of the drawn image.
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which to draw the image. 
// himl - handle to the image list that contains the image. 
// cx and cy - client coordinates for the upper-left corner of the image. 
// 
// Global variables and constants 
//     g_nImage - index of the image to draw. 
//     g_rcImage - bounding rectangle of the image. 
//     CX_IMAGE and CY_IMAGE - width and height of the image. 
extern int g_nImage; 
extern RECT g_rcImage; 
 
#define CX_IMAGE 32 
#define CY_IMAGE 32 
 
BOOL DrawTheImage(HWND hwnd, HIMAGELIST himl, int cx, int cy) 
{ 
    HDC hdc; 
 
    if ((hdc = GetDC(hwnd)) == NULL) 
        return FALSE; 
    if (!ImageList_Draw(himl, g_nImage, hdc, cx, cy, ILD_TRANSPARENT)) 
        return FALSE; 
    ReleaseDC(hwnd, hdc); 
 
    SetRect(&g_rcImage, cx, cy, CX_IMAGE + cx, CY_IMAGE + cy); 
 
    return TRUE; 
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[影像清單參考](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[關於影像清單](image-lists.md)
</dt> <dt>

[使用影像清單](using-image-lists.md)
</dt> </dl>

 

 





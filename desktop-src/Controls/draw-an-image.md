---
title: 如何繪製影像
description: 本主題將示範如何使用 ImageList \_ draw 函數來繪製影像。
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac13eef2eb5bc55866ac2fd930db5494f2683dd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933748"
---
# <a name="how-to-draw-an-image"></a><span data-ttu-id="53b5a-103">如何繪製影像</span><span class="sxs-lookup"><span data-stu-id="53b5a-103">How to Draw an Image</span></span>

<span data-ttu-id="53b5a-104">本主題將示範如何使用 [**ImageList \_ draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 函數來繪製影像。</span><span class="sxs-lookup"><span data-stu-id="53b5a-104">This topic demonstrates how to use the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) function to draw an image.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="53b5a-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="53b5a-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="53b5a-106">技術</span><span class="sxs-lookup"><span data-stu-id="53b5a-106">Technologies</span></span>

-   [<span data-ttu-id="53b5a-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="53b5a-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="53b5a-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="53b5a-108">Prerequisites</span></span>

-   <span data-ttu-id="53b5a-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="53b5a-109">C/C++</span></span>
-   <span data-ttu-id="53b5a-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="53b5a-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="53b5a-111">指示</span><span class="sxs-lookup"><span data-stu-id="53b5a-111">Instructions</span></span>


<span data-ttu-id="53b5a-112">若要繪製影像，請使用 [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 或 [**imagelist \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) 函數。</span><span class="sxs-lookup"><span data-stu-id="53b5a-112">To draw an image, you use the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) or [**ImageList\_DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) function.</span></span> <span data-ttu-id="53b5a-113">您可以指定影像清單的控制碼、要繪製之影像的索引、目的地裝置內容的控制碼、裝置內容中的位置，以及一或多個繪製樣式。</span><span class="sxs-lookup"><span data-stu-id="53b5a-113">You specify the handle to an image list, the index of the image to draw, the handle to the destination device context, a location within the device context, and one or more drawing styles.</span></span>

<span data-ttu-id="53b5a-114">下列 c + + 程式碼範例中的使用者定義函數會使用 [**ImageList \_ draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 函式來繪製影像，並儲存影像周框的用戶端座標。</span><span class="sxs-lookup"><span data-stu-id="53b5a-114">The user-defined function in the following C++ code example uses the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) function to draw an image and saves the client coordinates of the image's bounding rectangle.</span></span> <span data-ttu-id="53b5a-115">後續的函式會使用周框來判斷使用者是否已按一下影像。</span><span class="sxs-lookup"><span data-stu-id="53b5a-115">A subsequent function uses the bounding rectangle to determine whether the user has clicked on the image.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="53b5a-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="53b5a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53b5a-117">影像清單參考</span><span class="sxs-lookup"><span data-stu-id="53b5a-117">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="53b5a-118">關於影像清單</span><span class="sxs-lookup"><span data-stu-id="53b5a-118">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="53b5a-119">使用影像清單</span><span class="sxs-lookup"><span data-stu-id="53b5a-119">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 





---
title: 如何初始化影像清單
description: 樹狀檢視控制項中的每個專案都可以有兩個相關聯的影像。
ms.assetid: 3683DB35-D70F-4181-9181-95354599B9FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011d789da4eec39febae9d93436e23c23fa59507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092554"
---
# <a name="how-to-initialize-the-image-list"></a><span data-ttu-id="ff04d-103">如何初始化影像清單</span><span class="sxs-lookup"><span data-stu-id="ff04d-103">How to Initialize the Image List</span></span>

<span data-ttu-id="ff04d-104">樹狀檢視控制項中的每個專案都可以有兩個相關聯的影像。</span><span class="sxs-lookup"><span data-stu-id="ff04d-104">Every item in a tree-view control can have two images associated with it.</span></span> <span data-ttu-id="ff04d-105">專案會在選取時顯示一個影像，另一個則不會顯示。</span><span class="sxs-lookup"><span data-stu-id="ff04d-105">An item displays one image when it is selected and the other when it is not.</span></span> <span data-ttu-id="ff04d-106">若要包含具有樹狀檢視專案的影像，請先使用 [影像](image-lists.md) 清單函式來建立影像清單，並在其中新增影像。</span><span class="sxs-lookup"><span data-stu-id="ff04d-106">To include images with tree-view items, first use the [Image Lists](image-lists.md) functions to create an image list and add images to it.</span></span> <span data-ttu-id="ff04d-107">然後使用 [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) 訊息，將影像清單與樹狀檢視控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ff04d-107">Then associate the image list with the tree-view control by using the [**TVM\_SETIMAGELIST**](tvm-setimagelist.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ff04d-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="ff04d-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ff04d-109">技術</span><span class="sxs-lookup"><span data-stu-id="ff04d-109">Technologies</span></span>

-   [<span data-ttu-id="ff04d-110">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="ff04d-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ff04d-111">必要條件</span><span class="sxs-lookup"><span data-stu-id="ff04d-111">Prerequisites</span></span>

-   <span data-ttu-id="ff04d-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="ff04d-112">C/C++</span></span>
-   <span data-ttu-id="ff04d-113">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="ff04d-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ff04d-114">指示</span><span class="sxs-lookup"><span data-stu-id="ff04d-114">Instructions</span></span>

### <a name="initialize-the-image-list"></a><span data-ttu-id="ff04d-115">初始化影像清單</span><span class="sxs-lookup"><span data-stu-id="ff04d-115">Initialize the Image List</span></span>

<span data-ttu-id="ff04d-116">下列範例會建立影像清單、將三個位圖新增至清單，並將影像清單與樹狀檢視控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ff04d-116">The following example creates an image list, adds three bitmaps to the list, and associates the image list with a tree-view control.</span></span>


```C++
// InitTreeViewImageLists - creates an image list, adds three bitmaps 
// to it, and associates the image list with a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 
//
// Global variables and constants: 
// g_hInst - the global instance handle.
// g_nOpen, g_nClosed, and g_nDocument - global indexes of the images. 
// CX_BITMAP and CY_BITMAP - width and height of an icon. 
// NUM_BITMAPS - number of bitmaps to add to the image list. 
// IDB_OPEN_FILE, IDB_CLOSED_FILE, IDB_DOCUMENT -
//     resource identifiers of the bitmaps.

BOOL InitTreeViewImageLists(HWND hwndTV) 
{ 
    HIMAGELIST himl;  // handle to image list 
    HBITMAP hbmp;     // handle to bitmap 

    // Create the image list. 
    if ((himl = ImageList_Create(CX_BITMAP, 
                                 CY_BITMAP,
                                 FALSE, 
                                 NUM_BITMAPS, 0)) == NULL) 
        return FALSE; 

    // Add the open file, closed file, and document bitmaps. 
    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_OPEN_FILE)); 
    g_nOpen = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_CLOSED_FILE)); 
    g_nClosed = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_DOCUMENT)); 
    g_nDocument = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    // Fail if not all of the images were added. 
    if (ImageList_GetImageCount(himl) < 3) 
        return FALSE; 

    // Associate the image list with the tree-view control. 
    TreeView_SetImageList(hwndTV, himl, TVSIL_NORMAL); 

    return TRUE; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="ff04d-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff04d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff04d-118">使用 Tree-View 控制項</span><span class="sxs-lookup"><span data-stu-id="ff04d-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="ff04d-119">CustDTv 範例說明 Tree-View 控制項中的自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="ff04d-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 





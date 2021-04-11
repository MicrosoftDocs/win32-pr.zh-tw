---
title: 如何建立影像清單
description: 本主題將示範如何使用 ImageList \_ create 函數來建立影像清單。
ms.assetid: 6092C555-B5B6-49DB-B07B-684EDB890761
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c81ff3a46138c210474a1b00ddd2ba647d1368
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933739"
---
# <a name="how-to-create-an-image-list"></a><span data-ttu-id="766f4-103">如何建立影像清單</span><span class="sxs-lookup"><span data-stu-id="766f4-103">How to Create an Image List</span></span>

<span data-ttu-id="766f4-104">本主題將示範如何使用 [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 函數來建立影像清單。</span><span class="sxs-lookup"><span data-stu-id="766f4-104">This topic demonstrates how to use the [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) function to create an image list.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="766f4-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="766f4-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="766f4-106">技術</span><span class="sxs-lookup"><span data-stu-id="766f4-106">Technologies</span></span>

-   [<span data-ttu-id="766f4-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="766f4-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="766f4-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="766f4-108">Prerequisites</span></span>

-   <span data-ttu-id="766f4-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="766f4-109">C/C++</span></span>
-   <span data-ttu-id="766f4-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="766f4-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="766f4-111">指示</span><span class="sxs-lookup"><span data-stu-id="766f4-111">Instructions</span></span>


<span data-ttu-id="766f4-112">您可以藉由呼叫 [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 函數來建立影像清單。</span><span class="sxs-lookup"><span data-stu-id="766f4-112">You create an image list by calling the [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) function.</span></span> <span data-ttu-id="766f4-113">這些參數包含要建立的影像清單類型、每個影像的維度，以及您想要新增至清單的影像數目。</span><span class="sxs-lookup"><span data-stu-id="766f4-113">The parameters include the type of image list to create, the dimensions of each image, and the number of images that you intend to add to the list.</span></span>

<span data-ttu-id="766f4-114">下列範例會建立遮罩影像清單，並使用 [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) 宏將兩個圖示新增至清單中。</span><span class="sxs-lookup"><span data-stu-id="766f4-114">The following example creates a masked image list and uses the [**ImageList\_AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) macro to add two icons to the list.</span></span>



```C++
// AddIconsToImageList - creates a masked image list and adds some 
// icons to it. 
// Returns the handle to the new image list. 
// hinst - handle to the application instance. 
// 
// Global variables and constants 
//     g_nBird and g_nTree - indexes of the images. 
//     cx_icon and cy_icon - width and height of the icon. 
//     num_icons - number of icons to add to the image list. 
extern int g_nBird, g_nTree; 
 
#define CX_ICON  32 
#define CY_ICON  32 
#define NUM_ICONS 3 
 
HIMAGELIST AddIconsToImageList(HINSTANCE hinst) 
{ 
    HIMAGELIST himlIcons;  // handle to new image list 
    HICON hicon;           // handle to icon 
 
    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Create a masked image list large enough to hold the icons. 
    himlIcons = ImageList_Create(CX_ICON, CY_ICON, ILC_MASK, NUM_ICONS, 0); 
 
    // Load the icon resources, and add the icons to the image list. 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_BIRD)); 
    g_nBird = ImageList_AddIcon(himlIcons, hicon); 
 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_TREE)); 
    g_nTree = ImageList_AddIcon(himlIcons, hicon); 
 
    return himlIcons; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="766f4-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="766f4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="766f4-116">影像清單參考</span><span class="sxs-lookup"><span data-stu-id="766f4-116">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="766f4-117">關於影像清單</span><span class="sxs-lookup"><span data-stu-id="766f4-117">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="766f4-118">使用影像清單</span><span class="sxs-lookup"><span data-stu-id="766f4-118">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 





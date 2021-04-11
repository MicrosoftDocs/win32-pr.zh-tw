---
title: 如何建立 Tree-View 控制項
description: 若要建立樹狀檢視控制項，請使用 CreateWindowEx 函式，指定 \_ window 類別的 WC TREEVIEW 值。
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093391"
---
# <a name="how-to-create-a-tree-view-control"></a><span data-ttu-id="8ea99-103">如何建立 Tree-View 控制項</span><span class="sxs-lookup"><span data-stu-id="8ea99-103">How to Create a Tree-View Control</span></span>

<span data-ttu-id="8ea99-104">若要建立樹狀檢視控制項，請使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，指定 window 類別的 [**WC \_ TREEVIEW**](common-control-window-classes.md) 值。</span><span class="sxs-lookup"><span data-stu-id="8ea99-104">To create a tree-view control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_TREEVIEW**](common-control-window-classes.md) value for the window class.</span></span> <span data-ttu-id="8ea99-105">載入通用控制項 DLL 時，會在應用程式的位址空間中註冊樹狀檢視視窗類別。</span><span class="sxs-lookup"><span data-stu-id="8ea99-105">The tree-view window class is registered in the application's address space when the common control DLL is loaded.</span></span> <span data-ttu-id="8ea99-106">若要確定已載入 DLL，請使用 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) 函數。</span><span class="sxs-lookup"><span data-stu-id="8ea99-106">To ensure that the DLL is loaded, use the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8ea99-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="8ea99-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8ea99-108">技術</span><span class="sxs-lookup"><span data-stu-id="8ea99-108">Technologies</span></span>

-   [<span data-ttu-id="8ea99-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="8ea99-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8ea99-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="8ea99-110">Prerequisites</span></span>

-   <span data-ttu-id="8ea99-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="8ea99-111">C/C++</span></span>
-   <span data-ttu-id="8ea99-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="8ea99-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8ea99-113">指示</span><span class="sxs-lookup"><span data-stu-id="8ea99-113">Instructions</span></span>

### <a name="create-an-instance-of-a-tree-view-control"></a><span data-ttu-id="8ea99-114">建立 Tree-View 控制項的實例</span><span class="sxs-lookup"><span data-stu-id="8ea99-114">Create an Instance of a Tree-View Control</span></span>

<span data-ttu-id="8ea99-115">下列範例會建立一個樹狀檢視控制項，其大小調整為符合父視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="8ea99-115">The following example creates a tree-view control that is sized to fit the client area of the parent window.</span></span> <span data-ttu-id="8ea99-116">它也會使用應用程式定義的函式，將影像清單與控制項建立關聯，並將專案加入控制項。</span><span class="sxs-lookup"><span data-stu-id="8ea99-116">It also uses application-defined functions to associate an image list with the control and add items to the control.</span></span>


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a><span data-ttu-id="8ea99-117">備註</span><span class="sxs-lookup"><span data-stu-id="8ea99-117">Remarks</span></span>

<span data-ttu-id="8ea99-118">當您建立樹狀檢視控制項時，您也可以將 [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) 訊息傳送給它，以設定要用於文字的字型。</span><span class="sxs-lookup"><span data-stu-id="8ea99-118">When you create a tree-view control, you can also send it a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to set the font to be used for the text.</span></span> <span data-ttu-id="8ea99-119">您應該先傳送此訊息，然後再插入任何專案。</span><span class="sxs-lookup"><span data-stu-id="8ea99-119">You should send this message before inserting any items.</span></span> <span data-ttu-id="8ea99-120">根據預設，樹狀檢視會使用圖示標題字型。</span><span class="sxs-lookup"><span data-stu-id="8ea99-120">By default, a tree view uses the icon title font.</span></span> <span data-ttu-id="8ea99-121">雖然您可以使用 [自訂繪製](custom-draw.md)來自訂每個專案的字型，但是樹狀檢視控制項會使用 **WM \_ SETFONT** 訊息所指定的字型維度來判斷間距和配置。</span><span class="sxs-lookup"><span data-stu-id="8ea99-121">Although you can customize the font per-item by using [Custom Draw](custom-draw.md), the tree-view control uses the dimensions of the font specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ea99-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ea99-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ea99-123">使用 Tree-View 控制項</span><span class="sxs-lookup"><span data-stu-id="8ea99-123">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="8ea99-124">CustDTv 範例說明 Tree-View 控制項中的自訂繪圖</span><span class="sxs-lookup"><span data-stu-id="8ea99-124">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 
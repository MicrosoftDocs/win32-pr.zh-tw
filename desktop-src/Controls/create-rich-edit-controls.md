---
title: 如何建立 Rich Edit 控制項
description: 若要建立 rich edit 控制項，請呼叫 CreateWindowEx 函數，並指定 rich edit 視窗類別。
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024144"
---
# <a name="how-to-create-rich-edit-controls"></a><span data-ttu-id="9a260-103">如何建立 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="9a260-103">How to Create Rich Edit Controls</span></span>

<span data-ttu-id="9a260-104">若要建立 rich edit 控制項，請呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數，並指定 rich edit 視窗類別。</span><span class="sxs-lookup"><span data-stu-id="9a260-104">To create a rich edit control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the rich edit window class.</span></span> <span data-ttu-id="9a260-105">若為 Microsoft Rich Edit 4.1 (Msftedit.dll) ，請 \_ 將 Msftedit.dll 類別指定為 window 類別。</span><span class="sxs-lookup"><span data-stu-id="9a260-105">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT\_CLASS as the window class.</span></span> <span data-ttu-id="9a260-106">針對所有先前的版本，請指定 RICHEDIT \_ 類別。</span><span class="sxs-lookup"><span data-stu-id="9a260-106">For all previous versions, specify RICHEDIT\_CLASS.</span></span> <span data-ttu-id="9a260-107">如需詳細資訊，請參閱 [Rich Edit 的版本](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="9a260-107">For more information, see [Versions of Rich Edit](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="9a260-108">Rich edit 控制項支援大部分與編輯控制項搭配使用的視窗樣式，以及額外的樣式。</span><span class="sxs-lookup"><span data-stu-id="9a260-108">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="9a260-109">如果您想要在控制項中允許一個以上的文字，您應該指定 [**ES \_ 多**](edit-control-styles.md) 行的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="9a260-109">You should specify the [**ES\_MULTILINE**](edit-control-styles.md) window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="9a260-110">如需詳細資訊，請參閱 [Rich Edit 控制項樣式](rich-edit-control-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="9a260-110">For more information, see [Rich Edit Control Styles](rich-edit-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9a260-111">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="9a260-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9a260-112">技術</span><span class="sxs-lookup"><span data-stu-id="9a260-112">Technologies</span></span>

-   [<span data-ttu-id="9a260-113">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="9a260-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9a260-114">必要條件</span><span class="sxs-lookup"><span data-stu-id="9a260-114">Prerequisites</span></span>

-   <span data-ttu-id="9a260-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="9a260-115">C/C++</span></span>
-   <span data-ttu-id="9a260-116">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="9a260-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9a260-117">指示</span><span class="sxs-lookup"><span data-stu-id="9a260-117">Instructions</span></span>

### <a name="create-a-rich-edit-control"></a><span data-ttu-id="9a260-118">建立 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="9a260-118">Create a Rich Edit Control</span></span>

<span data-ttu-id="9a260-119">下列範例函式會建立 rich edit 控制項，並使用一些文字將它初始化。</span><span class="sxs-lookup"><span data-stu-id="9a260-119">The following example function creates a rich edit control and initializes it with some text.</span></span>


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



<span data-ttu-id="9a260-120">在 Microsoft Visual Studio 2005 和更新版本中，您可以從 [工具箱] 拖曳控制項，將 rich edit 控制項新增至對話方塊範本。</span><span class="sxs-lookup"><span data-stu-id="9a260-120">In Microsoft Visual Studio 2005 and later, it is possible to add a rich edit control into a dialog template by dragging the control from the toolbox.</span></span> <span data-ttu-id="9a260-121">不過，在對話方塊編輯器中執行此操作，並無法確保在建立控制項之前，將會載入所需的程式庫。</span><span class="sxs-lookup"><span data-stu-id="9a260-121">However, doing this in the dialog editor does not ensure that the required library will be loaded before the control is created.</span></span> <span data-ttu-id="9a260-122">必須先呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式來載入 Riched32.dll、Riched20.dll 或 Msftedit.dll，才能建立對話方塊。</span><span class="sxs-lookup"><span data-stu-id="9a260-122">It is necessary to call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Riched32.dll, Riched20.dll, or Msftedit.dll before the dialog is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a260-123">備註</span><span class="sxs-lookup"><span data-stu-id="9a260-123">Remarks</span></span>

<span data-ttu-id="9a260-124">若要搭配這些控制項使用視覺化樣式，應用程式必須包含資訊清單，而且必須在程式的開頭呼叫 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) 函式。</span><span class="sxs-lookup"><span data-stu-id="9a260-124">To use visual styles with these controls, an application must include a manifest and must call the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function at the beginning of the program.</span></span> <span data-ttu-id="9a260-125">如需視覺化樣式的詳細資訊，請參閱 [視覺化樣式](themes-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="9a260-125">For information on visual styles, see [Visual Styles](themes-overview.md).</span></span> <span data-ttu-id="9a260-126">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="9a260-126">For information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a260-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a260-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a260-128">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="9a260-128">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="9a260-129">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="9a260-129">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 
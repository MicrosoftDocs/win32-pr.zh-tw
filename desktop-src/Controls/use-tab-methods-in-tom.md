---
title: 如何在 TOM 中使用 Tab 方法
description: 下列範例提供的 C 函式說明如何使用 Text 物件模型中的 tab 方法 (TOM) 。
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9851b30fdf58c0d4200600c0c4c83c7f9a00a555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103841996"
---
# <a name="how-to-use-tab-methods-in-tom"></a><span data-ttu-id="ed572-103">如何在 TOM 中使用 Tab 方法</span><span class="sxs-lookup"><span data-stu-id="ed572-103">How to Use Tab Methods in TOM</span></span>

<span data-ttu-id="ed572-104">下列範例提供的 C 函式說明如何使用 Text 物件模型中的 tab 方法 (TOM) 。</span><span class="sxs-lookup"><span data-stu-id="ed572-104">The following example provides C functions that illustrate the use of the tab methods in the Text Object Model (TOM).</span></span> <span data-ttu-id="ed572-105">假設大部分的應用程式都包含工具列，以顯示目前所選取段落的目前位置和索引標籤類型。</span><span class="sxs-lookup"><span data-stu-id="ed572-105">It is assumed that most applications include a toolbar that shows the current position and type of the tabs for the currently selected paragraph.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ed572-106">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="ed572-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ed572-107">技術</span><span class="sxs-lookup"><span data-stu-id="ed572-107">Technologies</span></span>

-   [<span data-ttu-id="ed572-108">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="ed572-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ed572-109">必要條件</span><span class="sxs-lookup"><span data-stu-id="ed572-109">Prerequisites</span></span>

-   <span data-ttu-id="ed572-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="ed572-110">C/C++</span></span>
-   <span data-ttu-id="ed572-111">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="ed572-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ed572-112">指示</span><span class="sxs-lookup"><span data-stu-id="ed572-112">Instructions</span></span>

### <a name="use-a-tab-method"></a><span data-ttu-id="ed572-113">使用 Tab 方法</span><span class="sxs-lookup"><span data-stu-id="ed572-113">Use a Tab Method</span></span>

<span data-ttu-id="ed572-114">下列程式碼範例示範如何使用目前的索引標籤詳細資料來更新工具列。</span><span class="sxs-lookup"><span data-stu-id="ed572-114">The following code example demonstrates how to update a toolbar with the current tab details.</span></span>


```C++
HRESULT UpdateToolbar(ITextSelection *pSel)
{
    HRESULT hr       = S_OK;        
    ITextPara *pPara = 0;
    
    float f;
    long tbt;            // tab type
    long tbp;

    hr = pSel->GetPara(&pPara);
    
    if (FAILED(hr))
        goto cleanup;    // Paragraph properties are not supported
    
    f = (float) -1.0;    // Start at beginning
    
    while (pPara->GetTab(tbgoNext, &f, &tbt, NULL) == S_OK)
    {
            // Do something like draw tab icon on toolbar here
            // DrawTabPicture(f, tbt);
    }
    
cleanup:

    if (pPara)
        pPara->Release();
        
    return hr;
    
}
```



### <a name="copy-tab-information"></a><span data-ttu-id="ed572-115">複製索引標籤資訊</span><span class="sxs-lookup"><span data-stu-id="ed572-115">Copy Tab Information</span></span>

<span data-ttu-id="ed572-116">下列範例顯示如何只將索引標籤資訊從一個 [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) 介面複製到另一個介面。</span><span class="sxs-lookup"><span data-stu-id="ed572-116">The following example shows how to copy only the tab information from one [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) interface to another.</span></span> <span data-ttu-id="ed572-117">它會採用兩個參數： **ITextPara** \* *pParaFrom* (要複製索引標籤的段落) 和 **ITextPara** \* *pParaFrom* () 複製索引標籤的段落。</span><span class="sxs-lookup"><span data-stu-id="ed572-117">It takes two parameters: **ITextPara** \* *pParaFrom* (the paragraph from which to copy tabs) and **ITextPara** \* *pParaFrom* (the paragraph to which to copy tabs).</span></span>


```C++
HRESULT CopyOnlyTabs(ITextPara *pParaFrom, ITextPara *pParaTo)
{
    float f;
    short tbt;
    short style;
     
    pParaTo->ClearAllTabs();
    
    f = (float) -1.0;
    
    while (pParaFrom->GetTab(tbgoNext, &f, &tbt, &style) == S_OK)
        pParaTo->AddTab(f, tbt, style);
        
    return S_OK;                
    
}
```



## <a name="related-topics"></a><span data-ttu-id="ed572-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed572-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed572-119">使用 Text 物件模型</span><span class="sxs-lookup"><span data-stu-id="ed572-119">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="ed572-120">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="ed572-120">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="ed572-121">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="ed572-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 





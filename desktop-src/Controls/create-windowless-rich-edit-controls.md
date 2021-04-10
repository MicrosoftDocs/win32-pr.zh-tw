---
title: 如何提供視窗功能的無視窗 Rich Edit 控制項
description: 視窗功能包括接收訊息的能力，以及要在其中繪製之裝置內容的擁有權。 無視窗的 rich edit 控制項可透過一對介面 ITextServices 和 ITextHost 來接收這項功能。
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce987630c21b1e15a2237066b39dd264125a857
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "103933025"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a><span data-ttu-id="73280-104">如何提供視窗功能的無視窗 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="73280-104">How to Provide Windowless Rich Edit Controls with Window Functionality</span></span>

<span data-ttu-id="73280-105">視窗功能包括接收訊息的能力，以及要在其中繪製之裝置內容的擁有權。</span><span class="sxs-lookup"><span data-stu-id="73280-105">Window functionality includes the ability to receive messages and the ownership of a device context into which to draw.</span></span> <span data-ttu-id="73280-106">無視窗的 rich edit 控制項可透過一對介面接收這項功能： [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) 和 [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)。</span><span class="sxs-lookup"><span data-stu-id="73280-106">Windowless rich edit controls receive this functionality by way of a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="73280-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="73280-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="73280-108">技術</span><span class="sxs-lookup"><span data-stu-id="73280-108">Technologies</span></span>

-   [<span data-ttu-id="73280-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="73280-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="73280-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="73280-110">Prerequisites</span></span>

-   <span data-ttu-id="73280-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="73280-111">C/C++</span></span>
-   <span data-ttu-id="73280-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="73280-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="73280-113">指示</span><span class="sxs-lookup"><span data-stu-id="73280-113">Instructions</span></span>

### <a name="establish-the-window-functionality"></a><span data-ttu-id="73280-114">建立視窗功能</span><span class="sxs-lookup"><span data-stu-id="73280-114">Establish the Window Functionality</span></span>

<span data-ttu-id="73280-115">下列範例程式碼示範如何建立文字主機和文字服務。</span><span class="sxs-lookup"><span data-stu-id="73280-115">The following example code demonstrates how to create the text host and text services.</span></span>


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a><span data-ttu-id="73280-116">備註</span><span class="sxs-lookup"><span data-stu-id="73280-116">Remarks</span></span>

<span data-ttu-id="73280-117">程式碼範例中的 *hmodRichEdit* 參數是 Msftedit.dll 模組的控制碼，並假設已透過呼叫 **GetModuleHandle** 函式來取出此控制碼。</span><span class="sxs-lookup"><span data-stu-id="73280-117">The *hmodRichEdit* parameter in the code example is a handle to the Msftedit.dll module, and it is assumed that this handle has already been retrieved by a call to the **GetModuleHandle** function.</span></span>

## <a name="complete-example"></a><span data-ttu-id="73280-118">完整範例</span><span class="sxs-lookup"><span data-stu-id="73280-118">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="73280-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="73280-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73280-120">使用無視窗的 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="73280-120">Using Windowless Rich Edit Controls</span></span>](using-windowless-rich-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="73280-121">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="73280-121">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="73280-122">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="73280-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 





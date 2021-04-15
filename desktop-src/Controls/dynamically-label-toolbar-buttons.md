---
title: 如何動態標記工具列按鈕
description: 您可以使用 TB SETBUTTONINFO 訊息，將文字指派給現有的按鈕 \_ 。
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "104462800"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a><span data-ttu-id="93f22-103">如何動態標記工具列按鈕</span><span class="sxs-lookup"><span data-stu-id="93f22-103">How to Dynamically Label Toolbar Buttons</span></span>

<span data-ttu-id="93f22-104">您可以使用 [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) 訊息，將文字指派給現有的按鈕。</span><span class="sxs-lookup"><span data-stu-id="93f22-104">You can assign text to an existing button by using the [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="93f22-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="93f22-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="93f22-106">技術</span><span class="sxs-lookup"><span data-stu-id="93f22-106">Technologies</span></span>

-   [<span data-ttu-id="93f22-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="93f22-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="93f22-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="93f22-108">Prerequisites</span></span>

-   <span data-ttu-id="93f22-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="93f22-109">C/C++</span></span>
-   <span data-ttu-id="93f22-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="93f22-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="93f22-111">指示</span><span class="sxs-lookup"><span data-stu-id="93f22-111">Instructions</span></span>

### <a name="dynamically-label-a-toolbar-button"></a><span data-ttu-id="93f22-112">動態標示工具列按鈕</span><span class="sxs-lookup"><span data-stu-id="93f22-112">Dynamically Label a Toolbar Button</span></span>

<span data-ttu-id="93f22-113">下列範例示範如何在先前的範例 **中，將** 第三個按鈕的文字變更 **為 [另存新** 檔]。</span><span class="sxs-lookup"><span data-stu-id="93f22-113">The following example demonstrates how to change the text of the third button in the previous examples from **Save** to **Save As**.</span></span>


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a><span data-ttu-id="93f22-114">備註</span><span class="sxs-lookup"><span data-stu-id="93f22-114">Remarks</span></span>

<span data-ttu-id="93f22-115">使用 [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) 來變更按鈕的文字，並不會影響在內部字串清單中指派給該按鈕的字串。</span><span class="sxs-lookup"><span data-stu-id="93f22-115">Changing a button's text by using [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md) does not affect the string that is assigned to that button in the internal string list.</span></span>

<span data-ttu-id="93f22-116">如果您將工具列按鈕字串加入至內部文字清單中，您就無法藉由呼叫 [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md)來取得該字串的索引，而必須改用 [**TB \_ GETBUTTON**](tb-getbutton.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="93f22-116">If you add a toolbar button string to the internal text list, you cannot retrieve the index of that string by calling [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md)—you must use the [**TB\_GETBUTTON**](tb-getbutton.md) message instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93f22-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="93f22-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93f22-118">使用工具列控制項</span><span class="sxs-lookup"><span data-stu-id="93f22-118">Using Toolbar Controls</span></span>](using-toolbar-controls.md)
</dt> <dt>

<span data-ttu-id="93f22-119">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="93f22-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 





---
title: 如何使用豐富的編輯文字作業
description: 應用程式可以傳送訊息，以在 rich edit 控制項中取得或尋找文字。 您可以取出選取的文字或指定的文字範圍。
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b54619e1ce5952b7c0d06527c6aca2402a4e714
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933660"
---
# <a name="how-to-use-rich-edit-text-operations"></a><span data-ttu-id="29b89-104">如何使用豐富的編輯文字作業</span><span class="sxs-lookup"><span data-stu-id="29b89-104">How to Use Rich Edit Text Operations</span></span>

<span data-ttu-id="29b89-105">應用程式可以傳送訊息，以在 rich edit 控制項中取得或尋找文字。</span><span class="sxs-lookup"><span data-stu-id="29b89-105">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="29b89-106">您可以取出選取的文字或指定的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="29b89-106">You can retrieve either the selected text or a specified range of text.</span></span>

<span data-ttu-id="29b89-107">若要在 rich edit 控制項中取得選取的文字，請使用 [**EM \_ GETSELTEXT**](em-getseltext.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="29b89-107">To get the selected text in a rich edit control, use the [**EM\_GETSELTEXT**](em-getseltext.md) message.</span></span> <span data-ttu-id="29b89-108">文字會複製到指定的字元陣列。</span><span class="sxs-lookup"><span data-stu-id="29b89-108">The text is copied to the specified character array.</span></span> <span data-ttu-id="29b89-109">您必須確定陣列夠大，足以容納選取的文字加上終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="29b89-109">You must ensure that the array is large enough to hold the selected text plus a terminating null character.</span></span>

<span data-ttu-id="29b89-110">若要取出指定的文字範圍，請使用 [**EM \_ GETTEXTRANGE**](em-gettextrange.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="29b89-110">To retrieve a specified range of text, use the [**EM\_GETTEXTRANGE**](em-gettextrange.md) message.</span></span> <span data-ttu-id="29b89-111">與此訊息搭配使用的 [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) 結構會指定要取出的文字範圍，並指向接收文字的字元陣列。</span><span class="sxs-lookup"><span data-stu-id="29b89-111">The [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure used with this message specifies the text range to retrieve and points to a character array that receives the text.</span></span> <span data-ttu-id="29b89-112">同樣地，應用程式必須確定陣列夠大，足以容納指定的文字加上終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="29b89-112">Here again, the application must ensure that the array is large enough for the specified text plus a terminating null character.</span></span>

<span data-ttu-id="29b89-113">您可以使用 [**em \_ FINDTEXT**](em-findtext.md) 或 [**em \_ FINDTEXTEX**](em-findtextex.md) 訊息來搜尋 rich edit 控制項中的字串，或 Unicode 對等的 [**em \_ FINDTEXTW**](em-findtextw.md) 和 [**em \_ FINDTEXTEXW**](em-findtextexw.md)。</span><span class="sxs-lookup"><span data-stu-id="29b89-113">You can search for a string in a rich edit control by using the [**EM\_FINDTEXT**](em-findtext.md) or [**EM\_FINDTEXTEX**](em-findtextex.md) messages, or their Unicode equivalents, [**EM\_FINDTEXTW**](em-findtextw.md) and [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span> <span data-ttu-id="29b89-114">與 nonextended 版本搭配使用的 [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) 結構會指定要搜尋的文字範圍，以及要搜尋的字串。</span><span class="sxs-lookup"><span data-stu-id="29b89-114">The [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure that is used with the nonextended versions specifies the text range to search and the string to search for.</span></span> <span data-ttu-id="29b89-115">擴充的版本會使用 [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) 結構，此結構會指定相同的資訊，同時也會接收所找到文字之字元範圍的開始和結束點。</span><span class="sxs-lookup"><span data-stu-id="29b89-115">The extended versions use a [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, which specifies the same information and also receives the start and end points of the character range of the found text.</span></span> <span data-ttu-id="29b89-116">您也可以指定這類選項，如同搜尋是否區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="29b89-116">You can also specify such options as whether the search is case sensitive.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="29b89-117">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="29b89-117">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="29b89-118">技術</span><span class="sxs-lookup"><span data-stu-id="29b89-118">Technologies</span></span>

-   [<span data-ttu-id="29b89-119">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="29b89-119">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="29b89-120">必要條件</span><span class="sxs-lookup"><span data-stu-id="29b89-120">Prerequisites</span></span>

-   <span data-ttu-id="29b89-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="29b89-121">C/C++</span></span>
-   <span data-ttu-id="29b89-122">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="29b89-122">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="29b89-123">指示</span><span class="sxs-lookup"><span data-stu-id="29b89-123">Instructions</span></span>

### <a name="use-a-rich-edit-text-operation"></a><span data-ttu-id="29b89-124">使用 Rich Edit 文字操作</span><span class="sxs-lookup"><span data-stu-id="29b89-124">Use a Rich Edit Text Operation</span></span>

<span data-ttu-id="29b89-125">下列範例函式會在支援 Unicode 的 rich edit 控制項中，找到所選文字內的指定文字。</span><span class="sxs-lookup"><span data-stu-id="29b89-125">The following example function finds the specified text within the selected text in a rich edit control that supports Unicode.</span></span> <span data-ttu-id="29b89-126">如果找到目標，則會變成新的選取專案。</span><span class="sxs-lookup"><span data-stu-id="29b89-126">If the target is found, it becomes the new selection.</span></span>


```C++
BOOL FindTextInSelection(HWND hRich, WCHAR* target)
{
    CHARRANGE selectionRange;
    
    SendMessage(hRich, EM_EXGETSEL, 0, (LPARAM)&selectionRange);
    
    FINDTEXTEX ftex;
    
    ftex.lpstrText  = target;
    ftex.chrg.cpMin = selectionRange.cpMin;
    ftex.chrg.cpMax = selectionRange.cpMax;
    
    LRESULT lr = SendMessage(hRich, EM_FINDTEXTEXW, (WPARAM)FR_DOWN, (LPARAM) &ftex);
    
    if (lr >= 0)
    {
        LRESULT lr1 = SendMessage(hRich, EM_EXSETSEL, 0, (LPARAM)&ftex.chrgText);
        
        SendMessage(hRich, EM_HIDESELECTION, (LPARAM)FALSE, 0);
        
        return TRUE;
    }
    
    return FALSE;
    
}
```



## <a name="remarks"></a><span data-ttu-id="29b89-127">備註</span><span class="sxs-lookup"><span data-stu-id="29b89-127">Remarks</span></span>

<span data-ttu-id="29b89-128">Microsoft Rich Edit 3.0 也支援 HexToUnicode 輸入方法編輯器 (IME) 函式，可讓使用者使用快速鍵在十六進位和 Unicode 之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="29b89-128">Microsoft Rich Edit 3.0 also supports the HexToUnicode Input Method Editor (IME) function, which allows a user to convert between hexadecimal and Unicode by using hot keys.</span></span> <span data-ttu-id="29b89-129">如需詳細資訊，請參閱 [HEXTOUNICODE IME](/windows/desktop/Intl/hextounicode-ime)。</span><span class="sxs-lookup"><span data-stu-id="29b89-129">For more information, see [HexToUnicode IME](/windows/desktop/Intl/hextounicode-ime).</span></span>

## <a name="related-topics"></a><span data-ttu-id="29b89-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="29b89-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29b89-131">使用 Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="29b89-131">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="29b89-132">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="29b89-132">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 
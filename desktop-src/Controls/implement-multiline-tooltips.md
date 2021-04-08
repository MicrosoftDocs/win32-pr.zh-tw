---
title: 如何執行多行工具提示
description: 多行工具提示允許文字顯示在一行以上。
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d6f32d638b2d33ea6270aa5f8ce2c09f0f4174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671975"
---
# <a name="how-to-implement-multiline-tooltips"></a><span data-ttu-id="c59a9-103">如何執行多行工具提示</span><span class="sxs-lookup"><span data-stu-id="c59a9-103">How to Implement Multiline Tooltips</span></span>

<span data-ttu-id="c59a9-104">多行工具提示允許文字顯示在一行以上。</span><span class="sxs-lookup"><span data-stu-id="c59a9-104">Multiline tooltips allow text to be displayed on more than one line.</span></span>

<span data-ttu-id="c59a9-105">[版本 4.70](common-control-versions.md)和更新版本的通用控制項都支援它們。</span><span class="sxs-lookup"><span data-stu-id="c59a9-105">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <span data-ttu-id="c59a9-106">您的應用程式會藉由傳送 [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) 訊息（指定顯示矩形的寬度）來建立多行工具提示。</span><span class="sxs-lookup"><span data-stu-id="c59a9-106">Your application creates a multiline tooltip by sending a [**TTM\_SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) message, specifying the width of the display rectangle.</span></span> <span data-ttu-id="c59a9-107">超過此寬度的文字會換行至下一行，而不是擴展顯示區域。</span><span class="sxs-lookup"><span data-stu-id="c59a9-107">Text that exceeds this width wraps to the next line rather than widening the display region.</span></span> <span data-ttu-id="c59a9-108">視需要增加矩形高度以容納額外的行。</span><span class="sxs-lookup"><span data-stu-id="c59a9-108">The rectangle height is increased as needed to accommodate the additional lines.</span></span> <span data-ttu-id="c59a9-109">工具提示控制項會自動包裝行，或者您可以使用換行字元組合（ \\ r \\ n）來強制在特定位置換行。</span><span class="sxs-lookup"><span data-stu-id="c59a9-109">The tooltip control wraps the lines automatically, or you can use a carriage return/line feed combination, \\r\\n, to force line breaks at particular locations.</span></span>

<span data-ttu-id="c59a9-110">結果顯示如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="c59a9-110">The resulting display is shown in the following illustration.</span></span>

![具有工具提示之對話方塊的螢幕擷取畫面，其中包含的文字相片順序類似多行段落](images/tt-multiline.png)

> [!Note]  
> <span data-ttu-id="c59a9-112">[**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)結構的 **szText** 成員所指定的文字緩衝區只能容納80個字元。</span><span class="sxs-lookup"><span data-stu-id="c59a9-112">The text buffer specified by the **szText** member of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure can accommodate only 80 characters.</span></span> <span data-ttu-id="c59a9-113">如果您需要使用較長的字串，請將 **NMTTDISPINFO** 的 **lpszText** 成員指向包含所需文字的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c59a9-113">If you need to use a longer string, point the **lpszText** member of **NMTTDISPINFO** to a buffer containing the desired text.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="c59a9-114">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="c59a9-114">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c59a9-115">技術</span><span class="sxs-lookup"><span data-stu-id="c59a9-115">Technologies</span></span>

-   [<span data-ttu-id="c59a9-116">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="c59a9-116">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c59a9-117">必要條件</span><span class="sxs-lookup"><span data-stu-id="c59a9-117">Prerequisites</span></span>

-   <span data-ttu-id="c59a9-118">C/C++</span><span class="sxs-lookup"><span data-stu-id="c59a9-118">C/C++</span></span>
-   <span data-ttu-id="c59a9-119">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="c59a9-119">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c59a9-120">指示</span><span class="sxs-lookup"><span data-stu-id="c59a9-120">Instructions</span></span>

### <a name="implement-multiline-tooltips"></a><span data-ttu-id="c59a9-121">執行多行工具提示</span><span class="sxs-lookup"><span data-stu-id="c59a9-121">Implement Multiline Tooltips</span></span>

<span data-ttu-id="c59a9-122">下列程式碼片段是簡單 [TTN \_ GETDISPINFO](ttn-getdispinfo.md) 通知處理常式的範例。</span><span class="sxs-lookup"><span data-stu-id="c59a9-122">The following code fragment is an example of a simple [TTN\_GETDISPINFO](ttn-getdispinfo.md) notification handler.</span></span> <span data-ttu-id="c59a9-123">它會將顯示矩形設定為150圖元，以啟用多行工具提示。</span><span class="sxs-lookup"><span data-stu-id="c59a9-123">It enables a multiline tooltip by setting the display rectangle to 150 pixels.</span></span> <span data-ttu-id="c59a9-124">第一個單字後面會插入一個手動分行符號，以顯示分行符號可能很難和軟。</span><span class="sxs-lookup"><span data-stu-id="c59a9-124">A manual line break is inserted after the first word to show that line breaks can be hard as well as soft.</span></span>


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a><span data-ttu-id="c59a9-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="c59a9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c59a9-126">使用工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="c59a9-126">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 





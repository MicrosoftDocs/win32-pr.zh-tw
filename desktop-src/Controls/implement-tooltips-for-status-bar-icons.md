---
title: 如何執行狀態列圖示的工具提示
description: 顯示狀態列圖示之解釋性訊息的不造成干擾方式是執行工具提示。 按一下時，工具提示就會消失，但是您也可以指定超時值。
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463785"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="b8420-104">如何執行狀態列圖示的工具提示</span><span class="sxs-lookup"><span data-stu-id="b8420-104">How to Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="b8420-105">顯示狀態列圖示之解釋性訊息的不造成干擾方式是執行工具提示。</span><span class="sxs-lookup"><span data-stu-id="b8420-105">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="b8420-106">按一下時，工具提示就會消失，但是您也可以指定超時值。</span><span class="sxs-lookup"><span data-stu-id="b8420-106">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b8420-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="b8420-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b8420-108">技術</span><span class="sxs-lookup"><span data-stu-id="b8420-108">Technologies</span></span>

-   [<span data-ttu-id="b8420-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="b8420-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b8420-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="b8420-110">Prerequisites</span></span>

-   <span data-ttu-id="b8420-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="b8420-111">C/C++</span></span>
-   <span data-ttu-id="b8420-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="b8420-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b8420-113">指示</span><span class="sxs-lookup"><span data-stu-id="b8420-113">Instructions</span></span>

### <a name="implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="b8420-114">執行狀態列圖示的工具提示</span><span class="sxs-lookup"><span data-stu-id="b8420-114">Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="b8420-115">下列程式碼片段說明如何將氣球工具提示新增至狀態列圖示。</span><span class="sxs-lookup"><span data-stu-id="b8420-115">The following code fragment illustrates how to add a balloon tooltip to a status bar icon.</span></span>


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a><span data-ttu-id="b8420-116">備註</span><span class="sxs-lookup"><span data-stu-id="b8420-116">Remarks</span></span>

<span data-ttu-id="b8420-117">如需狀態列的詳細討論，請參閱 [工作列](/windows/desktop/shell/taskbar)。</span><span class="sxs-lookup"><span data-stu-id="b8420-117">For a detailed discussion of the status bar, see [The Taskbar](/windows/desktop/shell/taskbar).</span></span>

<span data-ttu-id="b8420-118">若要顯示氣球工具提示，您需要 \_ 在 [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) 結構中設定 n 資訊旗標，並使用 **szInfo** 和 **uTimeout** 成員來指定工具提示文字和超時時間。</span><span class="sxs-lookup"><span data-stu-id="b8420-118">To display a balloon tooltip, you need to set the NIF\_INFO flag in the [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) structure, and use the **szInfo** and **uTimeout** members to specify the tooltip text and time-out duration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8420-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8420-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8420-120">使用工具提示控制項</span><span class="sxs-lookup"><span data-stu-id="b8420-120">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 
---
title: 如何取出和設定快速鍵
description: 本主題將示範如何取得或設定快速鍵控制項的按鍵組合。
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106993738"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a><span data-ttu-id="d5b58-103">如何取出和設定快速鍵</span><span class="sxs-lookup"><span data-stu-id="d5b58-103">How to Retrieve and Set a Hot Key</span></span>

<span data-ttu-id="d5b58-104">本主題將示範如何取得或設定快速鍵控制項的按鍵組合。</span><span class="sxs-lookup"><span data-stu-id="d5b58-104">This topic demonstrates how to retrieve or set the key combination for a hot key control.</span></span> <span data-ttu-id="d5b58-105">[**HKM \_ SETHOTKEY**](hkm-sethotkey.md)訊息可讓應用程式設定快速鍵控制項的快速鍵組合。</span><span class="sxs-lookup"><span data-stu-id="d5b58-105">The [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message allows an application to set the hot key combination for a hot key control.</span></span> <span data-ttu-id="d5b58-106">應用程式會使用 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) 訊息來取得使用者所選擇之快速鍵的虛擬金鑰程式碼和修飾詞旗標。</span><span class="sxs-lookup"><span data-stu-id="d5b58-106">Applications use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier flags of the hot key that is chosen by the user.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d5b58-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="d5b58-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d5b58-108">技術</span><span class="sxs-lookup"><span data-stu-id="d5b58-108">Technologies</span></span>

-   [<span data-ttu-id="d5b58-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="d5b58-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d5b58-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="d5b58-110">Prerequisites</span></span>

-   <span data-ttu-id="d5b58-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="d5b58-111">C/C++</span></span>
-   <span data-ttu-id="d5b58-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="d5b58-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d5b58-113">指示</span><span class="sxs-lookup"><span data-stu-id="d5b58-113">Instructions</span></span>


<span data-ttu-id="d5b58-114">您可以使用 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) 訊息來取得虛擬金鑰程式碼和輔助按鍵，以描述使用者選擇的熱鍵。</span><span class="sxs-lookup"><span data-stu-id="d5b58-114">Use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier keys that describe a hot key chosen by the user.</span></span> <span data-ttu-id="d5b58-115">使用 [**HKM \_ SETHOTKEY**](hkm-sethotkey.md) 訊息來設定快速鍵的值。</span><span class="sxs-lookup"><span data-stu-id="d5b58-115">Use the [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message to set those values for a hot key.</span></span>

<span data-ttu-id="d5b58-116">在下列 c + + 程式碼範例中，應用程式定義函式會使用 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) 訊息從熱鍵控制項取出按鍵組合，然後使用 [**WM \_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) 訊息來設定全域熱鍵。</span><span class="sxs-lookup"><span data-stu-id="d5b58-116">In the following C++ code example, the application-defined function uses the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve a key combination from a hot key control and then uses the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message to set a global hot key.</span></span> <span data-ttu-id="d5b58-117">請注意，您無法為具有 [**WS \_ 子**](/windows/desktop/winmsg/window-styles) 視窗樣式的視窗設定全域快速鍵。</span><span class="sxs-lookup"><span data-stu-id="d5b58-117">Note that you cannot set a global hot key for a window that has the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) window style.</span></span>



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="d5b58-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="d5b58-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5b58-119">快速鍵控制參考</span><span class="sxs-lookup"><span data-stu-id="d5b58-119">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d5b58-120">關於快速鍵控制項</span><span class="sxs-lookup"><span data-stu-id="d5b58-120">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="d5b58-121">使用快速鍵控制項</span><span class="sxs-lookup"><span data-stu-id="d5b58-121">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 
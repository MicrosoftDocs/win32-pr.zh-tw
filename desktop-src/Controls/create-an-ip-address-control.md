---
title: 如何建立 IP 位址控制項
description: 本主題示範如何建立 IP 位址控制項的實例。
ms.assetid: E4DBECA6-B3F2-405F-8D95-32FA2334114D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8427a5695c0b9c79c19d328f4abc2ab0ffb2e5a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104093527"
---
# <a name="how-to-create-an-ip-address-control"></a><span data-ttu-id="47064-103">如何建立 IP 位址控制項</span><span class="sxs-lookup"><span data-stu-id="47064-103">How to Create an IP Address Control</span></span>

<span data-ttu-id="47064-104">本主題示範如何建立 IP 位址控制項的實例。</span><span class="sxs-lookup"><span data-stu-id="47064-104">This topic demonstrates how to create an instance of an IP address control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="47064-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="47064-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="47064-106">技術</span><span class="sxs-lookup"><span data-stu-id="47064-106">Technologies</span></span>

-   [<span data-ttu-id="47064-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="47064-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="47064-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="47064-108">Prerequisites</span></span>

-   <span data-ttu-id="47064-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="47064-109">C/C++</span></span>
-   <span data-ttu-id="47064-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="47064-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="47064-111">指示</span><span class="sxs-lookup"><span data-stu-id="47064-111">Instructions</span></span>


<span data-ttu-id="47064-112">建立 IP 位址控制項之前，請先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)來載入通用控制項 DLL。</span><span class="sxs-lookup"><span data-stu-id="47064-112">Before creating an IP address control, load the common controls DLL by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="47064-113">然後使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數來建立實例 IP 位址控制項。</span><span class="sxs-lookup"><span data-stu-id="47064-113">Then use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an instance IP address control.</span></span> <span data-ttu-id="47064-114">控制項的類別名稱是 [**WC \_ IPADDRESS**](common-control-window-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="47064-114">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md).</span></span> <span data-ttu-id="47064-115">使用 [**WS \_ 子**](/windows/desktop/winmsg/window-styles) 樣式，因為沒有與 IP 位址控制項相關聯的特定樣式常數。</span><span class="sxs-lookup"><span data-stu-id="47064-115">Use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style, because there is no specific style constant associated with the IP address control.</span></span>

<span data-ttu-id="47064-116">在下列 c + + 程式碼範例中，應用程式定義函式會先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) ，並將 [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)結構的 **dwICC** 成員設定為 [**ICC \_ 網際網路 \_ 類別**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)，以指定 IP 位址類別。</span><span class="sxs-lookup"><span data-stu-id="47064-116">In the following C++ code example, the application-defined function first calls [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) and sets the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure to [**ICC\_INTERNET\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), which specifies the IP address class.</span></span> <span data-ttu-id="47064-117">然後，它會呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 來建立 IP 位址控制項的實例。</span><span class="sxs-lookup"><span data-stu-id="47064-117">It then calls [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to create an instance of the IP address control.</span></span>


```C++
// CreateIPAdressFld - creates a IPAddress control.
// Returns the handle to the new control
// TO DO:  calling procedure needs to check whether the handle is NULL, in case 
// of an error in creation.
// int xcoord, ycoord the coordinates of location of the control in the parent window
// HINST hInst is the global handle to the application instance.
// HWND  hWndParent is the handle to the control's parent window. 
//
//
HWND CreateIPAddressFld (HWND hwndParent, int xcoord, int ycoord) 
{     
     
    INITCOMMONCONTROLSEX icex;
    
    // Ensure that the common control DLL is loaded. 
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC  = ICC_INTERNET_CLASSES ;
    InitCommonControlsEx(&icex); 
    
    // Create the IPAddress control.        
    HWND hWndIPAddressFld = CreateWindow(WC_IPADDRESS, 
                                L"", 
                                WS_CHILD | WS_OVERLAPPED | WS_VISIBLE, 
                                xcoord, 
                                ycoord,
                                150, 
                                20,  
                                hwndParent, 
                                NULL, 
                                hInst, 
                                NULL); 
                                
    return (hWndIPAddressFld);
}
```



## <a name="related-topics"></a><span data-ttu-id="47064-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="47064-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47064-119">IP 位址控制參考</span><span class="sxs-lookup"><span data-stu-id="47064-119">IP Address Control Reference</span></span>](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[<span data-ttu-id="47064-120">關於 IP 位址控制項</span><span class="sxs-lookup"><span data-stu-id="47064-120">About IP Address Controls</span></span>](ip-address-controls.md)
</dt> <dt>

[<span data-ttu-id="47064-121">使用 IP 位址控制項</span><span class="sxs-lookup"><span data-stu-id="47064-121">Using IP Address Controls</span></span>](using-ip-address-controls.md)
</dt> </dl>

 

 
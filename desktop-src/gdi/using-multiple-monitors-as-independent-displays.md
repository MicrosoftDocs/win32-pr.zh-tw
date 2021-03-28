---
description: 使用多個監視器作為獨立顯示器時，桌面會包含一或一組顯示器。
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: 使用多個監視器作為獨立顯示器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4761e0e04ae1adaa197b06f04fa36c61ccda3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973625"
---
# <a name="using-multiple-monitors-as-independent-displays"></a><span data-ttu-id="a78f8-103">使用多個監視器作為獨立顯示器</span><span class="sxs-lookup"><span data-stu-id="a78f8-103">Using Multiple Monitors as Independent Displays</span></span>

<span data-ttu-id="a78f8-104">使用多個監視器作為獨立顯示器時，桌面會包含一或一組顯示器。</span><span class="sxs-lookup"><span data-stu-id="a78f8-104">When using multiple monitors as independent displays, the desktop contains one display or set of displays.</span></span> <span data-ttu-id="a78f8-105">這組顯示器一律會包含主要監視器，而且會如本主題的其他章節所述運作。</span><span class="sxs-lookup"><span data-stu-id="a78f8-105">This set of displays always includes the primary monitor and behaves as mentioned in the other sections of this topic.</span></span> <span data-ttu-id="a78f8-106">應用程式可以使用任何其他監視器作為獨立顯示器。</span><span class="sxs-lookup"><span data-stu-id="a78f8-106">An application can use any other monitor as an independent display.</span></span>

> [!Note]  
> <span data-ttu-id="a78f8-107">在 Windows 顯示驅動程式模型 (WDDM) 的驅動程式上，不支援使用其他監視器作為獨立顯示器。</span><span class="sxs-lookup"><span data-stu-id="a78f8-107">Using other monitors as independent displays isn't supported on drivers that are implemented to the Windows Display Driver Model (WDDM).</span></span>

 

<span data-ttu-id="a78f8-108">「視窗管理員」並不知道任何獨立顯示器。</span><span class="sxs-lookup"><span data-stu-id="a78f8-108">The window manager knows nothing about the independent displays.</span></span> <span data-ttu-id="a78f8-109">這些是由應用程式完全控制，且應用程式不能使用任何視窗管理員函式 (所有視窗管理員呼叫都會自動移至主顯示器) 。</span><span class="sxs-lookup"><span data-stu-id="a78f8-109">They are completely controlled by the application, and no window manager functions are available to the application (all window manager calls automatically go to the primary display).</span></span> <span data-ttu-id="a78f8-110">每個獨立顯示器都有自己的原點和水準和垂直座標，而且是透過 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) 或 DirectX 函式（例如 **DIRECTDRAWCREATE**）的 GDI 函數來存取。</span><span class="sxs-lookup"><span data-stu-id="a78f8-110">Each independent display has its own origin and horizontal and vertical coordinates, and is accessed through the GDI functions such as [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) or the DirectX functions such as **DirectDrawCreate**.</span></span>

<span data-ttu-id="a78f8-111">若要找出獨立顯示器，請呼叫 [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) ，並 \_ \_ \_ \_ 在 [**顯示 \_ 設備**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) 結構中尋找未將顯示裝置附加至桌面旗標的顯示器。</span><span class="sxs-lookup"><span data-stu-id="a78f8-111">To locate the independent displays, call [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and look for the displays that do not have DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span>

<span data-ttu-id="a78f8-112">應用程式可以藉由呼叫來開啟顯示器</span><span class="sxs-lookup"><span data-stu-id="a78f8-112">An application can open a display by calling</span></span>


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



<span data-ttu-id="a78f8-113">在此呼叫中， *lpszDisplayName* 參數是 [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) 所傳回的其中一個裝置名稱，而 *lpDevMode* 是此裝置之圖形模式的描述。</span><span class="sxs-lookup"><span data-stu-id="a78f8-113">In this call, the *lpszDisplayName* parameter is one of the device names returned by [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and *lpDevMode* is a description of the graphics mode for this device.</span></span> <span data-ttu-id="a78f8-114">產生的 hdc 可以用來對裝置執行任何圖形作業。</span><span class="sxs-lookup"><span data-stu-id="a78f8-114">The resulting hdc can be used to perform any graphics operation to the device.</span></span>

 

 




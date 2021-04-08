---
title: 圖形效果
description: 在遠端桌面服務環境中做為遠端會話執行時，應該停用的功能清單。
ms.assetid: 229a1058-acba-4d4b-ba52-824dda4f91a5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f850b8bac5d084419b1f15c2e0efe619da5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932257"
---
# <a name="graphic-effects"></a><span data-ttu-id="1cfd0-103">圖形效果</span><span class="sxs-lookup"><span data-stu-id="1cfd0-103">Graphic effects</span></span>

<span data-ttu-id="1cfd0-104">遠端桌面服務伺服器依賴網路將所有輸入和輸出傳輸至其用戶端終端機。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-104">A Remote Desktop Services server relies on the network to transmit all input and output to its client terminals.</span></span> <span data-ttu-id="1cfd0-105">因此，過度使用圖形效果的應用程式可能會降低網路的效能，而影響所有遠端桌面服務用戶端的效能。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-105">Consequently, applications that make excessive use of graphic effects can affect performance for all Remote Desktop Services clients by slowing down the network.</span></span> <span data-ttu-id="1cfd0-106">此外，透過網路的傳送速率愈慢，可能會導致這些特殊效果比在本機影片環境中的外觀更不滿意。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-106">In addition, the slower transmission speed over a network might cause these special effects to appear less pleasing than they would be in a local video environment.</span></span>

<span data-ttu-id="1cfd0-107">尤其是，應用程式應該在遠端桌面服務環境中以遠端會話執行時，停用或最小化下列功能：</span><span class="sxs-lookup"><span data-stu-id="1cfd0-107">In particular, applications should disable or minimize the use of the following features when running in a Remote Desktop Services environment as a remote session:</span></span>

-   <span data-ttu-id="1cfd0-108">啟動顯示畫面-在應用程式啟動時顯示的圖形化產品或公司資訊。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-108">Splash screens—graphical product or company information displayed while an application is starting.</span></span> <span data-ttu-id="1cfd0-109">將啟動顯示畫面傳送至遠端桌面連線 (RDC) 用戶端會耗用額外的網路頻寬，並在存取應用程式之前強制使用者等待。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-109">Transmitting a splash screen to a Remote Desktop Connection (RDC) client consumes extra network bandwidth and forces the user to wait before accessing the application.</span></span>
-   <span data-ttu-id="1cfd0-110">同時耗用 CPU 時間和網路頻寬的動畫。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-110">Animations, which consume both CPU time and network bandwidth.</span></span>
-   <span data-ttu-id="1cfd0-111">直接輸入或輸出到畫面。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-111">Direct input or output to the screen.</span></span> <span data-ttu-id="1cfd0-112">如果您需要從畫面讀取位，請維護影片緩衝區的個別螢幕複製。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-112">If you need to read bits from the screen, maintain a separate, off-screen copy of the video buffer.</span></span> <span data-ttu-id="1cfd0-113">同樣地，如果您需要執行詳盡的螢幕輸出（例如，將數個影像覆迭以到達最後的複合畫面），請在非螢幕緩衝區中工作，然後將結果傳送至實際的影片緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-113">Similarly, if you need to do elaborate screen output—for example, overlaying several images to arrive at a final composite screen—do that work in an off-screen buffer, and then send the results to the actual video buffer.</span></span>

<span data-ttu-id="1cfd0-114">如需有關偵測遠端會話的詳細資訊，請參閱偵測 [遠端桌面服務環境](detecting-the-terminal-services-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-114">For more information about detecting remote sessions, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

<span data-ttu-id="1cfd0-115">盡可能使用 Microsoft Foundation Class library 或 MFC。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-115">Use the Microsoft Foundation Class library, or MFC, whenever possible.</span></span> <span data-ttu-id="1cfd0-116">MFC 有一長串的已嘗試和真正的類別，可執行各種不同的工作。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-116">The MFC has a long list of tried-and-true classes for performing a wide variety of tasks.</span></span> <span data-ttu-id="1cfd0-117">這些類別大多適用于遠端桌面服務環境，通常比重新設計的解決方案更好。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-117">Most of these classes work well in a Remote Desktop Services environment—usually much better than re-engineered solutions.</span></span> <span data-ttu-id="1cfd0-118">一個很好的例子就是提供內容相關解說文字的類別—當滑鼠指標停留在按鈕或功能表項目上時，就會出現在畫面上的解說文字。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-118">A good example is the class that provides context-sensitive help text—help text that appears on-screen when the mouse pointer hovers over a button or menu item.</span></span> <span data-ttu-id="1cfd0-119">如果應用程式使用 MFC 執行來提供此功能，它在桌面系統上的運作效果相當好。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-119">If an application uses the MFC implementation to provide this feature, it will work reasonably well on the desktop system.</span></span> <span data-ttu-id="1cfd0-120">但是，如果應用程式使用對話方塊或替代方法來執行這項功能，最終結果可能也無法在遠端桌面服務環境中運作。</span><span class="sxs-lookup"><span data-stu-id="1cfd0-120">But if the application implements this feature by using dialog boxes or an alternate approach, the final result might not function as well in a Remote Desktop Services environment.</span></span>

 

 





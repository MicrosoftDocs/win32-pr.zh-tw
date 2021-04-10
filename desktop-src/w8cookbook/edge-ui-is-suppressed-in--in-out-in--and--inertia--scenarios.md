---
title: Edge UI 會在「內建」和「慣性」案例中隱藏
description: Edge UI 會在「內建」和「慣性」案例中隱藏
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184061"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a><span data-ttu-id="2a829-103">Edge UI 會在「內建」和「慣性」案例中隱藏</span><span class="sxs-lookup"><span data-stu-id="2a829-103">Edge UI is suppressed in “in-out-in” and “inertia” scenarios</span></span>

## <a name="platform"></a><span data-ttu-id="2a829-104">平台</span><span class="sxs-lookup"><span data-stu-id="2a829-104">Platform</span></span>

<dl> <span data-ttu-id="2a829-105">用戶端-Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="2a829-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="2a829-106">Description</span><span class="sxs-lookup"><span data-stu-id="2a829-106">Description</span></span>

<span data-ttu-id="2a829-107">在某些情況下，使用者可能會意外地叫用 Edge UI， (常用鍵、應用程式行、應用程式切換) 。</span><span class="sxs-lookup"><span data-stu-id="2a829-107">There are some cases where users may unintentionally invoke Edge UI (Charms, App Bar, app switching).</span></span> <span data-ttu-id="2a829-108">我們推出了一項功能，可讓開發人員為整個螢幕設計 UI，而不需要進行 affordances (例如，框線) 來防止使用者意外碰到邊緣。</span><span class="sxs-lookup"><span data-stu-id="2a829-108">We have introduced a feature to allow developers to design their UI for the whole screen without making affordances (for example, borders) to prevent the user from accidentally hitting the edges.</span></span>

<span data-ttu-id="2a829-109">有兩種情況可能會導致最常導致意外的邊緣撥動：</span><span class="sxs-lookup"><span data-stu-id="2a829-109">There are two cases that might lead most often to inadvertent edge swipes:</span></span>

-   <span data-ttu-id="2a829-110">在快速移動中，互動的速度和不精確有時可能會讓它們從畫面邊緣進入</span><span class="sxs-lookup"><span data-stu-id="2a829-110">In fast panning, the speed and imprecision of the interaction can occasionally cause them to come in from the edge of the screen</span></span>
-   <span data-ttu-id="2a829-111">如果使用者在手寫時快速離開並重新進入螢幕區域（例如，在繪圖應用程式中），則這項傳入行為可能會錯誤地觸發 Edge UI 並中斷使用者體驗</span><span class="sxs-lookup"><span data-stu-id="2a829-111">If users rapidly leave and re-enter the screen area while inking with their finger, for example, in a painting app, this in-out-in behavior can mistakenly trigger the Edge UI and interrupt the user experience</span></span>

<span data-ttu-id="2a829-112">為了改進使用者和開發人員體驗，現在會在兩個特定的實例中隱藏 Edge UI：</span><span class="sxs-lookup"><span data-stu-id="2a829-112">To improve the user and developer experience, the Edge UI will now be suppressed in two specific instances:</span></span>

-   <span data-ttu-id="2a829-113">當使用者在應用程式中移動時，在支援 DManip 慣性和撥動的情況下，當慣性發生時，將不會在 timeout 視窗內叫用 Edge UI</span><span class="sxs-lookup"><span data-stu-id="2a829-113">When a user is panning in an application that supports DManip Inertia and swipes outside of the screen while inertia is occurring, the Edge UI will not be invoked within a timeout window</span></span>
-   <span data-ttu-id="2a829-114">在經過認證的裝置上，當使用者從螢幕中快速撥動到畫面之外，並在特定參數內 (的內部) 移動時，將不會叫用 Edge UI</span><span class="sxs-lookup"><span data-stu-id="2a829-114">On certified devices, when a user quickly swipes from within the screen to outside the screen and back inside (in-out-in motion) within certain parameters, the Edge UI will not be invoked</span></span>

## <a name="manifestations"></a><span data-ttu-id="2a829-115">表現</span><span class="sxs-lookup"><span data-stu-id="2a829-115">Manifestations</span></span>

<span data-ttu-id="2a829-116">當使用應用程式時，使用者快速地對邊緣進行輕量，將會看到意外的邊緣調用。</span><span class="sxs-lookup"><span data-stu-id="2a829-116">Users quickly swiping against the edge while using an app will see a decrease in unintentional edge invocation.</span></span>

## <a name="solution"></a><span data-ttu-id="2a829-117">解決方法</span><span class="sxs-lookup"><span data-stu-id="2a829-117">Solution</span></span>

<span data-ttu-id="2a829-118">開發人員應牢記這些緩和措施，而且應該能夠使用全螢幕，而不需要擔心使用者在邊緣與應用程式互動時，不會不慎觸發 Edge UI。</span><span class="sxs-lookup"><span data-stu-id="2a829-118">Developers should keep these mitigations in mind and should be able to use the full screen without fear that users will accidentally trigger the Edge UI while interacting with the application along the edge.</span></span>

 

 





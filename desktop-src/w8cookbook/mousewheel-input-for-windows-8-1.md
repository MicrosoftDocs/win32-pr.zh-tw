---
title: Windows 8.1 的滑鼠滾輪輸入
description: Windows 8.1 的滑鼠滾輪輸入
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839695"
---
# <a name="mousewheel-input-for-windows-81"></a><span data-ttu-id="bc3d8-103">Windows 8.1 的滑鼠滾輪輸入</span><span class="sxs-lookup"><span data-stu-id="bc3d8-103">Mousewheel input for Windows 8.1</span></span>

## <a name="platform"></a><span data-ttu-id="bc3d8-104">平台</span><span class="sxs-lookup"><span data-stu-id="bc3d8-104">Platform</span></span>

<dl> <span data-ttu-id="bc3d8-105">用戶端-Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="bc3d8-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="bc3d8-106">伺服器-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bc3d8-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="bc3d8-107">Description</span><span class="sxs-lookup"><span data-stu-id="bc3d8-107">Description</span></span>

<span data-ttu-id="bc3d8-108">在 Windows 8.1 中，在舊版 Windows 中，不再根據鍵盤焦點提供滑鼠滾輪事件。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-108">In Windows 8.1, mousewheel events are no longer delivered based on keyboard focus as in previous versions of Windows.</span></span> <span data-ttu-id="bc3d8-109">在 Windows 8.1 中，如果滑鼠停留在商店應用程式上，滑鼠滾輪將會傳遞給該應用程式;不過，基於相容性的目的，如果滑鼠停留在桌面應用程式上，則會繼續根據鍵盤焦點來傳遞滑鼠滾輪。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-109">In Windows 8.1, if the mouse is hovering over a store app, mousewheel will be delivered to that app; for compatibility purposes, however, if the mouse is hovering over a desktop app, mousewheel will continue to be delivered based on keyboard focus.</span></span>

## <a name="manifestations"></a><span data-ttu-id="bc3d8-110">表現</span><span class="sxs-lookup"><span data-stu-id="bc3d8-110">Manifestations</span></span>

<span data-ttu-id="bc3d8-111">當滑鼠停留在商店應用程式上時，滑鼠滾輪會在沒有使用者按一下 Store 應用程式的情況下，滾動任何適用的內容。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-111">When the mouse is hovering over Store apps, mousewheel will scroll any applicable content without the user having to click on the Store app.</span></span> <span data-ttu-id="bc3d8-112">這也適用于 [開始] 畫面。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-112">This also applies to the start screen.</span></span> <span data-ttu-id="bc3d8-113">這可讓您在 Windows 8.1 中滑鼠滾輪比 Windows 8 更簡單的互動來進行滾動。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-113">This makes scrolling by mousewheel a simpler interaction in Windows 8.1 than in Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="bc3d8-114">降低</span><span class="sxs-lookup"><span data-stu-id="bc3d8-114">Mitigation</span></span>

<span data-ttu-id="bc3d8-115">在大部分的情況下，這種變更應該不會影響現有的應用程式。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-115">For the most part this change should have no impact on existing apps.</span></span> <span data-ttu-id="bc3d8-116">如果商店應用程式只在註冊滑鼠點按事件之後才接聽滑鼠滾輪事件，該應用程式就不可能回應滑鼠滾輪，直到使用者主動按一下為止。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-116">If a Store app listened for mousewheel events only after it has registered a mouse click event, that app would not be likely to respond to mousewheel until the user actively clicked it.</span></span> <span data-ttu-id="bc3d8-117">因此，此處最有可能的缺點是，應用程式會繼續運作，就像在 Windows 8 一樣。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-117">Consequently, the most likely downside here is simply that an app continues to operate just as it did in Windows 8.</span></span> <span data-ttu-id="bc3d8-118">針對桌面應用程式，讓鍵盤焦點不再讓應用程式具有滑鼠滾輪輸入的 monopoly，但這也不會以任何方式中斷這些應用程式。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-118">For desktop apps, having keyboard focus no longer gives the app a monopoly over mousewheel input, but this also does not in any way break those apps.</span></span> <span data-ttu-id="bc3d8-119">因此，不需要短期的緩和措施。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-119">So no short-term mitigations are required.</span></span>

## <a name="solution"></a><span data-ttu-id="bc3d8-120">解決方法</span><span class="sxs-lookup"><span data-stu-id="bc3d8-120">Solution</span></span>

<span data-ttu-id="bc3d8-121">Store 應用程式開發人員應該預期會在沒有先驅滑鼠點擊事件的情況下接收滑鼠滾輪事件。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-121">Store app developers should expect to receive mousewheel events without a precursor mouse click event.</span></span> <span data-ttu-id="bc3d8-122">例如，它們不應該在註冊滑鼠點擊之後接聽滑鼠滾輪事件。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-122">They should not, for example, listen for mousewheel events only after registering a mouse click.</span></span> <span data-ttu-id="bc3d8-123">同樣地，桌面應用程式不應該嘗試抓取滑鼠滾輪事件 (例如，藉由在具有鍵盤焦點的情況下設定低層級的勾點) 。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-123">Similarly, desktop applications should not try to capture mousewheel events (for example, by setting a low-level hook) when they have keyboard focus.</span></span>

## <a name="tests"></a><span data-ttu-id="bc3d8-124">測試</span><span class="sxs-lookup"><span data-stu-id="bc3d8-124">Tests</span></span>

<span data-ttu-id="bc3d8-125">Store 應用程式開發人員應該在 Windows 8.1 上進行測試，以確認當滑鼠停留在應用程式上時，所有的滾動功能都能運作。</span><span class="sxs-lookup"><span data-stu-id="bc3d8-125">Store app developers should test on Windows 8.1 to verify that all scrolling functionality works whenever the mouse is hovering over the app.</span></span> <span data-ttu-id="bc3d8-126">傳統型應用程式開發人員應該在 Windows 8.1 上測試，以確認這些應用程式不會 (每個指導方針來捕捉滑鼠滾輪事件。 ) </span><span class="sxs-lookup"><span data-stu-id="bc3d8-126">Desktop app developers should test on Windows 8.1 to verify that they are not capturing mousewheel events (per guidance above.)</span></span>

 

 





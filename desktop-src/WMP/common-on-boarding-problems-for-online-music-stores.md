---
title: 線上音樂商店的常見內部問題
description: 線上音樂商店的常見內部問題
ms.assetid: 4210aabb-d1ad-4f98-88e0-941933d77303
keywords:
- Windows Media Player 線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f600d1035e0fd20be7786af4d4ffed4482138a72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682879"
---
# <a name="common-on-boarding-problems-for-online-music-stores"></a><span data-ttu-id="fb6c4-104">線上音樂商店的常見內部問題</span><span class="sxs-lookup"><span data-stu-id="fb6c4-104">Common On-Boarding Problems for Online Music Stores</span></span>

<span data-ttu-id="fb6c4-105">以下是您應該嘗試避免的常見 Windows Media Player 內建問題清單。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-105">Here is a list of common Windows Media Player on-boarding problems you should try to avoid.</span></span> <span data-ttu-id="fb6c4-106">任何這些問題都會導致您的存放區無法通過驗證測試。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-106">Any of these issues can cause your store to fail validation testing.</span></span> <span data-ttu-id="fb6c4-107">若未通過 RC2，將會延遲啟動，直到下一個可用的啟動視窗為止。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-107">Failing the RC2 pass will postpone your launch until the next available launch window.</span></span>

1.  <span data-ttu-id="fb6c4-108">無法從測試伺服器轉換到實際執行伺服器</span><span class="sxs-lookup"><span data-stu-id="fb6c4-108">Failure to transition from test servers to production servers</span></span>
    -   <span data-ttu-id="fb6c4-109">遺漏的頁面</span><span class="sxs-lookup"><span data-stu-id="fb6c4-109">Missing pages</span></span>
    -   <span data-ttu-id="fb6c4-110">IIS 設定 (存取、VRoots、HTTPs 或其他安全性設定) </span><span class="sxs-lookup"><span data-stu-id="fb6c4-110">IIS settings (Access, VRoots, https or other security settings)</span></span>
    -   <span data-ttu-id="fb6c4-111">測試帳戶無法再運作。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-111">Test accounts don't work anymore.</span></span>
    -   <span data-ttu-id="fb6c4-112">測試帳戶未套用信用額度。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-112">Test accounts don't have credits applied.</span></span>
    -   <span data-ttu-id="fb6c4-113">服務託管標誌不會被移動。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-113">Service hosted logos don't get moved.</span></span>
    -   <span data-ttu-id="fb6c4-114">先前已有重複發生的 IP 限制。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-114">IP restrictions that have been previously worked around re-occur.</span></span> <span data-ttu-id="fb6c4-115">尤其是，電子商務系統可能會有一組不同于音樂網站的限制。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-115">In particular, e-commerce systems might have a different set of restrictions from the music site.</span></span>
    -   <span data-ttu-id="fb6c4-116">ServiceInfo 檔不會更新以指向生產環境。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-116">The ServiceInfo document doesn't get updated to point to production.</span></span>
2.  <span data-ttu-id="fb6c4-117">立即播放區域中的 [購買] 連結 (或 [商店] 連結) 無效。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-117">The Buy link (or Shop link) in the Now Playing area is invalid.</span></span> <span data-ttu-id="fb6c4-118">這是經常被忽略的問題，而且會導致您的存放區即使在其他任何專案都處於正常運作的情況下也會失敗。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-118">This is a commonly overlooked issue, and it will cause your store to fail even when everything else is in working order.</span></span>
3.  <span data-ttu-id="fb6c4-119">Microsoft 的測試人員必須有足夠的購買能力。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-119">Microsoft's testers must have adequate purchasing power.</span></span> <span data-ttu-id="fb6c4-120">Microsoft 的驗證小組將會在數個購買案例中執行，範圍從小型購買到極大型的購買。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-120">Microsoft's validation team will run through several purchasing scenarios ranging from small purchases to very large purchases.</span></span> <span data-ttu-id="fb6c4-121">您必須提供充電方式，讓它們作為商店內的取用者。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-121">You must provide a rechargeable way for them to act as consumers within your store.</span></span> <span data-ttu-id="fb6c4-122">這可以透過提供虛擬信用卡來提供各種不同的帳戶。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-122">This can range from providing a variety of accounts through providing a dummy credit card.</span></span> <span data-ttu-id="fb6c4-123">例如，如果驗證測試人員嘗試購買專輯，但只有足夠的信用額度來購買單一曲目，則存放區在 RC2 中將會失敗。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-123">As an example, a store will fail in RC2 if a validation tester attempts to buy an album but has only enough credit to buy a single track.</span></span>
4.  <span data-ttu-id="fb6c4-124">如果您在服務頁面中使用 ActiveX 控制項，請確定它們都能在所有適用的 Windows 版本上完整安裝和卸載。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-124">If you use ActiveX controls inside your service pages, ensure that they install and uninstall cleanly, both on all applicable versions of Windows.</span></span> <span data-ttu-id="fb6c4-125">若未這麼做，就會發生一般問題。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-125">Failure to do so is a typical problem.</span></span> <span data-ttu-id="fb6c4-126">線上商店上的開發人員和測試人員通常會在自己的電腦上註冊 ActiveX 控制項，但忘了在使用者的電腦上安裝控制項。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-126">Often the developers and testers at an online store have the ActiveX controls registered on their own computers but forget about installing the controls on the user's computer.</span></span>

    <span data-ttu-id="fb6c4-127">如果您的存放區安裝了外掛程式或 ActiveX 控制項，您必須提供使用者簡單的方法來將它卸載。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-127">If your store installs a plug-in or an ActiveX control, you must provide the user an easy way to uninstall it.</span></span> <span data-ttu-id="fb6c4-128">例如，Microsoft 最近發現某些線上商店安裝了 Windows Media Player 11 for Windows Vista 中的 ActiveX 控制項，但無法透過 [新增/移除程式] 功能表移除這些控制項。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-128">For example, Microsoft recently found that some online stores installed ActiveX controls in Windows Media Player 11 for Windows Vista that could not be removed through the Add/Remove Programs menu.</span></span> <span data-ttu-id="fb6c4-129">經過一些調查之後，Microsoft 發現 ActiveX 控制項可以透過 Internet Explorer 的附加元件管理員來移除。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-129">After some investigation, Microsoft found that the ActiveX controls could be removed through the Add-on manager in Internet Explorer.</span></span> <span data-ttu-id="fb6c4-130">請務必透過說明檔傳達 (，至少) 安裝和卸載 ActiveX 控制項和外掛程式的方式。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-130">It's important that you communicate (through a Help file, at the least) the way to install and uninstall ActiveX controls and plug-ins.</span></span>

    <span data-ttu-id="fb6c4-131">如需有關如何將您的存放區與 Windows Vista 中的安全性基礎結構整合的詳細資訊，請參閱標題為「 [應用程式在最低許可權環境中的開發人員最佳做法和指導方針](/previous-versions/aa905330(v=msdn.10))」一文。</span><span class="sxs-lookup"><span data-stu-id="fb6c4-131">For more information on how to integrate your store with the security infrastructure in Windows Vista, see the article titled ["Developer Best Practices and Guidelines for Applications in a Least Privileged Environment"](/previous-versions/aa905330(v=msdn.10)).</span></span>

 

 
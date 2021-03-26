---
title: 更新 Orchestrator API
description: UpdateOrchestrator 會排程您的自動軟體更新，並考慮使用者的影響。
ms.date: 01/14/2021
ms.topic: overview
ms.openlocfilehash: a172cccdc56d2c645bb4e7d048066ca34aea07ba
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "103853179"
---
# <a name="updateorchestrator-api"></a><span data-ttu-id="45943-103">UpdateOrchestrator API</span><span class="sxs-lookup"><span data-stu-id="45943-103">UpdateOrchestrator API</span></span>

<span data-ttu-id="45943-104">**UpdateOrchestrator** 會排程您的自動軟體更新，並考慮使用者的影響。</span><span class="sxs-lookup"><span data-stu-id="45943-104">**UpdateOrchestrator** schedules your automatic software updates with user impact in mind.</span></span> <span data-ttu-id="45943-105">此 API 可讓您排程自動下載和安裝，以及它們的需求，以在最接近使用者的影響的最佳時間執行更新。</span><span class="sxs-lookup"><span data-stu-id="45943-105">This API allows you schedule automatic download and installs, along with their requirements in order to run updates at an optimal time that minimizes user-present impact.</span></span> <span data-ttu-id="45943-106">這些功能特別能以受限或較慢的運算資源，以較低的效能系統來獲益。</span><span class="sxs-lookup"><span data-stu-id="45943-106">These features particularly benefit lower performance systems with limited or slower computing resources.</span></span>

<span data-ttu-id="45943-107">Windows 19H1 包含第一代解決方案，適用于 OS 更新所採用的自動軟體更新使用案例和儲存應用程式更新，並公開此 API 的初始「有限存取」版本，適用于一組更新程式的「使用者模式」應用程式，如下所述。</span><span class="sxs-lookup"><span data-stu-id="45943-107">Windows 19H1 includes a first-generation solution for automatic software update use cases that were adopted by OS updates and Store App updates and exposes an initial ‘Limited Access’ version of this API for a select set of updaters of 'user-mode' apps as described below.</span></span>

## <a name="features"></a><span data-ttu-id="45943-108">功能</span><span class="sxs-lookup"><span data-stu-id="45943-108">Features</span></span>

- <span data-ttu-id="45943-109">以動態方式註冊軟體更新程式</span><span class="sxs-lookup"><span data-stu-id="45943-109">Dynamically registers software updaters</span></span>
 
- <span data-ttu-id="45943-110">在優化期間叫用已註冊的軟體更新程式，例如在使用者不存在的情況下，更新「使用者模式應用程式」。</span><span class="sxs-lookup"><span data-stu-id="45943-110">Invokes registered software updaters during optimal times, such as during user absence, to update 'user mode apps'.</span></span>
    - <span data-ttu-id="45943-111">包含在 AC 電源上「保持喚醒」的功能，可進一步降低使用者的影響。</span><span class="sxs-lookup"><span data-stu-id="45943-111">Includes the ability to 'keep awake' on AC power to further reduce user-away impact.</span></span>

- <span data-ttu-id="45943-112">在只叫用受信任的協力廠商註冊軟體的信任模型上運作更新程式</span><span class="sxs-lookup"><span data-stu-id="45943-112">Operates on a Trust Model that only invokes trusted 3rd party registered software updaters</span></span>
    - <span data-ttu-id="45943-113">將 UpdateOrchestrator 公開給任何和所有呼叫端（例如，在使用者不存在時更新 BIOS 固件或驅動程式）時，會有相當大的風險。</span><span class="sxs-lookup"><span data-stu-id="45943-113">There are substantial risks when exposing UpdateOrchestrator to any and all callers such as updating BIOS firmware or drivers when a user is not present.</span></span>  <span data-ttu-id="45943-114">UpdateOrchestrator 包含可減輕這些風險的信任模型。</span><span class="sxs-lookup"><span data-stu-id="45943-114">UpdateOrchestrator includes a trust model to mitigate these risks.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="45943-115">開發人員讀者</span><span class="sxs-lookup"><span data-stu-id="45943-115">Developer Audience</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45943-116">UpdateOrchestrator API 目前為有限的 [存取功能](/uwp/api/windows.applicationmodel.limitedaccessfeatures)。</span><span class="sxs-lookup"><span data-stu-id="45943-116">The UpdateOrchestrator API is currently a [limited access feature](/uwp/api/windows.applicationmodel.limitedaccessfeatures).</span></span> <span data-ttu-id="45943-117">此 API 將會在未來的版本中公開提供。</span><span class="sxs-lookup"><span data-stu-id="45943-117">This API will become publicly available in a future release.</span></span>

<span data-ttu-id="45943-118">如果您已經有適用于 Win32 「使用者模式」應用程式的背景軟體更新程式，例如適用于 Acrobat Reader 或閥門串流的 Adobe 更新程式，請使用 UpdateOrchestrator API。</span><span class="sxs-lookup"><span data-stu-id="45943-118">Use UpdateOrchestrator API if you already have background software updaters for Win32 'user mode' applications such as Adobe's updater for Acrobat Reader or Valve's Steam.</span></span> <span data-ttu-id="45943-119">UWP/Store 應用程式不需要此介面，因為 Microsoft Store 已經利用此功能來進行軟體更新。</span><span class="sxs-lookup"><span data-stu-id="45943-119">This interface is not needed for UWP/Store applications as the Microsoft Store already takes advantage of this functionality for software updates.</span></span>

<span data-ttu-id="45943-120">為了提供最佳的客戶體驗，此初始 API 版本的範圍是一組符合下列準則的已註冊更新程式：</span><span class="sxs-lookup"><span data-stu-id="45943-120">To provide the best customer experience, this initial API release is scoped to a select set of registered updaters that meet the following criteria:</span></span>

- <span data-ttu-id="45943-121">僅限「使用者模式」應用程式的更新</span><span class="sxs-lookup"><span data-stu-id="45943-121">Updates for 'user mode' applications only</span></span>
- <span data-ttu-id="45943-122">不涉及 BIOS/固件/裝置或軟體驅動程式</span><span class="sxs-lookup"><span data-stu-id="45943-122">Do not involve BIOS/Firmware/Device or Software Drivers</span></span>
    - <span data-ttu-id="45943-123">更新未通過一般品質準則的 BIOS、固件或裝置/軟體驅動程式會造成重大風險，特別是當使用者不存在時。</span><span class="sxs-lookup"><span data-stu-id="45943-123">Updating BIOS, firmware, or device/software drivers that have not passed a common quality criteria pose a substantial risk, particularly when a user is not present.</span></span> 
- <span data-ttu-id="45943-124">參與此 API 的使用方式，需要能夠擔保您的背景軟體更新程式在使用者系統上透過審核所下載及安裝的所有內容。</span><span class="sxs-lookup"><span data-stu-id="45943-124">Participating in the usage of this API entails being able to vouch for all content downloaded and installed by your background software updaters on users systems via audits.</span></span> 

<span data-ttu-id="45943-125">此 API 可能會在公開發行之前大幅修改。</span><span class="sxs-lookup"><span data-stu-id="45943-125">This API may be modified significantly before public release.</span></span>   <span data-ttu-id="45943-126">在開發 UpdateOrchestrator API 時，此初始版本為限制存取功能，僅適用于目前符合上述準則的更新程式。</span><span class="sxs-lookup"><span data-stu-id="45943-126">While UpdateOrchestrator API is under development, this initial release as limited access feature is only for updaters that meet above criteria at this time.</span></span>

<span data-ttu-id="45943-127">我們的目標是要改善此 API 的功能，並減少在 Windows 上更新程式多個自動軟體的影響。</span><span class="sxs-lookup"><span data-stu-id="45943-127">Our aim is to improve the functionality of this API and reduce impact from multiple automatic software updaters on Windows.</span></span> <span data-ttu-id="45943-128">我們會透過這 [**份簡短問卷**](https://aka.ms/UOAPISurvey) 來感謝您的輸入，以協助我們瞭解 UpdateOrchestrator API 如何能更妥善地滿足您的開發人員需求。</span><span class="sxs-lookup"><span data-stu-id="45943-128">We would appreciate your input through this [**brief survey**](https://aka.ms/UOAPISurvey) to help us understand how UpdateOrchestrator API can better serve your developer needs.</span></span>


---
description: 隔離是 AppContainer 執行環境的主要目標。
ms.assetid: 13C579F9-7F9F-4602-9B03-08CD820C3BBA
title: AppContainer 隔離
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82fec44fd3d6eb9495370c42e52726ceb0f63806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194057"
---
# <a name="appcontainer-isolation"></a><span data-ttu-id="92c36-103">AppContainer 隔離</span><span class="sxs-lookup"><span data-stu-id="92c36-103">AppContainer Isolation</span></span>

<span data-ttu-id="92c36-104">隔離是 AppContainer 執行環境的主要目標。</span><span class="sxs-lookup"><span data-stu-id="92c36-104">Isolation is the primary goal of an AppContainer execution environment.</span></span> <span data-ttu-id="92c36-105">藉由將應用程式與不需要的資源和其他應用程式隔離，可將惡意操作的機會降到最低。</span><span class="sxs-lookup"><span data-stu-id="92c36-105">By isolating an application from unneeded resources and other applications, opportunities for malicious manipulation are minimized.</span></span> <span data-ttu-id="92c36-106">根據最低許可權授與存取權，可防止應用程式和使用者存取其權利以外的資源。</span><span class="sxs-lookup"><span data-stu-id="92c36-106">Granting access based upon least-privilege prevents applications and users from accessing resources beyond their rights.</span></span> <span data-ttu-id="92c36-107">控制資源的存取可保護進程、裝置和網路。</span><span class="sxs-lookup"><span data-stu-id="92c36-107">Controlling access to resources protects the process, the device, and the network.</span></span>

<span data-ttu-id="92c36-108">Windows 中的大部分弱點都是從應用程式開始。</span><span class="sxs-lookup"><span data-stu-id="92c36-108">Most vulnerabilities in Windows start with the application.</span></span> <span data-ttu-id="92c36-109">一些常見的範例包括從其瀏覽器中斷的應用程式，或是將錯誤檔傳送至 Internet Explorer 以及利用外掛程式（例如 flash）。</span><span class="sxs-lookup"><span data-stu-id="92c36-109">Some common examples include an application breaking out of its browser or sending a bad document to Internet Explorer as well as exploitation of plugins, such as flash.</span></span> <span data-ttu-id="92c36-110">這些應用程式可以在 AppContainer 中隔離，而裝置和資源就越安全。</span><span class="sxs-lookup"><span data-stu-id="92c36-110">The more these applications can be isolated in an AppContainer, the safer the device and resources are.</span></span> <span data-ttu-id="92c36-111">即使應用程式中的弱點遭到惡意探索，應用程式仍無法存取授與 AppContainer 以外的資源。</span><span class="sxs-lookup"><span data-stu-id="92c36-111">Even if vulnerability in an app is exploited, the app cannot access resources beyond what is granted to the AppContainer.</span></span> <span data-ttu-id="92c36-112">惡意應用程式無法接管電腦的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="92c36-112">Malicious apps cannot take over the rest of the machine.</span></span>

## <a name="credential-isolation"></a><span data-ttu-id="92c36-113">認證隔離</span><span class="sxs-lookup"><span data-stu-id="92c36-113">Credential Isolation</span></span>

<span data-ttu-id="92c36-114">若要管理身分識別和認證，AppContainer 會防止使用使用者認證來存取資源或登入其他環境。</span><span class="sxs-lookup"><span data-stu-id="92c36-114">Managing identity and credentials, the AppContainer prevents the use of user credentials to gain access to resources or login to other environments.</span></span> <span data-ttu-id="92c36-115">AppContainer 環境會建立識別碼，其利用使用者和應用程式的組合身分識別，因此認證對每個使用者/應用程式配對而言都是唯一的，且應用程式無法模擬使用者。</span><span class="sxs-lookup"><span data-stu-id="92c36-115">The AppContainer environment creates an identifier that uses the combined identities of the user and the application, so credentials are unique to each user/application pairing and the application cannot impersonate the user.</span></span>

## <a name="device-isolation"></a><span data-ttu-id="92c36-116">裝置隔離</span><span class="sxs-lookup"><span data-stu-id="92c36-116">Device Isolation</span></span>

<span data-ttu-id="92c36-117">將應用程式與裝置資源隔離，例如被動式感應器 (攝影機、麥克風、GPS) 和貨幣泵 (3G/4G、撥打電話) AppContainer 環境會防止應用程式惡意利用裝置。</span><span class="sxs-lookup"><span data-stu-id="92c36-117">Isolating the application from device resources, such as passive sensors (camera, microphone, GPS), and money pumps (3G/4G, dial phone) the AppContainer environment prevents the application from maliciously exploiting the device.</span></span> <span data-ttu-id="92c36-118">依預設會封鎖這些資源，並且可以視需要授與存取權。</span><span class="sxs-lookup"><span data-stu-id="92c36-118">These resources are blocked by default and can be granted access as necessary.</span></span> <span data-ttu-id="92c36-119">在某些情況下，這些資源會由「訊息代理程式」進一步保護。</span><span class="sxs-lookup"><span data-stu-id="92c36-119">In some cases these resources are further protected by 'brokers'.</span></span> <span data-ttu-id="92c36-120">有些資源（例如鍵盤和滑鼠）一律可供 AppContainer 和常駐應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="92c36-120">Some resources, such as keyboard and mouse, are always available to the AppContainer and resident application.</span></span>

## <a name="file-isolation"></a><span data-ttu-id="92c36-121">檔案隔離</span><span class="sxs-lookup"><span data-stu-id="92c36-121">File Isolation</span></span>

<span data-ttu-id="92c36-122">控制檔案和登錄存取，AppContainer 環境可防止應用程式修改不應使用的檔案。</span><span class="sxs-lookup"><span data-stu-id="92c36-122">Controlling file and registry access, the AppContainer environment prevents the application from modifying files that it should not.</span></span> <span data-ttu-id="92c36-123">可將讀寫存取權授與特定的持續性檔案和登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="92c36-123">Read-write access can be granted to specific persistent files and registry keys.</span></span> <span data-ttu-id="92c36-124">唯讀存取的限制較少。</span><span class="sxs-lookup"><span data-stu-id="92c36-124">Read-only access is less restricted.</span></span> <span data-ttu-id="92c36-125">應用程式一律可以存取專為該 AppContainer 建立的記憶體常駐檔案。</span><span class="sxs-lookup"><span data-stu-id="92c36-125">An application always has access to the memory resident files created specifically for that AppContainer.</span></span>

## <a name="network-isolation"></a><span data-ttu-id="92c36-126">網路隔離</span><span class="sxs-lookup"><span data-stu-id="92c36-126">Network Isolation</span></span>

<span data-ttu-id="92c36-127">除了特別配置的網路資源之外，AppContainer 還可防止應用程式「將其環境「進行」「進行」，並惡意地利用網路資源。</span><span class="sxs-lookup"><span data-stu-id="92c36-127">Isolating the application from network resources beyond those specifically allocated, AppContainer prevents the application from 'escaping' its environment and maliciously exploiting network resources.</span></span> <span data-ttu-id="92c36-128">您可以授與存取網際網路、內部網路存取，以及做為伺服器的細微存取權。</span><span class="sxs-lookup"><span data-stu-id="92c36-128">Granular access can be granted for Internet access, Intranet access, and acting as a server.</span></span>

## <a name="process-isolation"></a><span data-ttu-id="92c36-129">處理序隔離</span><span class="sxs-lookup"><span data-stu-id="92c36-129">Process Isolation</span></span>

<span data-ttu-id="92c36-130">將應用程式核心物件沙箱化，AppContainer 環境可防止應用程式影響或受到其他應用程式進程的影響。</span><span class="sxs-lookup"><span data-stu-id="92c36-130">Sandboxing the application kernel objects, the AppContainer environment prevents the application from influencing, or being influenced by, other application processes.</span></span> <span data-ttu-id="92c36-131">這可防止適當包含的應用程式在發生例外狀況時損毀其他進程。</span><span class="sxs-lookup"><span data-stu-id="92c36-131">This prevents a properly contained application from corrupting other processes in the event of an exception.</span></span>

## <a name="window-isolation"></a><span data-ttu-id="92c36-132">視窗隔離</span><span class="sxs-lookup"><span data-stu-id="92c36-132">Window Isolation</span></span>

<span data-ttu-id="92c36-133">將應用程式與其他視窗隔離，AppContainer 環境可防止應用程式影響其他應用程式介面。</span><span class="sxs-lookup"><span data-stu-id="92c36-133">Isolating the application from other windows, the AppContainer environment prevents the application from affecting other application interfaces.</span></span>

 

 




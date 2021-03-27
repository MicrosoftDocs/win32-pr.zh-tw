---
description: 基本上不會有如何撰寫自動執行時間啟動應用程式的限制。
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: 如何執行自動啟動應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944189"
---
# <a name="how-to-implement-autorun-startup-applications"></a><span data-ttu-id="e9512-103">如何執行自動啟動應用程式</span><span class="sxs-lookup"><span data-stu-id="e9512-103">How to Implement AutoRun Startup Applications</span></span>

<span data-ttu-id="e9512-104">基本上不會有如何撰寫自動執行時間啟動應用程式的限制。</span><span class="sxs-lookup"><span data-stu-id="e9512-104">There are essentially no constraints on how to write an AutoRun startup application.</span></span> <span data-ttu-id="e9512-105">您可以執行啟動應用程式，以執行您在安裝、卸載、設定或執行應用程式時所需的任何動作。</span><span class="sxs-lookup"><span data-stu-id="e9512-105">You can implement the startup application to do whatever you find necessary to install, uninstall, configure, or run your application.</span></span> <span data-ttu-id="e9512-106">但是，下列秘訣提供一些指導方針來執行有效的自動執行啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="e9512-106">However, the following tips provide some guidelines to implementing an effective AutoRun startup application.</span></span>

## <a name="instructions"></a><span data-ttu-id="e9512-107">指示</span><span class="sxs-lookup"><span data-stu-id="e9512-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="e9512-108">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="e9512-108">Step 1:</span></span>

<span data-ttu-id="e9512-109">請確定使用者在將自動執行光碟插入磁片磁碟機之後，儘快收到意見反應。</span><span class="sxs-lookup"><span data-stu-id="e9512-109">Make sure that users receive feedback as soon as possible after they insert an AutoRun disc into the drive.</span></span> <span data-ttu-id="e9512-110">啟動應用程式應該是快速載入的小程式。</span><span class="sxs-lookup"><span data-stu-id="e9512-110">Startup applications should be small programs that load quickly.</span></span> <span data-ttu-id="e9512-111">他們應該清楚地識別應用程式，並提供簡單的方法來取消作業。</span><span class="sxs-lookup"><span data-stu-id="e9512-111">They should clearly identify the application and provide an easy way to cancel the operation.</span></span>

### <a name="step-2"></a><span data-ttu-id="e9512-112">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="e9512-112">Step 2:</span></span>

<span data-ttu-id="e9512-113">查看是否已安裝程式。</span><span class="sxs-lookup"><span data-stu-id="e9512-113">Check to see if the program is already installed.</span></span> <span data-ttu-id="e9512-114">如果沒有，則下一個步驟可能會是安裝程式。</span><span class="sxs-lookup"><span data-stu-id="e9512-114">If not, the next step will probably be the setup procedure.</span></span> <span data-ttu-id="e9512-115">啟動應用程式可以透過啟動另一個執行緒開始載入安裝程式碼，來利用使用者花在閱讀對話方塊的時間。</span><span class="sxs-lookup"><span data-stu-id="e9512-115">The startup application can take advantage of the time the user spends reading the dialog box by starting another thread to begin loading the setup code.</span></span> <span data-ttu-id="e9512-116">當使用者按一下 **[確定]** 時，如果未完全載入您的安裝程式，您的安裝程式將會部分存在。</span><span class="sxs-lookup"><span data-stu-id="e9512-116">By the time the user clicks **OK**, your setup program will already be partly if not fully loaded.</span></span> <span data-ttu-id="e9512-117">這種方法可大幅減少使用者在載入應用程式時所需的時間量。</span><span class="sxs-lookup"><span data-stu-id="e9512-117">This approach significantly reduces the user's perception of the amount of time it takes to load your application.</span></span>

> [!Note]  
> <span data-ttu-id="e9512-118">啟動應用程式的初始部分通常會為使用者提供使用者介面（例如對話方塊），詢問他們要如何繼續進行。</span><span class="sxs-lookup"><span data-stu-id="e9512-118">Typically, the initial part of the startup application presents users with a user interface, such as a dialog box, asking them how they would like to proceed.</span></span>

 

### <a name="step-3"></a><span data-ttu-id="e9512-119">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="e9512-119">Step 3:</span></span>

<span data-ttu-id="e9512-120">啟動另一個執行緒開始載入應用程式程式碼，縮短使用者的等候時間。</span><span class="sxs-lookup"><span data-stu-id="e9512-120">Start another thread to begin loading application code to shorten the waiting time for the user.</span></span> <span data-ttu-id="e9512-121">如果已安裝應用程式，使用者可能會插入磁片來執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="e9512-121">If the application has already been installed, the user probably inserted the disk to run the application.</span></span>

### <a name="step-4"></a><span data-ttu-id="e9512-122">步驟 4：</span><span class="sxs-lookup"><span data-stu-id="e9512-122">Step 4:</span></span>

<span data-ttu-id="e9512-123">使用下列提示可將硬碟使用方式降至最低：</span><span class="sxs-lookup"><span data-stu-id="e9512-123">Use the following hints to minimize hard disk usage:</span></span>

-   <span data-ttu-id="e9512-124">將必須放在硬碟上的檔案數目維持在最小值。</span><span class="sxs-lookup"><span data-stu-id="e9512-124">Keep the number of files that must be on the hard disk to a minimum.</span></span> <span data-ttu-id="e9512-125">它們應該限制為執行程式所需的檔案，或是從媒體讀取的大量時間。</span><span class="sxs-lookup"><span data-stu-id="e9512-125">They should be restricted to files that are essential to running the program or that would take an unacceptably large amount of time to read from the media.</span></span>
-   <span data-ttu-id="e9512-126">在許多情況下，不需要在硬碟上安裝非必要的檔案，但可能會提供提升效能的優點。</span><span class="sxs-lookup"><span data-stu-id="e9512-126">In many cases, installing nonessential files on the hard disk is not necessary, but might provide benefits such as increased performance.</span></span> <span data-ttu-id="e9512-127">為使用者提供選項，決定如何在硬碟儲存體的成本與效益之間進行取捨。</span><span class="sxs-lookup"><span data-stu-id="e9512-127">Give the user the option of deciding how to make the trade-off between the costs and benefits of hard disk storage.</span></span>
-   <span data-ttu-id="e9512-128">提供一種方法，將任何已放置於硬碟上的元件卸載。</span><span class="sxs-lookup"><span data-stu-id="e9512-128">Provide a way to uninstall any components that were placed on the hard disk.</span></span>
-   <span data-ttu-id="e9512-129">如果您的應用程式會快取資料，請提供使用者對它的一些控制權。</span><span class="sxs-lookup"><span data-stu-id="e9512-129">If your application caches data, give the user some control over it.</span></span> <span data-ttu-id="e9512-130">在啟動應用程式中包含選項，例如設定將儲存在硬碟上的最大快取資料量上限，或讓應用程式在終止時捨棄任何快取的資料。</span><span class="sxs-lookup"><span data-stu-id="e9512-130">Include options in the startup application such as setting a limit on the maximum amount of cached data that will be stored on the hard disk, or having the application discard any cached data when it terminates.</span></span>

### <a name="step-5"></a><span data-ttu-id="e9512-131">步驟 5：</span><span class="sxs-lookup"><span data-stu-id="e9512-131">Step 5:</span></span>

<span data-ttu-id="e9512-132">視需要停用自動播放。</span><span class="sxs-lookup"><span data-stu-id="e9512-132">Disable Autorun if needed.</span></span> <span data-ttu-id="e9512-133">您可以透過程式設計的方式，完全隱藏自動執行時間，即使媒體具有自動完成 .inf 檔案也一樣。</span><span class="sxs-lookup"><span data-stu-id="e9512-133">AutoRun can be suppressed programmatically or disabled entirely with the registry, even when a medium has an Autorun.inf file.</span></span> <span data-ttu-id="e9512-134">如需詳細資訊，請參閱 [啟用和停用自動](autoplay-reg.md) 啟動。</span><span class="sxs-lookup"><span data-stu-id="e9512-134">See [Enabling and Disabling AutoRun](autoplay-reg.md) for more information.</span></span>

 

 




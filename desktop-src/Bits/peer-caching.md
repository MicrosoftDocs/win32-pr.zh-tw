---
title: 對等快取
description: 從背景智慧型傳送服務 (位) 4.0 開始，BITS 服務已擴充為允許使用 Windows BranchCache 下載的 URL 資料的子網層級對等快取。
ms.assetid: 4197eed3-1812-4440-99e7-9462635ef6ad
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 3c87e6013bb37610e934c13414bd2636407108ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965437"
---
# <a name="peer-caching"></a><span data-ttu-id="982c5-103">對等快取</span><span class="sxs-lookup"><span data-stu-id="982c5-103">Peer Caching</span></span>

<span data-ttu-id="982c5-104">從背景智慧型傳送服務 (位) 4.0 開始，BITS 服務已擴充為允許使用 Windows BranchCache 下載的 URL 資料的子網層級對等快取。</span><span class="sxs-lookup"><span data-stu-id="982c5-104">Starting with Background Intelligent Transfer Service (BITS) 4.0, the BITS service was extended to allow subnet-level peer caching for downloaded URL data by using Windows BranchCache.</span></span> <span data-ttu-id="982c5-105">BITS 用戶端可以從自己的子網中已下載資料的其他電腦抓取資料，而不是從遠端伺服器取得資料。</span><span class="sxs-lookup"><span data-stu-id="982c5-105">BITS clients can retrieve data from other computers in their own subnet that have already downloaded the data, instead of retrieving the data from remote servers.</span></span> <span data-ttu-id="982c5-106">如需 Windows BranchCache 的詳細資訊，請參閱 [BranchCache 總覽](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="982c5-106">For more information about Windows BranchCache, see the [BranchCache Overview](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).</span></span>

<span data-ttu-id="982c5-107">如果系統管理員透過群組原則或本機設定設定，在組織中的用戶端和伺服器電腦上啟用 Windows BranchCache，BITS 將會使用 Windows BranchCache 進行資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="982c5-107">If an administrator enables Windows BranchCache on client and server computers in an organization through a group policy or local configuration settings, BITS will use Windows BranchCache for data transfers.</span></span>

-   [<span data-ttu-id="982c5-108">BITS 4.0 對等快取的設定</span><span class="sxs-lookup"><span data-stu-id="982c5-108">Configuration for BITS 4.0 Peer Caching</span></span>](#configuration-for-bits-40-peer-caching)
-   [<span data-ttu-id="982c5-109">停用 Windows BranchCache</span><span class="sxs-lookup"><span data-stu-id="982c5-109">Disabling Windows BranchCache</span></span>](#disabling-windows-branchcache)
-   [<span data-ttu-id="982c5-110">驗證和監視</span><span class="sxs-lookup"><span data-stu-id="982c5-110">Verification and Monitoring</span></span>](#verification-and-monitoring)
-   [<span data-ttu-id="982c5-111">BITS 3.0 中的對等快取</span><span class="sxs-lookup"><span data-stu-id="982c5-111">Peer Caching in BITS 3.0</span></span>](#peer-caching-in-bits-30)

## <a name="configuration-for-bits-40-peer-caching"></a><span data-ttu-id="982c5-112">BITS 4.0 對等快取的設定</span><span class="sxs-lookup"><span data-stu-id="982c5-112">Configuration for BITS 4.0 Peer Caching</span></span>

<span data-ttu-id="982c5-113">需要下列設定，BITS 4.0 中的對等快取才能運作：</span><span class="sxs-lookup"><span data-stu-id="982c5-113">The following configuration is required for peer caching in BITS 4.0 to function:</span></span>

-   <span data-ttu-id="982c5-114">您必須透過群組原則或本機設定，在用戶端上啟用 Windows BranchCache。</span><span class="sxs-lookup"><span data-stu-id="982c5-114">Windows BranchCache must be enabled on the client through a group policy or local configuration settings.</span></span> <span data-ttu-id="982c5-115">如需詳細資訊，請參閱 [BranchCache 用戶端](/previous-versions/windows/it-pro/windows-7/dd637820(v=ws.10))設定。</span><span class="sxs-lookup"><span data-stu-id="982c5-115">For more information, see [BranchCache client configuration](/previous-versions/windows/it-pro/windows-7/dd637820(v=ws.10)).</span></span>
    > [!Note]  
    > <span data-ttu-id="982c5-116">Windows BranchCache 功能預設為停用。</span><span class="sxs-lookup"><span data-stu-id="982c5-116">The Windows BranchCache feature is disabled by default.</span></span>

     

-   <span data-ttu-id="982c5-117">Windows BranchCache 功能是必須安裝在伺服器上的選擇性元件。</span><span class="sxs-lookup"><span data-stu-id="982c5-117">The Windows BranchCache feature is an optional component that must be installed on the server.</span></span> <span data-ttu-id="982c5-118">如需詳細資訊，請參閱 [BranchCache server configuration](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="982c5-118">For more information, see [BranchCache server configuration](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).</span></span>
-   <span data-ttu-id="982c5-119">伺服器也必須透過群組原則或本機設定來啟用 Windows BranchCache 功能。</span><span class="sxs-lookup"><span data-stu-id="982c5-119">The server must also enable the Windows BranchCache feature though group policy or local configuration settings.</span></span> <span data-ttu-id="982c5-120">如需詳細資訊，請參閱 [BranchCache server configuration](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="982c5-120">For more information, see [BranchCache server configuration](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).</span></span>
    > [!Note]  
    > <span data-ttu-id="982c5-121">Windows BranchCache 功能預設為停用。</span><span class="sxs-lookup"><span data-stu-id="982c5-121">The Windows BranchCache feature is disabled by default.</span></span>

     

<span data-ttu-id="982c5-122">預設的 BITS 群組原則允許對等快取。</span><span class="sxs-lookup"><span data-stu-id="982c5-122">The default BITS group policy allows peer caching.</span></span> <span data-ttu-id="982c5-123">如果電腦上的 Windows BranchCache 是全域啟用的，則也會啟用 BITS 傳送工作的這項功能。</span><span class="sxs-lookup"><span data-stu-id="982c5-123">If Windows BranchCache is enabled globally on a computer, this feature is also enabled for BITS transfer jobs.</span></span> <span data-ttu-id="982c5-124">如需有關 BITS 特定群組原則的詳細資訊，請參閱 [群組原則](group-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="982c5-124">For more information about the BITS-specific group policies, see [Group Policies](group-policies.md).</span></span>

## <a name="disabling-windows-branchcache"></a><span data-ttu-id="982c5-125">停用 Windows BranchCache</span><span class="sxs-lookup"><span data-stu-id="982c5-125">Disabling Windows BranchCache</span></span>

<span data-ttu-id="982c5-126">系統管理員可以使用群組原則來停用 Windows BranchCache。</span><span class="sxs-lookup"><span data-stu-id="982c5-126">An administrator can use a group policy to disable the use of the Windows BranchCache.</span></span> <span data-ttu-id="982c5-127"> (請參閱 [群組原則](group-policies.md)。 ) 如果已停用 Windows BRANCHCACHE，BITS 用戶端只會從遠端伺服器取出資料。</span><span class="sxs-lookup"><span data-stu-id="982c5-127">(See [Group Policies](group-policies.md).) If the Windows BranchCache is disabled, BITS clients will retrieve data only from remote servers.</span></span>

<span data-ttu-id="982c5-128">應用程式也可以藉由呼叫 [**IBackgroundCopyJob4：： SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) 方法並設定 **BG \_ 停用 \_ 分支 \_** 快取旗標，以每個作業為基礎停用 Windows BranchCache。</span><span class="sxs-lookup"><span data-stu-id="982c5-128">An application can also disable the Windows BranchCache on a per job basis by calling the [**IBackgroundCopyJob4::SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) method and setting the **BG\_DISABLE\_BRANCH\_CACHE** flag.</span></span>

> [!Note]  
> <span data-ttu-id="982c5-129">這些設定不會影響 BITS 以外的應用程式使用 Windows BranchCache。</span><span class="sxs-lookup"><span data-stu-id="982c5-129">These settings do not affect the use of Windows BranchCache by applications other than BITS.</span></span> <span data-ttu-id="982c5-130">這些設定不適用於透過 SMB 的 BITS 傳輸。</span><span class="sxs-lookup"><span data-stu-id="982c5-130">These settings do not apply to BITS transfers over SMB.</span></span> <span data-ttu-id="982c5-131">BITS 不會控制 Windows BranchCache 透過 SMB 傳送的任何設定。</span><span class="sxs-lookup"><span data-stu-id="982c5-131">BITS does not control any settings for Windows BranchCache transfers over SMB.</span></span>

 

## <a name="verification-and-monitoring"></a><span data-ttu-id="982c5-132">驗證和監視</span><span class="sxs-lookup"><span data-stu-id="982c5-132">Verification and Monitoring</span></span>

<span data-ttu-id="982c5-133">有幾種方式可以驗證和監視對等快取統計資料。</span><span class="sxs-lookup"><span data-stu-id="982c5-133">There are a number of ways to verify and monitor peer caching statistics.</span></span> <span data-ttu-id="982c5-134">系統管理員可以呼叫 [**IBackgroundCopyFile4：： GetPeerDownloadStats**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibackgroundcopyfile4-getpeerdownloadstats) 方法，以查詢從對等和源伺服器下載的資料量。</span><span class="sxs-lookup"><span data-stu-id="982c5-134">Administrators can call the [**IBackgroundCopyFile4::GetPeerDownloadStats**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibackgroundcopyfile4-getpeerdownloadstats) method to query the amount of data that was downloaded from peers and from origin servers.</span></span> <span data-ttu-id="982c5-135">系統管理員也可以檢查事件記錄檔中的事件 [識別碼 60](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc734635(v=ws.10))，以提供作業特定的資訊。</span><span class="sxs-lookup"><span data-stu-id="982c5-135">Administrators can also check the event log for [Event ID 60](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc734635(v=ws.10)), which provides job-specific information.</span></span>

<span data-ttu-id="982c5-136">Windows BranchCache 功能也提供一些機制來驗證和監視對等快取統計資料。</span><span class="sxs-lookup"><span data-stu-id="982c5-136">The Windows BranchCache feature also provides a number of mechanisms to verify and monitor peer caching statistics.</span></span> <span data-ttu-id="982c5-137">如需詳細資訊，請參閱 [驗證和監視](/previous-versions/windows/it-pro/windows-7/dd637782(v=ws.10)) 和 [效能計數器](/previous-versions/windows/it-pro/windows-7/dd637826(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="982c5-137">For more information, see [Verification and Monitoring](/previous-versions/windows/it-pro/windows-7/dd637782(v=ws.10)) and [Performance Counters](/previous-versions/windows/it-pro/windows-7/dd637826(v=ws.10)).</span></span>

<span data-ttu-id="982c5-138">使用 Windows BranchCache 的對等快取模型會取代 BITS 3.0 中使用的對等快取模型。</span><span class="sxs-lookup"><span data-stu-id="982c5-138">The peer caching model that uses Windows BranchCache replaces the peer caching model used in BITS 3.0.</span></span> <span data-ttu-id="982c5-139">如需 Windows BranchCache 的詳細資訊，請參閱下列各項：</span><span class="sxs-lookup"><span data-stu-id="982c5-139">For more information about Windows BranchCache, see the following:</span></span>

-   <span data-ttu-id="982c5-140">[BranchCache](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj127252(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="982c5-140">[BranchCache](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj127252(v=ws.11))</span></span>
-   <span data-ttu-id="982c5-141">[BranchCache 概觀](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="982c5-141">[BranchCache Overview](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))</span></span>
-   [<span data-ttu-id="982c5-142">Windows 7 服務</span><span class="sxs-lookup"><span data-stu-id="982c5-142">Windows 7 Services</span></span>](../win7devguide/services.md)
-   [<span data-ttu-id="982c5-143">對等散發 API</span><span class="sxs-lookup"><span data-stu-id="982c5-143">Peer Distribution API</span></span>](../p2psdk/peer-distribution.md)

## <a name="peer-caching-in-bits-30"></a><span data-ttu-id="982c5-144">BITS 3.0 中的對等快取</span><span class="sxs-lookup"><span data-stu-id="982c5-144">Peer Caching in BITS 3.0</span></span>

> [!Note]  
> <span data-ttu-id="982c5-145">從 Windows 7 開始，BITS 3.0 對等快取模型已被取代。</span><span class="sxs-lookup"><span data-stu-id="982c5-145">Starting with Windows 7, the BITS 3.0 peer caching model is deprecated.</span></span> <span data-ttu-id="982c5-146">如果已安裝 BITS 4.0，BITS 3.0 對等快取模型就無法使用。</span><span class="sxs-lookup"><span data-stu-id="982c5-146">If BITS 4.0 is installed, the BITS 3.0 peer caching model is unavailable.</span></span>

 

<span data-ttu-id="982c5-147">如果系統管理員啟用對等快取，而作業允許從對等下載內容，BITS 將會嘗試從一或多個對等電腦下載內容。</span><span class="sxs-lookup"><span data-stu-id="982c5-147">If the administrator enables peer caching and the job permits downloading content from a peer, BITS will try to download the content from one or more peers.</span></span> <span data-ttu-id="982c5-148">從對等下載比從網際網路下載內容快很多。</span><span class="sxs-lookup"><span data-stu-id="982c5-148">Downloading from a peer is much faster than downloading content from the Internet.</span></span> <span data-ttu-id="982c5-149">依預設會停用對等快取，且工作必須明確允許從對等下載內容。</span><span class="sxs-lookup"><span data-stu-id="982c5-149">Peer caching is disabled by default and jobs must explicitly permit downloading content from peers.</span></span> <span data-ttu-id="982c5-150">系統管理員可以使用群組原則來啟用對等快取。</span><span class="sxs-lookup"><span data-stu-id="982c5-150">An administrator can use a group policy to enable peer caching.</span></span> <span data-ttu-id="982c5-151">啟用對等快取之後，系統管理員可以停用從對等下載，或將內容提供給對等。</span><span class="sxs-lookup"><span data-stu-id="982c5-151">After enabling peer caching, the administrator can disable either downloading from a peer or serving content to a peer.</span></span>

<span data-ttu-id="982c5-152">應用程式也可以藉由呼叫 [**IBitsPeerCacheAdministration：： SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) 方法來啟用對等快取。</span><span class="sxs-lookup"><span data-stu-id="982c5-152">An application can also enable peer caching by calling the [**IBitsPeerCacheAdministration::SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) method.</span></span> <span data-ttu-id="982c5-153">但是，如果設定，則會由群組原則設定覆寫這些設定。</span><span class="sxs-lookup"><span data-stu-id="982c5-153">However, these settings are overridden by the group policy settings, if set.</span></span>

<span data-ttu-id="982c5-154">啟用對等快取時，BITS 會建立位於相同子網且屬於相同網域的對等清單。</span><span class="sxs-lookup"><span data-stu-id="982c5-154">When peer caching is enabled, BITS creates a list of peers that are in the same subnet and belong to the same domain.</span></span> <span data-ttu-id="982c5-155">此清單不會包含來自受信任網域的對等。</span><span class="sxs-lookup"><span data-stu-id="982c5-155">The list will not include peers from a trusted domain.</span></span> <span data-ttu-id="982c5-156">對等快取只能在網域環境中啟用。</span><span class="sxs-lookup"><span data-stu-id="982c5-156">Peer caching can be enabled only in a domain environment.</span></span>

<span data-ttu-id="982c5-157">BITS 會執行下列動作來探索對等：</span><span class="sxs-lookup"><span data-stu-id="982c5-157">BITS discovers the peers by doing the following:</span></span>

-   <span data-ttu-id="982c5-158">接聽宣告本身的對等伺服器。</span><span class="sxs-lookup"><span data-stu-id="982c5-158">Listening for peer servers that announce themselves.</span></span> <span data-ttu-id="982c5-159">對等伺服器會在啟動時自行宣告。</span><span class="sxs-lookup"><span data-stu-id="982c5-159">A peer server will announce itself when it starts.</span></span> <span data-ttu-id="982c5-160">如果用戶端在其清單中需要更多對等，則 BITS 會將對等伺服器新增至清單。</span><span class="sxs-lookup"><span data-stu-id="982c5-160">BITS will add the peer server to the list if the client needs more peers in its list.</span></span>
-   <span data-ttu-id="982c5-161">當對等伺服器在其對等清單中需要更多對等時，廣播要求。</span><span class="sxs-lookup"><span data-stu-id="982c5-161">Broadcasting a request for peer servers when it needs more peers in its peer list.</span></span> <span data-ttu-id="982c5-162">可用來提供內容回應要求的對等伺服器。</span><span class="sxs-lookup"><span data-stu-id="982c5-162">Peer servers that are available to serve content respond to the request.</span></span>

<span data-ttu-id="982c5-163">如果伺服器執行下列動作，則 BITS 會從對等清單中移除對等伺服器：</span><span class="sxs-lookup"><span data-stu-id="982c5-163">BITS removes peer servers from the peer list if the server does the following:</span></span>

-   <span data-ttu-id="982c5-164">驗證失敗</span><span class="sxs-lookup"><span data-stu-id="982c5-164">Fails authentication</span></span>
-   <span data-ttu-id="982c5-165">離線 (無法使用) 太長</span><span class="sxs-lookup"><span data-stu-id="982c5-165">Is offline (unavailable) for too long</span></span>
-   <span data-ttu-id="982c5-166">提供有錯誤的憑證</span><span class="sxs-lookup"><span data-stu-id="982c5-166">Provides a certificate with errors</span></span>

<span data-ttu-id="982c5-167">當作業向對等要求內容時，BITS 會從對等清單中隨機播放對等的子集，並詢問其是否有內容。</span><span class="sxs-lookup"><span data-stu-id="982c5-167">When a job requests content from a peer, BITS randomly chooses a subset of peers from the peer list and asks them if they have the content.</span></span> <span data-ttu-id="982c5-168">BITS 只能從已驗證的對等伺服器下載內容。</span><span class="sxs-lookup"><span data-stu-id="982c5-168">BITS can download content only from authenticated peer servers.</span></span> <span data-ttu-id="982c5-169">用戶端和伺服器一開始會使用 Kerberos 進行驗證，然後在內容探索和下載期間交換自我簽署憑證以進行驗證。</span><span class="sxs-lookup"><span data-stu-id="982c5-169">The client and server initially authenticate each other using Kerberos and then exchange self-signed certificates for authentication during content discovery and download.</span></span>

<span data-ttu-id="982c5-170">BITS 會從第一個經過驗證的對等下載內容，以回應要求。</span><span class="sxs-lookup"><span data-stu-id="982c5-170">BITS downloads the content from the first authenticated peer to respond to the request.</span></span> <span data-ttu-id="982c5-171">如果其中一個對等不包含所有內容，BITS 將會從源伺服器下載其餘部分之前，從一或多個對等下載它。</span><span class="sxs-lookup"><span data-stu-id="982c5-171">If one peer does not contain all of the content, BITS will download what it can from one or more of the peers before downloading the rest from the origin server.</span></span> <span data-ttu-id="982c5-172">如果任何對等都沒有內容，或從對等下載時發生錯誤，BITS 會從源伺服器下載內容。</span><span class="sxs-lookup"><span data-stu-id="982c5-172">If none of the peers has the content or an error occurs while downloading from a peer, BITS downloads the content from the origin server.</span></span>

<span data-ttu-id="982c5-173">只有在應用程式驗證檔案內容之後，才可以將下載的內容提供給其他對等。</span><span class="sxs-lookup"><span data-stu-id="982c5-173">The downloaded content becomes available to serve to other peers only after the application validates the files contents.</span></span> <span data-ttu-id="982c5-174">如果應用程式未明確驗證檔案，則會在應用程式完成工作時，以隱含方式驗證檔案。</span><span class="sxs-lookup"><span data-stu-id="982c5-174">If the application does not explicitly validate the file, the file is implicitly validated when the application completes the job.</span></span>

<span data-ttu-id="982c5-175">根據預設，對等伺服器只能將內容提供給三個用戶端。</span><span class="sxs-lookup"><span data-stu-id="982c5-175">By default, a peer server can serve content to only three clients simultaneously.</span></span> <span data-ttu-id="982c5-176">如果伺服器目前忙於提供三個用戶端，則回應其他要求會有延遲。</span><span class="sxs-lookup"><span data-stu-id="982c5-176">If the server is currently busy serving three clients, there will be a delay in responding to other requests.</span></span> <span data-ttu-id="982c5-177">BITS 會限制用來將內容提供給 1 Mbps 的頻寬。</span><span class="sxs-lookup"><span data-stu-id="982c5-177">BITS limits the bandwidth used to serve content to 1 Mbps.</span></span> <span data-ttu-id="982c5-178">您可以使用 [MaxBandwidthServed](group-policies.md) 群組原則來變更限制。</span><span class="sxs-lookup"><span data-stu-id="982c5-178">You can use the [MaxBandwidthServed](group-policies.md) group policy to change the limit.</span></span>

> [!Note]  
> <span data-ttu-id="982c5-179">只有網域網路才支援這項功能;工作組或家用網路不支援對等快取。</span><span class="sxs-lookup"><span data-stu-id="982c5-179">This feature is supported only in domain networks; peer caching is not supported on workgroups or home networks.</span></span>

<span data-ttu-id="982c5-180">另請參閱[管理對等](/windows/desktop/Bits/administering-the-peer-cache)快取</span><span class="sxs-lookup"><span data-stu-id="982c5-180">See also [Administering the Peer Cache](/windows/desktop/Bits/administering-the-peer-cache)</span></span>
 

 

 
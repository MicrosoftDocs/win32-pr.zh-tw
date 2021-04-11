---
description: 設定錯誤的防火牆可能會導致 WSD 應用程式失敗。
ms.assetid: eba61235-29b4-463a-b7c5-d34d3b39b095
title: 檢查介面卡和防火牆設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490909c9f3acdc3025e72350118f303bfdae73d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318927"
---
# <a name="inspecting-adapter-and-firewall-settings"></a><span data-ttu-id="51e9d-103">檢查介面卡和防火牆設定</span><span class="sxs-lookup"><span data-stu-id="51e9d-103">Inspecting Adapter and Firewall Settings</span></span>

<span data-ttu-id="51e9d-104">設定錯誤的防火牆可能會導致 WSD 應用程式失敗。</span><span class="sxs-lookup"><span data-stu-id="51e9d-104">A misconfigured firewall can cause WSD applications to fail.</span></span> <span data-ttu-id="51e9d-105">本主題提供在 WSD 用戶端和主機無法在網路上看到彼此時，所要使用的一些疑難排解程式。</span><span class="sxs-lookup"><span data-stu-id="51e9d-105">This topic provides some troubleshooting procedures to use when WSD clients and hosts cannot see each other on the network.</span></span> <span data-ttu-id="51e9d-106">使用任何其他應用程式疑難排解程式之前，應該先檢查防火牆設定。</span><span class="sxs-lookup"><span data-stu-id="51e9d-106">The firewall settings should be inspected before using any other application troubleshooting procedure.</span></span>

<span data-ttu-id="51e9d-107">**檢查介面卡和防火牆設定**</span><span class="sxs-lookup"><span data-stu-id="51e9d-107">**To inspect the adapter and firewall settings**</span></span>

1.  <span data-ttu-id="51e9d-108">確認已啟用 **網路探索** 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="51e9d-108">Verify that the **Network Discovery** exception is enabled.</span></span>
2.  <span data-ttu-id="51e9d-109">確認沒有任何應用程式特定的防火牆規則封鎖應用程式。</span><span class="sxs-lookup"><span data-stu-id="51e9d-109">Check that there are no application-specific firewall rules blocking the application.</span></span>
3.  <span data-ttu-id="51e9d-110">明確啟用用於探索和中繼資料交換的埠。</span><span class="sxs-lookup"><span data-stu-id="51e9d-110">Explicitly enable the ports used for discovery and metadata exchange.</span></span>
4.  <span data-ttu-id="51e9d-111">停用防火牆，然後重新測試應用程式。</span><span class="sxs-lookup"><span data-stu-id="51e9d-111">Disable the firewall and retest the application.</span></span>
    > [!Note]  
    > <span data-ttu-id="51e9d-112">完成此步驟之後，應重新啟用防火牆。</span><span class="sxs-lookup"><span data-stu-id="51e9d-112">The firewall should be re-enabled after completing this step.</span></span>

     

## <a name="verifying-that-the-network-discovery-exception-is-enabled"></a><span data-ttu-id="51e9d-113">確認已啟用網路探索例外狀況</span><span class="sxs-lookup"><span data-stu-id="51e9d-113">Verifying that the Network Discovery exception is enabled</span></span>

<span data-ttu-id="51e9d-114">如果有任何 WS-Discovery 的應用程式正在執行，則必須允許 **網路探索** 防火牆例外。</span><span class="sxs-lookup"><span data-stu-id="51e9d-114">If any WS-Discovery applications are running, the **Network Discovery** firewall exception must be allowed.</span></span>

<span data-ttu-id="51e9d-115">**若要啟用網路探索防火牆例外狀況**</span><span class="sxs-lookup"><span data-stu-id="51e9d-115">**To enable the Network Discovery firewall exception**</span></span>

1.  <span data-ttu-id="51e9d-116">按一下 [ **開始**]，按一下 [ **執行**]，然後輸入 **firewall.cpl**。</span><span class="sxs-lookup"><span data-stu-id="51e9d-116">Click **Start**, click **Run**, and then type **firewall.cpl**.</span></span> <span data-ttu-id="51e9d-117">這會開啟 **Windows 防火牆主控台** applet。</span><span class="sxs-lookup"><span data-stu-id="51e9d-117">This opens the **Windows Firewall Control Panel** applet.</span></span>
2.  <span data-ttu-id="51e9d-118">選擇 [ **允許程式通過 Windows 防火牆**]。</span><span class="sxs-lookup"><span data-stu-id="51e9d-118">Choose **Allow a program through Windows Firewall**.</span></span>
3.  <span data-ttu-id="51e9d-119">在 [ **例外** ] 索引標籤上，選取 [ **網路探索** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="51e9d-119">On the **Exceptions** tab, select the **Network Discovery** check box.</span></span>
4.  <span data-ttu-id="51e9d-120">按一下 **[確定]** 關閉防火牆小程式。</span><span class="sxs-lookup"><span data-stu-id="51e9d-120">Click **OK** to close the firewall applet.</span></span>

<span data-ttu-id="51e9d-121">進行此防火牆變更之後，請重新測試程式。</span><span class="sxs-lookup"><span data-stu-id="51e9d-121">Retest the program after making this firewall change.</span></span> <span data-ttu-id="51e9d-122">如果程式現在可順利運作，就會識別出問題的原因，而不需要進行進一步的疑難排解步驟。</span><span class="sxs-lookup"><span data-stu-id="51e9d-122">If the program now works successfully, the cause of the problem has been identified and no further troubleshooting steps are necessary.</span></span> <span data-ttu-id="51e9d-123">否則，請移至下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="51e9d-123">Otherwise, move on to the next step.</span></span>

## <a name="checking-for-application-specific-firewall-rules"></a><span data-ttu-id="51e9d-124">檢查應用程式特定的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="51e9d-124">Checking for application-specific firewall rules</span></span>

<span data-ttu-id="51e9d-125">Windows 防火牆的 Advanced 設定可以發生在 Microsoft Management Control (MMC) 嵌入式管理單元中，名為 [ **具有 Advanced Security 的 Windows 防火牆**]。</span><span class="sxs-lookup"><span data-stu-id="51e9d-125">Advanced configuration of the Windows Firewall can take place in a Microsoft Management Control (MMC) snap-in named **Windows Firewall with Advanced Security**.</span></span> <span data-ttu-id="51e9d-126">此嵌入式管理單元可以用來針對可疑的防火牆問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="51e9d-126">This snap-in can be used to troubleshoot suspected firewall problems.</span></span>

<span data-ttu-id="51e9d-127">開發人員可以使用「 [具有 Advanced 安全性的 Windows 防火牆](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) 」 api 來建立適用于其 WSD 應用程式的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="51e9d-127">Developers can use the [Windows Firewall with Advanced Security](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) APIs to create firewall rules that apply to their WSD applications.</span></span> <span data-ttu-id="51e9d-128">具體來說， [**INetFwRules**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules)介面的 [**add**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add)方法可以用來加入新的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="51e9d-128">Specifically, the [**Add**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add) method of the [**INetFwRules**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules) interface can be used to add a new firewall rule.</span></span> <span data-ttu-id="51e9d-129">如果未正確建立防火牆規則，用戶端和主機可能無法在網路上看到彼此。</span><span class="sxs-lookup"><span data-stu-id="51e9d-129">If firewall rules are created incorrectly, clients and hosts may not be able to see each other on the network.</span></span>

<span data-ttu-id="51e9d-130">**檢查應用程式特定的防火牆規則**</span><span class="sxs-lookup"><span data-stu-id="51e9d-130">**To check for application-specific firewall rules**</span></span>

1.  <span data-ttu-id="51e9d-131">按一下 [ **開始**]，按一下 [ **執行**]，然後輸入 **wf**。</span><span class="sxs-lookup"><span data-stu-id="51e9d-131">Click **Start**, click **Run**, and then type **wf.msc**.</span></span>
2.  <span data-ttu-id="51e9d-132">尋找可能會封鎖流量的應用程式特定規則。</span><span class="sxs-lookup"><span data-stu-id="51e9d-132">Look for application-specific rules that may be blocking traffic.</span></span> <span data-ttu-id="51e9d-133">如需詳細資訊，請參閱 [具有 Advanced Security 的 Windows 防火牆-診斷和疑難排解工具](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink)。</span><span class="sxs-lookup"><span data-stu-id="51e9d-133">For more information, see [Windows Firewall with Advanced Security - Diagnostics and Troubleshooting Tools](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink).</span></span>
3.  <span data-ttu-id="51e9d-134">移除應用程式特定的規則。</span><span class="sxs-lookup"><span data-stu-id="51e9d-134">Remove application-specific rules.</span></span>

<span data-ttu-id="51e9d-135">如果找不到特定應用程式的規則，請移至下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="51e9d-135">If no application-specific rules were found, move on to the next step.</span></span> <span data-ttu-id="51e9d-136">如果已找到並移除應用程式專屬的規則，請在進行防火牆變更之後，重新測試程式。</span><span class="sxs-lookup"><span data-stu-id="51e9d-136">If an application-specific rule was found and removed, retest the program after making the firewall change.</span></span> <span data-ttu-id="51e9d-137">如果程式現在可順利運作，就會識別出問題的原因，而不需要進行進一步的疑難排解步驟。</span><span class="sxs-lookup"><span data-stu-id="51e9d-137">If the program now works successfully, the cause of the problem has been identified and no further troubleshooting steps are necessary.</span></span> <span data-ttu-id="51e9d-138">否則，請移至下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="51e9d-138">Otherwise, move on to the next step.</span></span>

## <a name="enabling-the-ports-used-for-discovery-and-metadata-exchange"></a><span data-ttu-id="51e9d-139">啟用用於探索和中繼資料交換的埠</span><span class="sxs-lookup"><span data-stu-id="51e9d-139">Enabling the ports used for discovery and metadata exchange</span></span>

<span data-ttu-id="51e9d-140">WS-Discovery 使用 UDP 埠3702進行訊息交換。</span><span class="sxs-lookup"><span data-stu-id="51e9d-140">WS-Discovery uses the UDP port 3702 for message exchange.</span></span> <span data-ttu-id="51e9d-141">此外，TCP 通訊埠5357和5358有時也會用於中繼資料交換。</span><span class="sxs-lookup"><span data-stu-id="51e9d-141">In addition, TCP ports 5357 and 5358 are sometimes used for metadata exchange.</span></span> <span data-ttu-id="51e9d-142">您可以使用在 [Windows 防火牆中開啟埠](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx)所述的程式，在防火牆上明確開啟這些埠。</span><span class="sxs-lookup"><span data-stu-id="51e9d-142">These ports can be explicitly opened on the firewall using the procedures described in [Open a port in Windows Firewall](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx).</span></span>

<span data-ttu-id="51e9d-143">進行此防火牆變更之後，請重新測試程式。</span><span class="sxs-lookup"><span data-stu-id="51e9d-143">Retest the program after making this firewall change.</span></span> <span data-ttu-id="51e9d-144">如果程式現在可順利運作，就會識別出問題的原因，而不需要進行進一步的疑難排解步驟。</span><span class="sxs-lookup"><span data-stu-id="51e9d-144">If the program now works successfully, the cause of the problem has been identified and no further troubleshooting steps are necessary.</span></span> <span data-ttu-id="51e9d-145">否則，請移至下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="51e9d-145">Otherwise, move on to the next step.</span></span>

## <a name="disabling-the-firewall"></a><span data-ttu-id="51e9d-146">停用防火牆</span><span class="sxs-lookup"><span data-stu-id="51e9d-146">Disabling the firewall</span></span>

<span data-ttu-id="51e9d-147">您可以停用 Windows 防火牆，以協助針對疑似問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="51e9d-147">The Windows Firewall can be disabled to help troubleshoot suspected problems.</span></span> <span data-ttu-id="51e9d-148">其他適用的防火牆 (例如路由器上的防火牆) 也可基於疑難排解目的而停用。</span><span class="sxs-lookup"><span data-stu-id="51e9d-148">Other applicable firewalls (such as the firewall on a router) can also be disabled for troubleshooting purposes.</span></span> <span data-ttu-id="51e9d-149">如需啟用和停用 Windows 防火牆的相關資訊，請參閱 [開啟或關閉 Windows 防火牆](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx)。</span><span class="sxs-lookup"><span data-stu-id="51e9d-149">For information about enabling and disabling the Windows Firewall, see [Turn Windows Firewall on or off](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx).</span></span>

<span data-ttu-id="51e9d-150">停用任何適用的防火牆之後，請重新測試應用程式。</span><span class="sxs-lookup"><span data-stu-id="51e9d-150">Retest the application after disabling any applicable firewalls.</span></span> <span data-ttu-id="51e9d-151">如果程式現在可順利運作，則防火牆會封鎖流量。</span><span class="sxs-lookup"><span data-stu-id="51e9d-151">If the program now works successfully, then the firewall was blocking the traffic.</span></span> <span data-ttu-id="51e9d-152">封鎖流量有幾個可能的原因。</span><span class="sxs-lookup"><span data-stu-id="51e9d-152">There are a few possible causes of blocked traffic.</span></span>

-   <span data-ttu-id="51e9d-153">應用程式特定的例外狀況會封鎖流量。</span><span class="sxs-lookup"><span data-stu-id="51e9d-153">Application-specific exceptions blocked the traffic.</span></span> <span data-ttu-id="51e9d-154">檢查應用程式特定的防火牆規則，如上所述。</span><span class="sxs-lookup"><span data-stu-id="51e9d-154">Check for application-specific firewall rules as described above.</span></span>
-   <span data-ttu-id="51e9d-155">裝置花太多時間回應 UDP 要求。</span><span class="sxs-lookup"><span data-stu-id="51e9d-155">The device took too long to respond to UDP requests.</span></span> <span data-ttu-id="51e9d-156">Windows 防火牆可能會在傳送初始要求之後，封鎖傳回超過4秒的 UDP 回應。</span><span class="sxs-lookup"><span data-stu-id="51e9d-156">The Windows Firewall may block UDP responses that return more than 4 seconds after the initial request was sent.</span></span> <span data-ttu-id="51e9d-157">遵循 [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md) 所提供的程式，查看問題是否發生在4秒以內回應的主機，以繼續進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="51e9d-157">Continue troubleshooting by following the procedures given in [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) to see if the problem reproduces with a host that responds in less than 4 seconds.</span></span>

<span data-ttu-id="51e9d-158">如果在停用防火牆之後，應用程式仍失敗，則防火牆不會導致應用程式失敗。</span><span class="sxs-lookup"><span data-stu-id="51e9d-158">If the application still fails after the firewall is disabled, then the firewall is not causing the application failure.</span></span> <span data-ttu-id="51e9d-159">重新啟用防火牆，並遵循 [使用一般主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)的程式，繼續進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="51e9d-159">Re-enable the firewalls and continue troubleshooting by following the procedures given in [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="51e9d-160">疑難排解完成後，應該一律重新啟用防火牆。</span><span class="sxs-lookup"><span data-stu-id="51e9d-160">Firewalls should always be re-enabled after troubleshooting has finished.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51e9d-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="51e9d-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51e9d-162">WSDAPI 診斷程式</span><span class="sxs-lookup"><span data-stu-id="51e9d-162">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="51e9d-163">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="51e9d-163">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 

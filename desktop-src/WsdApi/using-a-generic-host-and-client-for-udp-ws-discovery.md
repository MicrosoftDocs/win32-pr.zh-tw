---
description: 如果用戶端和主機無法在網路上看到彼此，則泛型主機和用戶端可以替代自訂主機和用戶端，以協助對問題進行疑難排解。
ms.assetid: e82ce911-b2a7-4a57-a2f0-9aca6b74478f
title: 使用泛型主機和用戶端進行 UDP WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3289f5205e4e417fe8162b401be6c608432cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191722"
---
# <a name="using-a-generic-host-and-client-for-udp-ws-discovery"></a><span data-ttu-id="7ab79-103">使用泛型主機和用戶端進行 UDP WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="7ab79-103">Using a Generic Host and Client for UDP WS-Discovery</span></span>

<span data-ttu-id="7ab79-104">如果用戶端和主機無法在網路上看到彼此，則泛型主機和用戶端可以替代自訂主機和用戶端，以協助對問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="7ab79-104">If the client and host cannot see each other on the network, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="7ab79-105">如果裝置位址未出現在 WSD Debug 用戶端輸出中，則網路環境可能會造成失敗。</span><span class="sxs-lookup"><span data-stu-id="7ab79-105">If the device address does not appear in the WSD Debug Client output, then the network environment is probably causing the failure.</span></span> <span data-ttu-id="7ab79-106">如需泛型主機和用戶端的詳細資訊，請參閱 [調試](debugging-tools.md)程式。</span><span class="sxs-lookup"><span data-stu-id="7ab79-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="7ab79-107">如果主機或用戶端是在電腦上執行的應用程式，則泛型主機或用戶端應該在與實際主機或用戶端相同的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="7ab79-107">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="7ab79-108">例如，如果實際的主機或用戶端以系統管理員身分執行，則泛型主機或用戶端必須以系統管理員身分執行。</span><span class="sxs-lookup"><span data-stu-id="7ab79-108">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="7ab79-109">此外，如果主機或用戶端是獨立裝置，則應該由執行泛型主機或用戶端的電腦完全取代。</span><span class="sxs-lookup"><span data-stu-id="7ab79-109">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client.</span></span>

<span data-ttu-id="7ab79-110">**使用泛型主機和用戶端對 UDP WS-MANAGEMENT 進行疑難排解**</span><span class="sxs-lookup"><span data-stu-id="7ab79-110">**To using a generic host and client to troubleshoot UDP WS-Discovery**</span></span>

1.  <span data-ttu-id="7ab79-111">開啟 [命令提示字元] 視窗。</span><span class="sxs-lookup"><span data-stu-id="7ab79-111">Open a command prompt window.</span></span>
2.  <span data-ttu-id="7ab79-112">執行下列命令： **WSDDebug \_host.exe/mode 中繼資料/start**</span><span class="sxs-lookup"><span data-stu-id="7ab79-112">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="7ab79-113">可能會出現 **Windows 安全性警示** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7ab79-113">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="7ab79-114">如果是的話，請按一下 [ **解除封鎖** ]，以允許 WSD Debug 主機執行。</span><span class="sxs-lookup"><span data-stu-id="7ab79-114">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="7ab79-115">此命令會產生類似下列的輸出。</span><span class="sxs-lookup"><span data-stu-id="7ab79-115">This command generates output similar to the following.</span></span> <span data-ttu-id="7ab79-116">記下裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ab79-116">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="7ab79-117">執行下列命令： **WSDDebug \_client.exe/mode metadata/hello off/resolve** *<id>* 。</span><span class="sxs-lookup"><span data-stu-id="7ab79-117">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="7ab79-118">取代 *<id>* 為在步驟2中識別的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ab79-118">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="7ab79-119">可能會出現 **Windows 安全性警示** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7ab79-119">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="7ab79-120">如果是，請按一下 [ **解除封鎖** ]，以允許 WSD Debug 用戶端執行。</span><span class="sxs-lookup"><span data-stu-id="7ab79-120">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="7ab79-121">WSD Debug 用戶端會產生類似下列的輸出。</span><span class="sxs-lookup"><span data-stu-id="7ab79-121">WSD Debug Client generates output similar to the following.</span></span>

``` syntax
WSDAPI Debug Client
Copyright (C) Microsoft Corporation 2007.  All rights reserved.
Client ID is urn:uuid:0f571af7-6b0e-4daf-8054-f2233ac27910
Hello mode is disabled
Client metadata>
*****************************************************************************
Add at 02/28/07 15:16:51
+ EPR:
  + Address:                 urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Types:
    (wsdp) https://schemas.xmlsoap.org/ws/2006/02/devprof:Device
+ XAddrs:
  https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
+ Metadata version:          2
+ Instance ID:               1
+ Probe/Resolve tag:         WSDAPI debug_client
+ Remote transport address:  [::1]:3702
+ Local transport address:   ::1
+ Local interface GUID:      42133cd4-6a70-11db-bbc9-806e6f6e6963
Client metadata>
```

<span data-ttu-id="7ab79-122">WSD Debug 用戶端可能會在具有許多 DPWS 裝置的網路上產生大量的輸出。</span><span class="sxs-lookup"><span data-stu-id="7ab79-122">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="7ab79-123">輸出可以重新導向至檔案，以方便分析。</span><span class="sxs-lookup"><span data-stu-id="7ab79-123">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="7ab79-124">在 WSD Debug Client 提示字元中輸入 **log t** *<filename>* ，以將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="7ab79-124">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="7ab79-125">在 WSD Debug 用戶端提示字元中輸入 **log t stop** ，即可停止輸出重新導向。</span><span class="sxs-lookup"><span data-stu-id="7ab79-125">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="7ab79-126">請記下 (EPR) 位址的端點參考。</span><span class="sxs-lookup"><span data-stu-id="7ab79-126">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="7ab79-127">此 EPR 位址應符合上述步驟2中識別的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ab79-127">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="7ab79-128">如果是這種情況，則應用程式失敗可能與作業系統或網路環境無關。</span><span class="sxs-lookup"><span data-stu-id="7ab79-128">If this is the case, then the application failure is likely not related to the operating system or the network environment.</span></span> <span data-ttu-id="7ab79-129">以自訂主機和用戶端取代一般主機和用戶端，並遵循 [使用 WSD Debug 用戶端驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)的程式，繼續進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="7ab79-129">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WSD Debug Client to Verify Multicast Traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>

<span data-ttu-id="7ab79-130">如果裝置識別碼與 EPR 位址不符，則應用程式失敗可能與作業系統或網路環境有關。</span><span class="sxs-lookup"><span data-stu-id="7ab79-130">If the device ID does not match the EPR address, then the application failure is probably related to the operating system or the network environment.</span></span> <span data-ttu-id="7ab79-131">失敗可能有一或多個下列原因：</span><span class="sxs-lookup"><span data-stu-id="7ab79-131">The failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="7ab79-132">應用程式正在錯誤的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="7ab79-132">The application is running in the wrong security context.</span></span> <span data-ttu-id="7ab79-133">請確認應用程式使用正確的認證，而且用戶端和主機具有足夠的許可權可存取網路。</span><span class="sxs-lookup"><span data-stu-id="7ab79-133">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="7ab79-134">防火牆設定錯誤。</span><span class="sxs-lookup"><span data-stu-id="7ab79-134">The firewall configuration is wrong.</span></span> <span data-ttu-id="7ab79-135">遵循 [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md) 中的指示，確認 Windows 防火牆設定正確無誤，而且沒有任何其他規則捨棄封包。</span><span class="sxs-lookup"><span data-stu-id="7ab79-135">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="7ab79-136">您也可以將用戶端和主機複製到「初始化」電腦， (一個預設作業系統安裝尚未加入網域) 的電腦，以便嘗試重現失敗。</span><span class="sxs-lookup"><span data-stu-id="7ab79-136">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="7ab79-137">IPSec 原則封鎖了應用程式。</span><span class="sxs-lookup"><span data-stu-id="7ab79-137">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="7ab79-138">將用戶端和主機複製到不受 IPSec 原則影響的電腦上，然後嘗試重現失敗。</span><span class="sxs-lookup"><span data-stu-id="7ab79-138">Copy the client and host onto a machine not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ab79-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="7ab79-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ab79-140">WSDAPI 診斷程式</span><span class="sxs-lookup"><span data-stu-id="7ab79-140">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="7ab79-141">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="7ab79-141">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




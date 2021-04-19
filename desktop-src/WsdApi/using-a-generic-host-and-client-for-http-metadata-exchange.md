---
description: 如果用戶端和主機無法交換中繼資料，則可以將泛型主機和用戶端替換為自訂主機和用戶端，以協助對問題進行疑難排解。
ms.assetid: 7e5c8444-b3ee-4e9c-984f-13d54f2bbfc0
title: 使用泛型主機和用戶端進行 HTTP 中繼資料交換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36827dde8aa03fa15fc4beaa5917f1f2c3c36eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977795"
---
# <a name="using-a-generic-host-and-client-for-http-metadata-exchange"></a><span data-ttu-id="e8836-103">使用泛型主機和用戶端進行 HTTP 中繼資料交換</span><span class="sxs-lookup"><span data-stu-id="e8836-103">Using a Generic Host and Client for HTTP Metadata Exchange</span></span>

<span data-ttu-id="e8836-104">如果用戶端和主機無法交換中繼資料，則可以將泛型主機和用戶端替換為自訂主機和用戶端，以協助對問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="e8836-104">If the client and host cannot exchange metadata, then a generic host and client can be substituted for the custom host and client to help troubleshoot the issue.</span></span> <span data-ttu-id="e8836-105">如果裝置位址或裝置中繼資料未出現在 WSD Debug 用戶端輸出中，則提供的傳輸位址或網路環境可能會造成失敗。</span><span class="sxs-lookup"><span data-stu-id="e8836-105">If the device address or device metadata does not appear in the WSD Debug Client output, then the supplied transport addresses or the network environment may be causing the failure.</span></span> <span data-ttu-id="e8836-106">如需泛型主機和用戶端的詳細資訊，請參閱 [調試](debugging-tools.md)程式。</span><span class="sxs-lookup"><span data-stu-id="e8836-106">For more information about the generic host and client, see [Debugging Tools](debugging-tools.md).</span></span>

<span data-ttu-id="e8836-107">如果已驗證泛型主機和用戶端可以同時完成 WS-Discovery 和 HTTP 中繼資料交換，則可以跳過此診斷程式，並遵循 [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)的程式，繼續進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="e8836-107">If it has been verified that a generic host and client can complete both WS-Discovery and HTTP metadata exchange, then this diagnostic procedure can be skipped and troubleshooting can be continued by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="e8836-108">如果主機或用戶端是在電腦上執行的應用程式，則泛型主機或用戶端應該在與實際主機或用戶端相同的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="e8836-108">If either the host or client is an application running on a PC, the generic host or client should be run in the same security context as the actual host or client.</span></span> <span data-ttu-id="e8836-109">例如，如果實際的主機或用戶端以系統管理員身分執行，則泛型主機或用戶端必須以系統管理員身分執行。</span><span class="sxs-lookup"><span data-stu-id="e8836-109">For example, if the actual host or client runs as Administrator, then the generic host or client must run as Administrator.</span></span> <span data-ttu-id="e8836-110">此外，如果主機或用戶端是獨立裝置，則應該由執行泛型主機或用戶端的電腦完全取代為可保證無限制網路存取的安全性內容 (例如，以系統管理員身分執行) 。</span><span class="sxs-lookup"><span data-stu-id="e8836-110">Also, if either the host or client is a standalone device, it should be completely replaced by a PC running a generic host or client in a security context that guarantees unlimited network access (for example, running as Administrator).</span></span>

<span data-ttu-id="e8836-111">**使用泛型主機和用戶端對 HTTP 中繼資料交換進行疑難排解**</span><span class="sxs-lookup"><span data-stu-id="e8836-111">**To using a generic host and client to troubleshoot HTTP metadata exchange**</span></span>

1.  <span data-ttu-id="e8836-112">開啟 [命令提示字元] 視窗。</span><span class="sxs-lookup"><span data-stu-id="e8836-112">Open a command prompt window.</span></span>
2.  <span data-ttu-id="e8836-113">執行下列命令： **WSDDebug \_host.exe/mode 中繼資料/start**</span><span class="sxs-lookup"><span data-stu-id="e8836-113">Run the following command: **WSDDebug\_host.exe /mode metadata /start**</span></span>

    > [!Note]  
    > <span data-ttu-id="e8836-114">可能會出現 **Windows 安全性警示** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e8836-114">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="e8836-115">如果是的話，請按一下 [ **解除封鎖** ]，以允許 WSD Debug 主機執行。</span><span class="sxs-lookup"><span data-stu-id="e8836-115">If so, click **Unblock** to allow the WSD Debug Host to run.</span></span>

     

    <span data-ttu-id="e8836-116">此命令會產生類似下列的輸出。</span><span class="sxs-lookup"><span data-stu-id="e8836-116">This command generates output similar to the following.</span></span> <span data-ttu-id="e8836-117">記下裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8836-117">Make a note of the device ID.</span></span>

    ``` syntax
    WSDAPI Debug Host
    Copyright (C) Microsoft Corporation 2007.  All rights reserved.
    Device ID is urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    Host metadata>
    ```

3.  <span data-ttu-id="e8836-118">執行下列命令： **WSDDebug \_client.exe/mode metadata/hello off/resolve** *<id>* 。</span><span class="sxs-lookup"><span data-stu-id="e8836-118">Run the following command: **WSDDebug\_client.exe /mode metadata /hello off /resolve** *<id>*.</span></span> <span data-ttu-id="e8836-119">取代 *<id>* 為在步驟2中識別的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8836-119">Replace *<id>* with the device ID identified in step 2.</span></span>
    > [!Note]  
    > <span data-ttu-id="e8836-120">可能會出現 **Windows 安全性警示** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e8836-120">A **Windows Security Alert** dialog box may appear.</span></span> <span data-ttu-id="e8836-121">如果是，請按一下 [ **解除封鎖** ]，以允許 WSD Debug 用戶端執行。</span><span class="sxs-lookup"><span data-stu-id="e8836-121">If so, click **Unblock** to allow the WSD Debug Client to run.</span></span>

     

<span data-ttu-id="e8836-122">WSD Debug 用戶端會產生類似下列的輸出。</span><span class="sxs-lookup"><span data-stu-id="e8836-122">WSD Debug Client generates output similar to the following.</span></span>

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
*****************************************************************************
Getting metadata for host at 02/28/07 15:16:51:
+ Endpoint reference:
  + Address:
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
Client metadata>
*****************************************************************************
Metadata for host:
+ Endpoint reference:
  + Address:           urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice
  + Friendly name:
    [no lang]: Debugging Host
  + Firmware version:  1.0
  + Serial number:     00000000
Metadata section:
  + Dialect:
    https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel
  + Manufacturer:
    [no lang]: Microsoft Corporation
  + Manufacturer URL:  https://www.microsoft.com/
  + Model names:
    [no lang]: Microsoft Debugging Host
  + Model number:      https://www.microsoft.com/
End of metadata
Client metadata>
```

<span data-ttu-id="e8836-123">WSD Debug 用戶端可能會在具有許多 DPWS 裝置的網路上產生大量的輸出。</span><span class="sxs-lookup"><span data-stu-id="e8836-123">The WSD Debug Client may generate a lot of output on a network with many DPWS devices.</span></span> <span data-ttu-id="e8836-124">輸出可以重新導向至檔案，以方便分析。</span><span class="sxs-lookup"><span data-stu-id="e8836-124">The output can be redirected to a file for easier analysis.</span></span> <span data-ttu-id="e8836-125">在 WSD Debug Client 提示字元中輸入 **log t** *<filename>* ，以將輸出重新導向至檔案。</span><span class="sxs-lookup"><span data-stu-id="e8836-125">Type **log tee** *<filename>* at the WSD Debug Client prompt to redirect output to a file.</span></span> <span data-ttu-id="e8836-126">在 WSD Debug 用戶端提示字元中輸入 **log t stop** ，即可停止輸出重新導向。</span><span class="sxs-lookup"><span data-stu-id="e8836-126">Output redirection can be stopped by typing **log tee stop** at the WSD Debug Client prompt.</span></span>

<span data-ttu-id="e8836-127">請記下 (EPR) 位址的端點參考。</span><span class="sxs-lookup"><span data-stu-id="e8836-127">Make a note of the endpoint reference (EPR) address.</span></span> <span data-ttu-id="e8836-128">此 EPR 位址應符合上述步驟2中識別的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8836-128">This EPR address should match the device ID identified in step 2 above.</span></span> <span data-ttu-id="e8836-129">此外，請確認 WSD 偵錯工具用戶端已完全列印裝置的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e8836-129">Also, verify that the WSD Debug Client completely printed the metadata for the device.</span></span> <span data-ttu-id="e8836-130">裝置中繼資料的開頭 `Metadata for host` 和結尾是 `End of metadata` 。</span><span class="sxs-lookup"><span data-stu-id="e8836-130">The device metadata begins with `Metadata for host` and ends with `End of metadata`.</span></span>

<span data-ttu-id="e8836-131">如果裝置識別碼和裝置中繼資料正確地出現在 WSD Debug 用戶端輸出中，則應用程式失敗可能與提供的傳輸位址、作業系統或網路環境無關。</span><span class="sxs-lookup"><span data-stu-id="e8836-131">If the device ID and device metadata appears correctly in the WSD Debug Client output, then the application failure is likely not related to the supplied transport addresses, the operating system, or the network environment.</span></span> <span data-ttu-id="e8836-132">使用自訂主機和用戶端來取代一般主機和用戶端，並遵循 [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)的程式，繼續進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="e8836-132">Replace the generic host and client with the custom host and client, and continue troubleshooting by following the procedures in [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

<span data-ttu-id="e8836-133">如果裝置位址和裝置中繼資料未出現在 WSD Debug 用戶端輸出中，則失敗可能會有下列一或多個原因：</span><span class="sxs-lookup"><span data-stu-id="e8836-133">If the device address and device metadata do not appear in the WSD Debug Client output, then the failure could have one or more of the following causes:</span></span>

-   <span data-ttu-id="e8836-134">主機所公告的傳輸位址不正確或格式不正確。</span><span class="sxs-lookup"><span data-stu-id="e8836-134">The transport address advertised by the host is incorrect or malformed.</span></span> <span data-ttu-id="e8836-135">WSD Debug 用戶端會嘗試從 [ProbeMatches](probematches-message.md)或 [ResolveMatches](resolvematches-message.md)訊息的 **XADDRS** 元素所提供的 URL 取得裝置中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e8836-135">WSD Debug Client attempts to get device metadata from the URL provided in the **XAddrs** element of a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message.</span></span> <span data-ttu-id="e8836-136">用於中繼資料交換的 URL 會出現在 WSD Debug 用戶端輸出中，並在前面加上片語 `Using xAddr` 。</span><span class="sxs-lookup"><span data-stu-id="e8836-136">The URL used for metadata exchange appears in the WSD Debug Client output, prefixed by the phrase `Using xAddr`.</span></span> <span data-ttu-id="e8836-137">下列範例顯示在上述 WSD Debug 用戶端輸出中用於中繼資料交換的 XAddrs。</span><span class="sxs-lookup"><span data-stu-id="e8836-137">The following example shows the XAddrs used for metadata exchange in the above WSD Debug Client output.</span></span>

    ``` syntax
    Using xAddr: https://[::1]:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
    ```

    <span data-ttu-id="e8836-138">如果提供的 XAddrs 不符合 [XAddr 驗證規則](xaddr-validation-rules.md)，則 WSD Debug 用戶端無法取得裝置的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e8836-138">If the supplied XAddrs do not conform to the [XAddr validation rules](xaddr-validation-rules.md), then the WSD Debug Client cannot get the device's metadata.</span></span>

-   <span data-ttu-id="e8836-139">應用程式正在錯誤的安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="e8836-139">The application is running in the wrong security context.</span></span> <span data-ttu-id="e8836-140">請確認應用程式使用正確的認證，而且用戶端和主機具有足夠的許可權可存取網路。</span><span class="sxs-lookup"><span data-stu-id="e8836-140">Verify that the application is using the correct credentials and that the client and host have sufficient permission to access the network.</span></span>
-   <span data-ttu-id="e8836-141">防火牆設定錯誤。</span><span class="sxs-lookup"><span data-stu-id="e8836-141">The firewall configuration is wrong.</span></span> <span data-ttu-id="e8836-142">遵循 [檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md) 中的指示，確認 Windows 防火牆設定正確無誤，而且沒有任何其他規則捨棄封包。</span><span class="sxs-lookup"><span data-stu-id="e8836-142">Follow the instructions in [Inspecting Adapter and Firewall Settings](inspecting-adapter-and-firewall-settings.md) to verify that the Windows Firewall settings are correct and that there are no other rules dropping the packets.</span></span> <span data-ttu-id="e8836-143">您也可以將用戶端和主機複製到「初始化」電腦， (一個預設作業系統安裝尚未加入網域) 的電腦，以便嘗試重現失敗。</span><span class="sxs-lookup"><span data-stu-id="e8836-143">The client and host can also be copied onto a "pristine" machine (one with a default operating system installation that has never been joined to a domain) in order to attempt to reproduce the failure.</span></span>
-   <span data-ttu-id="e8836-144">IPSec 原則封鎖了應用程式。</span><span class="sxs-lookup"><span data-stu-id="e8836-144">An IPSec policy is blocking the application.</span></span> <span data-ttu-id="e8836-145">將用戶端和主機複製到不受 IPSec 原則影響的電腦，然後嘗試重現失敗。</span><span class="sxs-lookup"><span data-stu-id="e8836-145">Copy the client and host onto a machine that is not subject to IPSec policies and try to reproduce the failure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8836-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8836-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8836-147">WSDAPI 診斷程式</span><span class="sxs-lookup"><span data-stu-id="e8836-147">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="e8836-148">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="e8836-148">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 




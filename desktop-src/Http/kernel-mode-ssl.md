---
title: 核心模式 SSL
description: 核心模式 SSL
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- 核心模式 SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737ac7c6c25bac6e7b66d91aa967fc6fa550459b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106991090"
---
# <a name="kernel-mode-ssl"></a><span data-ttu-id="73fff-104">核心模式 SSL</span><span class="sxs-lookup"><span data-stu-id="73fff-104">Kernel Mode SSL</span></span>

<span data-ttu-id="73fff-105">核心模式 SSL 是在 Windows Server 2003 Service Pack 1 中引進， (SP1) 支援有限。</span><span class="sxs-lookup"><span data-stu-id="73fff-105">Kernel mode SSL was introduced in Windows Server 2003 with Service Pack 1 (SP1) with limited support.</span></span> <span data-ttu-id="73fff-106">針對在 Windows Server 2003 SP1 上執行的電腦，必須將登錄機碼設定為啟用核心 SSL。</span><span class="sxs-lookup"><span data-stu-id="73fff-106">For computers running on Windows Server 2003 with SP1 a registry key must be set to enable kernel SSL.</span></span> <span data-ttu-id="73fff-107">針對在 Windows Server 2008 和 Windows Vista 上執行的電腦，會提供 SSL 的完整核心模式支援。</span><span class="sxs-lookup"><span data-stu-id="73fff-107">For computers running on Windows Server 2008 and Windows Vista, full kernel mode support for SSL is provided.</span></span>

<span data-ttu-id="73fff-108">下列各節說明核心模式的 SSL 支援：</span><span class="sxs-lookup"><span data-stu-id="73fff-108">The following sections describe kernel mode SSL support:</span></span>

-   <span data-ttu-id="73fff-109">Windows Server 2003 （含 SP1）中的核心模式 SSL</span><span class="sxs-lookup"><span data-stu-id="73fff-109">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>
-   <span data-ttu-id="73fff-110">Windows Server 2008 和 Windows Vista 中的核心模式 SSL</span><span class="sxs-lookup"><span data-stu-id="73fff-110">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a><span data-ttu-id="73fff-111">Windows Server 2003 （含 SP1）中的核心模式 SSL</span><span class="sxs-lookup"><span data-stu-id="73fff-111">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>

<span data-ttu-id="73fff-112">在 Windows Server 2003 （含 SP1）中，HTTP 伺服器 API 提供在核心模式中執行 SSL 安全性的選項 (使用者模式 SSL 是預設) 。</span><span class="sxs-lookup"><span data-stu-id="73fff-112">In Windows Server 2003 with SP1, HTTP Server API provides the option of running SSL security in kernel mode (user mode SSL is the default).</span></span> <span data-ttu-id="73fff-113">核心模式功能藉由將加密和解密作業移至核心來改善 SSL 效能，進而減少核心模式和使用者模式之間的轉換數目。</span><span class="sxs-lookup"><span data-stu-id="73fff-113">The kernel mode feature improves SSL performance by moving encryption and decryption operations to the kernel, thus reducing the number of transitions between kernel mode and user mode.</span></span>

<span data-ttu-id="73fff-114">當 SSL 以核心模式執行時，不支援下列功能：</span><span class="sxs-lookup"><span data-stu-id="73fff-114">The following features are not supported when SSL is run in kernel mode:</span></span>

-   <span data-ttu-id="73fff-115">Client certificates</span><span class="sxs-lookup"><span data-stu-id="73fff-115">Client certificates</span></span>
-   <span data-ttu-id="73fff-116">RC2 密碼</span><span class="sxs-lookup"><span data-stu-id="73fff-116">RC2 ciphers</span></span>
-   <span data-ttu-id="73fff-117">PCT 1.0 通訊協定</span><span class="sxs-lookup"><span data-stu-id="73fff-117">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="73fff-118">伺服器憑證設定變更需要重新開機 HTTP 服務</span><span class="sxs-lookup"><span data-stu-id="73fff-118">Server certificate configuration changes require a restart of the HTTP service</span></span>
-   <span data-ttu-id="73fff-119">大量加密和卸載支援</span><span class="sxs-lookup"><span data-stu-id="73fff-119">Bulk encryption and offload support</span></span>

## <a name="configuring-kernel-mode-ssl"></a><span data-ttu-id="73fff-120">設定核心模式 SSL</span><span class="sxs-lookup"><span data-stu-id="73fff-120">Configuring Kernel Mode SSL</span></span>

<span data-ttu-id="73fff-121">核心模式 SSL 是由 **EnableKernelSSL** 登錄值所控制，並藉由將值設定為1來啟用。</span><span class="sxs-lookup"><span data-stu-id="73fff-121">Kernel mode SSL is controlled by the **EnableKernelSSL** registry value and is enabled by setting the value to 1.</span></span> <span data-ttu-id="73fff-122">啟用核心模式 SSL 將會停用使用者模式 SSL，且需要重新開機 HTTP 服務才會生效。</span><span class="sxs-lookup"><span data-stu-id="73fff-122">Enabling kernel mode SSL will disable user mode SSL and requires the HTTP service to be restarted to take effect.</span></span> <span data-ttu-id="73fff-123">**EnableKernelSSL** 登錄機碼位於：</span><span class="sxs-lookup"><span data-stu-id="73fff-123">The **EnableKernelSSL** registry key is located at:</span></span>

<span data-ttu-id="73fff-124">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **服務** \\ **HTTP** \\ **參數** \\ **EnableKernelSSL**</span><span class="sxs-lookup"><span data-stu-id="73fff-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**HTTP**\\**Parameters**\\**EnableKernelSSL**</span></span>

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a><span data-ttu-id="73fff-125">Windows Server 2008 和 Windows Vista 中的核心模式 SSL</span><span class="sxs-lookup"><span data-stu-id="73fff-125">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

<span data-ttu-id="73fff-126">針對在 Windows Server 2008 和 Windows Vista 上執行的電腦，HTTP 伺服器 API 具備增強的 SSL 功能。</span><span class="sxs-lookup"><span data-stu-id="73fff-126">For computers running on Windows Server 2008 and Windows Vista, the HTTP Server API features enhanced SSL functionality.</span></span>

<span data-ttu-id="73fff-127">以下是支援的新功能：</span><span class="sxs-lookup"><span data-stu-id="73fff-127">The following new features are supported:</span></span>

-   <span data-ttu-id="73fff-128">核心模式 SSL 中的完整用戶端憑證支援</span><span class="sxs-lookup"><span data-stu-id="73fff-128">Full client certificate support in kernel mode SSL</span></span>
-   <span data-ttu-id="73fff-129">所有 HTTP SSL 交易的核心模式 SSL</span><span class="sxs-lookup"><span data-stu-id="73fff-129">Kernel mode SSL for all HTTP SSL transactions</span></span>
-   <span data-ttu-id="73fff-130">大量加密和卸載支援</span><span class="sxs-lookup"><span data-stu-id="73fff-130">Bulk encryption and offload support</span></span>
-   <span data-ttu-id="73fff-131">PCT 1.0 通訊協定</span><span class="sxs-lookup"><span data-stu-id="73fff-131">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="73fff-132">RC2 密碼</span><span class="sxs-lookup"><span data-stu-id="73fff-132">RC2 ciphers</span></span>
-   <span data-ttu-id="73fff-133">提高使用者模式 SSL 的效能</span><span class="sxs-lookup"><span data-stu-id="73fff-133">Increased performance over user mode SSL</span></span>

## <a name="configuration"></a><span data-ttu-id="73fff-134">組態</span><span class="sxs-lookup"><span data-stu-id="73fff-134">Configuration</span></span>

<span data-ttu-id="73fff-135">核心模式 SSL 可透過下列兩個登錄值設定：位於下列位置的 HTTP 參數機碼：</span><span class="sxs-lookup"><span data-stu-id="73fff-135">Kernel mode SSL is configurable through two registry values under the HTTP Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

<span data-ttu-id="73fff-136">使用者必須擁有系統管理員/本機系統許可權，才能修改登錄值，以及查看或修改記錄檔以及包含它們的資料夾。</span><span class="sxs-lookup"><span data-stu-id="73fff-136">A user must have Administrator/Local System privileges to modify the registry values and view, or modify, the log files and the folder that contains them.</span></span>

<span data-ttu-id="73fff-137">啟動 HTTP 伺服器 API 驅動程式時，會讀取登錄值中的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="73fff-137">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="73fff-138">如此一來，如果設定已變更，則必須停止並重新啟動驅動程式，才能讀取新的值。</span><span class="sxs-lookup"><span data-stu-id="73fff-138">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="73fff-139">您可以使用下列主控台命令來完成這項作業：</span><span class="sxs-lookup"><span data-stu-id="73fff-139">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="73fff-140">**net stop HTTP**</span><span class="sxs-lookup"><span data-stu-id="73fff-140">**net stop http**</span></span>

<span data-ttu-id="73fff-141">**net start HTTP**</span><span class="sxs-lookup"><span data-stu-id="73fff-141">**net start http**</span></span>

<span data-ttu-id="73fff-142">下表列出登錄設定值。</span><span class="sxs-lookup"><span data-stu-id="73fff-142">The following table lists registry configuration values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73fff-143">登錄值</span><span class="sxs-lookup"><span data-stu-id="73fff-143">Registry Value</span></span></th>
<th><span data-ttu-id="73fff-144">Description</span><span class="sxs-lookup"><span data-stu-id="73fff-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73fff-145">EnableKernelSSL</span><span class="sxs-lookup"><span data-stu-id="73fff-145">EnableKernelSSL</span></span></td>
<td><span data-ttu-id="73fff-146"><strong>Windows Server 2008 和 Windows Vista：</strong> 此登錄值已過時。</span><span class="sxs-lookup"><span data-stu-id="73fff-146"><strong>Windows Server 2008 and Windows Vista:</strong> This registry value is obsolete.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73fff-147">EnableSslCloseNotify</span><span class="sxs-lookup"><span data-stu-id="73fff-147">EnableSslCloseNotify</span></span></td>
<td><span data-ttu-id="73fff-148">設定為<strong>TRUE</strong>以啟用關閉通知的<strong>DWORD</strong>值，否則為<strong>FALSE</strong>以停用關閉通知需求。</span><span class="sxs-lookup"><span data-stu-id="73fff-148">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable close-notify, or <strong>FALSE</strong> to disable the close-notify requirement.</span></span> <span data-ttu-id="73fff-149">關閉-通知預設為停用。</span><span class="sxs-lookup"><span data-stu-id="73fff-149">Close-notify is disabled by default.</span></span><br/> <span data-ttu-id="73fff-150">當啟用 [關閉-通知] 時，用戶端應用程式必須在關閉 TCP 連接之前傳送「關閉通知」訊息。</span><span class="sxs-lookup"><span data-stu-id="73fff-150">When close-notify is enabled, the client application is required to send a close-notify message before closing TCP connections.</span></span> <span data-ttu-id="73fff-151">HTTP 伺服器 API 也會在關閉連接之前傳送關閉通知。</span><span class="sxs-lookup"><span data-stu-id="73fff-151">The HTTP Server API also sends a close-notify before closing the connection.</span></span><br/> <span data-ttu-id="73fff-152">當啟用 [關閉] 通知時，當用戶端傳送「關閉通知」訊息時，HTTP 伺服器 API 會在未來連線到用戶端時重複使用 SSL 會話。</span><span class="sxs-lookup"><span data-stu-id="73fff-152">When close-notify is enabled, and the client sends a close-notify message, the HTTP Server API will reuse the SSL session on future connections to the client.</span></span> <span data-ttu-id="73fff-153">如果用戶端未傳送關閉通知，HTTP 伺服器 API 將不會在未來的連接上重複使用相同的 SSL 會話。</span><span class="sxs-lookup"><span data-stu-id="73fff-153">If the client does not send a close-notify, the HTTP Server API will not reuse the same SSL session on future connections.</span></span> <span data-ttu-id="73fff-154">因此，在新的連接上會觸發完整的 SSL 交握，因此會降低效能。</span><span class="sxs-lookup"><span data-stu-id="73fff-154">Thus, a full SSL handshake is triggered on the new connection thereby reducing performance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="73fff-155">啟用「關閉通知」有助於減輕對 HTTPS 要求和回應的截斷攻擊。</span><span class="sxs-lookup"><span data-stu-id="73fff-155">Enabling close-notify helps mitigate truncation attacks against the HTTPS requests and responses.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="73fff-156">停用 [關閉通知] 時，HTTP 伺服器 API 會重複使用 SSL 會話，以供未來連接使用。</span><span class="sxs-lookup"><span data-stu-id="73fff-156">When close-notify is disabled, the HTTP Server API reuses the SSL session for future connections.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73fff-157">DisableSslCertChainCacheOnlyUrlRetrieval</span><span class="sxs-lookup"><span data-stu-id="73fff-157">DisableSslCertChainCacheOnlyUrlRetrieval</span></span></td>
<td><span data-ttu-id="73fff-158">設定為<strong>TRUE</strong>的<strong>DWORD</strong>值，可讓 HTTP 伺服器 API 從網際網路或本機存放區取出中繼憑證，或使用<strong>FALSE</strong>從本機存放區取出中繼憑證。</span><span class="sxs-lookup"><span data-stu-id="73fff-158">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable the HTTP Server API to retrieve intermediate certificates from either the Internet, or the local store, or <strong>FALSE</strong> to retrieve intermediate certificates from the local store only.</span></span> <span data-ttu-id="73fff-159">預設的登錄值為 <strong>FALSE</strong>。</span><span class="sxs-lookup"><span data-stu-id="73fff-159">The default registry value is <strong>FALSE</strong>.</span></span><br/> <span data-ttu-id="73fff-160">根據預設，HTTP 伺服器 API 會在本機電腦帳戶下，從中繼憑證授權單位單位存放區中取出中繼憑證，以建立用戶端憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="73fff-160">By default, the HTTP Server API builds a client certificate chain by retrieving the intermediate certificates from the Intermediate Certificate Authority store under the local machine account.</span></span> <span data-ttu-id="73fff-161">將此值設定為 <strong>TRUE</strong> ，可讓 HTTP 伺服器 API 只從本機存放區取得中繼憑證，但也可從網際網路上的中繼憑證授權單位單位抓取。</span><span class="sxs-lookup"><span data-stu-id="73fff-161">Setting this value to <strong>TRUE</strong> enables the HTTP Server API to retrieve the intermediate certificates not only from the local store, but also from the Intermediate Certificate Authority on the Internet.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 






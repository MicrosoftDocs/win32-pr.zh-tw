---
description: 使用安全通訊端延伸模組的 Advanced Winsock 範例
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: 使用安全通訊端延伸模組的 Advanced Winsock 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6701809ad97c7d39acf1f0eae646e7555e5c967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943427"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a><span data-ttu-id="1e0e8-103">使用安全通訊端延伸模組的 Advanced Winsock 範例</span><span class="sxs-lookup"><span data-stu-id="1e0e8-103">Advanced Winsock Samples Using Secure Socket Extensions</span></span>

## <a name="secure-tcp-client-and-server-sample"></a><span data-ttu-id="1e0e8-104">保護 TCP 用戶端和伺服器範例</span><span class="sxs-lookup"><span data-stu-id="1e0e8-104">Secure TCP Client and Server Sample</span></span>

<span data-ttu-id="1e0e8-105">Microsoft Windows 軟體開發套件 (SDK) 包含更先進的 Winsock 範例，示範如何使用安全通訊端延伸模組。</span><span class="sxs-lookup"><span data-stu-id="1e0e8-105">A more advanced Winsock sample that demonstrates the use of secure socket extensions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1e0e8-106">此範例包含使用 Winsock 和安全通訊端擴充功能安全地連接的 TCP 用戶端和伺服器。</span><span class="sxs-lookup"><span data-stu-id="1e0e8-106">The sample includes a TCP client and server that connect securely using the Winsock and the secure socket extensions.</span></span>

<span data-ttu-id="1e0e8-107">根據預設，Winsock 範例原始程式碼會安裝在下列目錄中：</span><span class="sxs-lookup"><span data-stu-id="1e0e8-107">By default, the Winsock sample source code is installed in the following directory:</span></span>

<span data-ttu-id="1e0e8-108">*C： \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ 範例 \\ NetDs \\ winsock*</span><span class="sxs-lookup"><span data-stu-id="1e0e8-108">*C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\NetDs\\winsock*</span></span>

<span data-ttu-id="1e0e8-109">範例位於下列資料夾底下：</span><span class="sxs-lookup"><span data-stu-id="1e0e8-109">A sample is located under the following folder:</span></span>

<span data-ttu-id="1e0e8-110">*securesocket*</span><span class="sxs-lookup"><span data-stu-id="1e0e8-110">*securesocket*</span></span>

<span data-ttu-id="1e0e8-111">範例程式碼會分割成不同的目錄，如下所述：</span><span class="sxs-lookup"><span data-stu-id="1e0e8-111">The sample code is split into separate directories as described below:</span></span>

-   <span data-ttu-id="1e0e8-112">stcpclient-包含安全 TCP 用戶端程式代碼的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1e0e8-112">stcpclient - the folder that contains the secure TCP client code.</span></span>
-   <span data-ttu-id="1e0e8-113">stcpcommon-包含安全 TCP 用戶端與伺服器之間共用之通用程式庫程式碼的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1e0e8-113">stcpcommon - the folder that contains common library code that is shared between the secure TCP client and server.</span></span>
-   <span data-ttu-id="1e0e8-114">stcpserver-包含安全 TCP 伺服器程式碼的資料夾。</span><span class="sxs-lookup"><span data-stu-id="1e0e8-114">stcpserver - the folder that contains the secure TCP server code.</span></span>

<span data-ttu-id="1e0e8-115">請注意，這些範例是要在執行 Windows Vista 或更新版本的兩部不同電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="1e0e8-115">It should be noted that the samples are meant to be run on two different computers running Windows Vista or later.</span></span> <span data-ttu-id="1e0e8-116">此外，您必須在兩部電腦上布建 IPsec 認證，才能讓連線成功，因為此範例使用 IPsec 保護其流量。</span><span class="sxs-lookup"><span data-stu-id="1e0e8-116">Additionally, IPsec credentials must be provisioned on both the computers for the connection to succeed, because the sample uses IPsec for securing its traffic.</span></span> <span data-ttu-id="1e0e8-117">如需有關設定 IPsec 認證的詳細資訊，請參閱 [IPsec](/windows/desktop/FWP/ipsec-configuration) 設定的相關檔。</span><span class="sxs-lookup"><span data-stu-id="1e0e8-117">Please refer to the documentation on [IPsec Configuration](/windows/desktop/FWP/ipsec-configuration) for more information on setting up IPsec credentials.</span></span>

<span data-ttu-id="1e0e8-118">建立範例將會產生兩個可執行檔：</span><span class="sxs-lookup"><span data-stu-id="1e0e8-118">Building the sample will generate two executable files:</span></span>

<span data-ttu-id="1e0e8-119">*stcpclient.exe* 和 *stcpserver.exe*。</span><span class="sxs-lookup"><span data-stu-id="1e0e8-119">*stcpclient.exe* and *stcpserver.exe*.</span></span>

<span data-ttu-id="1e0e8-120">將 *stcpclient.exe* 複製到電腦 A，然後將 *stcpserver.exe* 複製到電腦 B。在電腦 B 上，在命令提示字元中執行下列命令，以啟動 TCP 伺服器：</span><span class="sxs-lookup"><span data-stu-id="1e0e8-120">Copy *stcpclient.exe* to computer A and copy *stcpserver.exe* to computer B. On computer B, start the TCP server by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="1e0e8-121">**stcpserver.exe**</span><span class="sxs-lookup"><span data-stu-id="1e0e8-121">**stcpserver.exe**</span></span>

<span data-ttu-id="1e0e8-122">執行下列命令以取得伺服器的其他使用方式選項：</span><span class="sxs-lookup"><span data-stu-id="1e0e8-122">Execute the following command for more usage options for the server:</span></span>

<span data-ttu-id="1e0e8-123">**stcpserver.exe/？**</span><span class="sxs-lookup"><span data-stu-id="1e0e8-123">**stcpserver.exe /?**</span></span>

<span data-ttu-id="1e0e8-124">然後在電腦 A 上，在命令提示字元中執行下列命令，以啟動 TCP 用戶端：</span><span class="sxs-lookup"><span data-stu-id="1e0e8-124">Then on computer A, start the TCP client by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="1e0e8-125">**stcpclient.exe <的完整 DNS------------------->a**</span><span class="sxs-lookup"><span data-stu-id="1e0e8-125">**stcpclient.exe <fully-qualified-DNS-name-for-machine-B>**</span></span>

<span data-ttu-id="1e0e8-126">此時，應該會安全地建立連接。</span><span class="sxs-lookup"><span data-stu-id="1e0e8-126">At this point the connection should get established securely.</span></span>

<span data-ttu-id="1e0e8-127">執行下列命令以取得用戶端的更多使用方式選項：</span><span class="sxs-lookup"><span data-stu-id="1e0e8-127">Execute the following command for more usage options for the client:</span></span>

<span data-ttu-id="1e0e8-128">**stcpclient.exe/？**</span><span class="sxs-lookup"><span data-stu-id="1e0e8-128">**stcpclient.exe /?**</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e0e8-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e0e8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e0e8-130">關於 Windows 篩選平台</span><span class="sxs-lookup"><span data-stu-id="1e0e8-130">About Windows Filtering Platform</span></span>](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[<span data-ttu-id="1e0e8-131">應用層強制 (ALE) </span><span class="sxs-lookup"><span data-stu-id="1e0e8-131">Application Layer Enforcement (ALE)</span></span>](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[<span data-ttu-id="1e0e8-132">IPsec 設定</span><span class="sxs-lookup"><span data-stu-id="1e0e8-132">IPsec Configuration</span></span>](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[<span data-ttu-id="1e0e8-133">IPsec 功能</span><span class="sxs-lookup"><span data-stu-id="1e0e8-133">IPsec Functions</span></span>](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[<span data-ttu-id="1e0e8-134">使用安全通訊端擴充功能</span><span class="sxs-lookup"><span data-stu-id="1e0e8-134">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="1e0e8-135">安全性支援提供者介面 (SSPI)</span><span class="sxs-lookup"><span data-stu-id="1e0e8-135">Security Support Provider Interface (SSPI)</span></span>](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[<span data-ttu-id="1e0e8-136">Windows 篩選平台</span><span class="sxs-lookup"><span data-stu-id="1e0e8-136">Windows Filtering Platform</span></span>](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[<span data-ttu-id="1e0e8-137">Windows 篩選平台 API 函式</span><span class="sxs-lookup"><span data-stu-id="1e0e8-137">Windows Filtering Platform API Functions</span></span>](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[<span data-ttu-id="1e0e8-138">Winsock 安全通訊端擴充功能</span><span class="sxs-lookup"><span data-stu-id="1e0e8-138">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 

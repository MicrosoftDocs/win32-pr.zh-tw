---
title: 網路原則伺服器
description: 網路原則伺服器 (NPS) 是 Microsoft 對遠端驗證撥入使用者服務 (RADIUS) 伺服器和 proxy 的實施。
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315442"
---
# <a name="network-policy-server"></a><span data-ttu-id="45f74-103">網路原則伺服器</span><span class="sxs-lookup"><span data-stu-id="45f74-103">Network Policy Server</span></span>

## <a name="purpose"></a><span data-ttu-id="45f74-104">目的</span><span class="sxs-lookup"><span data-stu-id="45f74-104">Purpose</span></span>

<span data-ttu-id="45f74-105">網路原則伺服器 (NPS) 是 Microsoft 對遠端驗證撥入使用者服務 (RADIUS) 伺服器和 proxy 的實施。</span><span class="sxs-lookup"><span data-stu-id="45f74-105">Network Policy Server (NPS) is the Microsoft implementation of a Remote Authentication Dial-in User Service (RADIUS) server and proxy.</span></span> <span data-ttu-id="45f74-106">這是網際網路驗證服務 (IAS) 的後續版本。</span><span class="sxs-lookup"><span data-stu-id="45f74-106">It is the successor of Internet Authentication Service (IAS).</span></span>

<span data-ttu-id="45f74-107">NPS 作為 RADIUS 伺服器，可針對無線、驗證交換器，以及遠端存取撥號和虛擬私人網路 (VPN) 連接，執行驗證、授權和帳戶處理。</span><span class="sxs-lookup"><span data-stu-id="45f74-107">As a RADIUS server, NPS performs authentication, authorization, and accounting for wireless, authenticating switch, and remote access dial-up and virtual private network (VPN) connections.</span></span>

<span data-ttu-id="45f74-108">NPS 也是網路存取保護 (NAP) 的健康情況評估伺服器。</span><span class="sxs-lookup"><span data-stu-id="45f74-108">NPS is also a health evaluator server for Network Access Protection (NAP).</span></span> <span data-ttu-id="45f74-109">NPS 會執行網路連線嘗試的驗證與授權，並根據設定的系統健康狀態原則，評估電腦的健康狀態，並決定如何限制不符合規範的電腦網路存取或通訊。</span><span class="sxs-lookup"><span data-stu-id="45f74-109">NPS performs authentication and authorization of network connection attempts and, based on configured system health policies, evaluates computer health compliance and determines how to limit a noncompliant computer's network access or communication.</span></span> <span data-ttu-id="45f74-110">這是僅限 NPS 專用的新功能;IAS 不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="45f74-110">This is a new feature specific to NPS only; IAS does not support it.</span></span> <span data-ttu-id="45f74-111">如需 NPS 新功能的完整清單，請參閱 [網際網路驗證服務和網路原則伺服器](internet-authentication-service-vs-network-policy-server.md) 。</span><span class="sxs-lookup"><span data-stu-id="45f74-111">See [Internet Authentication Service and Network Policy Server](internet-authentication-service-vs-network-policy-server.md) for a complete list of features new to NPS.</span></span>

<span data-ttu-id="45f74-112">NPS 包含兩個 API 集合： NPS 擴充功能 API 和伺服器資料物件 (SDO) API。</span><span class="sxs-lookup"><span data-stu-id="45f74-112">NPS includes two API sets: NPS Extensions API and Server Data Objects (SDO) API.</span></span> <span data-ttu-id="45f74-113">Nps 擴充功能 API 和 SDO API 也都受到 NPS （網際網路驗證服務）的先驅支援。</span><span class="sxs-lookup"><span data-stu-id="45f74-113">Both NPS Extensions API and SDO API are also supported by the precursor of NPS, the Internet Authentication Service.</span></span>

<span data-ttu-id="45f74-114">NPS 擴充功能 API 可用於擴充 NPS 和先前由 IAS 提供的驗證、授權和帳戶處理方法。</span><span class="sxs-lookup"><span data-stu-id="45f74-114">NPS Extensions API can be used to extend the authentication, authorization, and accounting methods offered by NPS and previously by IAS.</span></span>

<span data-ttu-id="45f74-115">您可以使用伺服器資料物件 API，在執行 NPS 或 IAS 的電腦上操作網路原則設定。</span><span class="sxs-lookup"><span data-stu-id="45f74-115">Server Data Objects API can be used to manipulate the network policy configuration on a computer that runs NPS or IAS.</span></span>

> [!Note]  
> <span data-ttu-id="45f74-116">NPS 中的網路原則相當於 IAS 中的遠端存取原則。</span><span class="sxs-lookup"><span data-stu-id="45f74-116">Network policies in NPS are equivalent to remote access policies in IAS.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="45f74-117">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="45f74-117">Developer audience</span></span>

<span data-ttu-id="45f74-118">NPS 擴充功能 API 是專為使用 C/c + + 開發軟體的程式設計人員所設計。</span><span class="sxs-lookup"><span data-stu-id="45f74-118">The NPS Extensions API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="45f74-119">程式設計人員應該熟悉網路概念和 RADIUS 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="45f74-119">Programmers should be familiar with networking concepts and the RADIUS protocol.</span></span> <span data-ttu-id="45f74-120">RADIUS 記載于 [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) 和 [rfc 2866](https://www.ietf.org/rfc/rfc2866.txt)中。</span><span class="sxs-lookup"><span data-stu-id="45f74-120">RADIUS is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

<span data-ttu-id="45f74-121">伺服器資料物件 API 是設計來供使用 C/c + + 或 Visual Basic 開發軟體的程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="45f74-121">The Server Data Objects API is designed for use by programmers using C/C++ or Visual Basic development software.</span></span> <span data-ttu-id="45f74-122">程式設計人員應該熟悉 [遠端存取服務](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) 和 RADIUS 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="45f74-122">Programmers should be familiar with [Remote Access Service](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) and the RADIUS protocol.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="45f74-123">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="45f74-123">Run-time requirements</span></span>

<span data-ttu-id="45f74-124">Windows Server 2008 支援 NPS 擴充功能 API，並安裝 Microsoft 商用網際網路服務 (MCIS) 。</span><span class="sxs-lookup"><span data-stu-id="45f74-124">NPS Extensions API is supported on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

<span data-ttu-id="45f74-125">Windows Server 2008 支援 Server Data Objects API。</span><span class="sxs-lookup"><span data-stu-id="45f74-125">Server Data Objects API is supported on Windows Server 2008.</span></span>

<span data-ttu-id="45f74-126">您可以在 Windows Server 2008 上使用 NPS 安裝 Microsoft 商用網際網路服務 (MCIS) 。</span><span class="sxs-lookup"><span data-stu-id="45f74-126">NPS is available on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="45f74-127">本節內容</span><span class="sxs-lookup"><span data-stu-id="45f74-127">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="45f74-128">概觀</span><span class="sxs-lookup"><span data-stu-id="45f74-128">Overview</span></span>](about-network-policy-server.md)
</dt> <dd>

<span data-ttu-id="45f74-129">關於 RADIUS、IAS 和 NPS 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="45f74-129">General information regarding RADIUS, IAS, and NPS.</span></span>

</dd> <dt>

[<span data-ttu-id="45f74-130">網路原則伺服器延伸模組 API</span><span class="sxs-lookup"><span data-stu-id="45f74-130">Network Policy Server Extensions API</span></span>](ias-extensions.md)
</dt> <dd>

<span data-ttu-id="45f74-131">用來執行用於驗證、授權和帳戶處理之延伸模組 Dll 的 API。</span><span class="sxs-lookup"><span data-stu-id="45f74-131">API for implementing extension DLLs used for authentication, authorization, and accounting.</span></span>

</dd> <dt>

[<span data-ttu-id="45f74-132">伺服器資料物件 API</span><span class="sxs-lookup"><span data-stu-id="45f74-132">Server Data Objects API</span></span>](server-data-objects.md)
</dt> <dd>

<span data-ttu-id="45f74-133">用於管理網路原則設定的 API。</span><span class="sxs-lookup"><span data-stu-id="45f74-133">API for managing the network policy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="45f74-134">SQL 可程式性</span><span class="sxs-lookup"><span data-stu-id="45f74-134">SQL Programmability</span></span>](sql-programmability.md)
</dt> <dd>

<span data-ttu-id="45f74-135">用來管理 NPS (IAS) 記錄的預存程式範例。</span><span class="sxs-lookup"><span data-stu-id="45f74-135">Samples of stored procedures used for managing NPS (IAS) logging.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="45f74-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="45f74-136">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="45f74-137">[TechNet：網路原則伺服器](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="45f74-137">[TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="45f74-138">[TechNet：網際網路驗證服務](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="45f74-138">[TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="45f74-139">網路存取保護</span><span class="sxs-lookup"><span data-stu-id="45f74-139">Network Access Protection</span></span>](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 
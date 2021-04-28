---
description: Microsoft Message Queuing (MSMQ) 移除 Windows 2000 用戶端支援服務
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Microsoft Message Queuing (MSMQ) 移除 Windows 2000 用戶端支援服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be68d40271153567bdaf6b04d73218aaf3d3977
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088146"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a><span data-ttu-id="c2ea5-103">Microsoft Message Queuing (MSMQ) 移除 Windows 2000 用戶端支援服務</span><span class="sxs-lookup"><span data-stu-id="c2ea5-103">Microsoft Message Queuing (MSMQ) - Removal of Windows 2000 Client Support Service</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="c2ea5-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="c2ea5-104">Affected Platforms</span></span>

<span data-ttu-id="c2ea5-105">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2ea5-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="c2ea5-106">功能影響</span><span class="sxs-lookup"><span data-stu-id="c2ea5-106">Feature Impact</span></span>

 <span data-ttu-id="c2ea5-107">**嚴重性** -高</span><span class="sxs-lookup"><span data-stu-id="c2ea5-107">**Severity** - High</span></span>  
<span data-ttu-id="c2ea5-108">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="c2ea5-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="c2ea5-109">Description</span><span class="sxs-lookup"><span data-stu-id="c2ea5-109">Description</span></span>

<span data-ttu-id="c2ea5-110">Windows 2000 用戶端支援服務是訊息佇列伺服器的選用元件，您可以將它安裝在 Windows 2003 或 Windows 2008 網域控制站電腦上。</span><span class="sxs-lookup"><span data-stu-id="c2ea5-110">The Windows 2000 Client Support Service is an optional component of the Message Queuing Server that you can install on a Windows 2003 or Windows 2008 domain controller machine.</span></span> <span data-ttu-id="c2ea5-111">這項服務可讓 Windows 2000 用戶端在 Windows 2003/2008 電腦上安裝任何訊息佇列伺服器的網域整合模式下運作。</span><span class="sxs-lookup"><span data-stu-id="c2ea5-111">This service allows Windows 2000 clients to operate in a domain-integrated mode with any Message Queuing server installed on Windows 2003/2008 machines.</span></span> <span data-ttu-id="c2ea5-112">在 Windows XP 上運作的 MSMQ 用戶端不需要此服務。</span><span class="sxs-lookup"><span data-stu-id="c2ea5-112">MSMQ Clients operating on Windows XP upwards do not need this service.</span></span>

### <a name="manifestation-of-impact"></a><span data-ttu-id="c2ea5-113">影響的表現</span><span class="sxs-lookup"><span data-stu-id="c2ea5-113">Manifestation of Impact</span></span>

<span data-ttu-id="c2ea5-114">當 windows 7 網域中的所有網域控制站都是 Windows Server 2008 R2 的互通性時，這項變更會影響 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="c2ea5-114">This change impacts Windows 2000 when interoperating in a Windows 7 domain where all domain controllers are Windows Server 2008 R2.</span></span> <span data-ttu-id="c2ea5-115">如果客戶升級至 Windows 7 網域，除非這些用戶端升級為較高的 Windows 版本，否則網域中任何 Windows 2000 電腦上的現有 MSMQ 應用程式將無法以網域整合模式運作。</span><span class="sxs-lookup"><span data-stu-id="c2ea5-115">If a customer upgrades to the Windows 7 domain, the existing MSMQ applications on any Windows 2000 machines in the domain will not be able to operate in a domain-integrated mode unless these clients upgrade to a higher Windows version.</span></span>

### <a name="mitigation"></a><span data-ttu-id="c2ea5-116">降低</span><span class="sxs-lookup"><span data-stu-id="c2ea5-116">Mitigation</span></span>

<span data-ttu-id="c2ea5-117">在 Windows 7 網域上具有 Windows 2000 用戶端電腦的使用者，可以設定網域中的 Windows 2003/2008 網域控制站，並在這個網域控制站上安裝 MSMQ Windows 2000 用戶端支援服務。</span><span class="sxs-lookup"><span data-stu-id="c2ea5-117">Users who have Windows 2000 Client machines on a Windows 7 domain can configure a Windows 2003/2008 domain controller in the domain and install the MSMQ Windows 2000 Client Support Service on this domain controller.</span></span>

### <a name="leveraging-feature-capabilities"></a><span data-ttu-id="c2ea5-118">運用功能功能</span><span class="sxs-lookup"><span data-stu-id="c2ea5-118">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="c2ea5-119">具有執行 MSMQ 之 Windows 2000 用戶端電腦的使用者應該升級至較高的 Windows 版本，才能利用 MSMQ 伺服器的 Active Directory 型執行。</span><span class="sxs-lookup"><span data-stu-id="c2ea5-119">Users who have Windows 2000 Client machines running MSMQ should upgrade to a higher Windows version in order to take advantage of the Active Directory-based implementation of the MSMQ Server.</span></span>

### <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="c2ea5-120">相容性、效能、可靠性和可用性測試</span><span class="sxs-lookup"><span data-stu-id="c2ea5-120">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="c2ea5-121">在具有一或多個下層網域控制站的 Windows 7 網域上有 Windows 2000 用戶端電腦執行 MSMQ 的使用者，應該確認其應用程式在此混合網域上是否正常運作。</span><span class="sxs-lookup"><span data-stu-id="c2ea5-121">Users who have Windows 2000 Client machines running MSMQ on a Windows 7 domain with one or more down-level domain controllers should verify that their applications are functional on this mixed domain.</span></span>

 

 




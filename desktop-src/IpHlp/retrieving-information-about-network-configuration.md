---
description: IP 協助程式提供本機電腦網路設定的相關資訊。
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: 正在抓取網路設定的相關資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945141"
---
# <a name="retrieving-information-about-network-configuration"></a><span data-ttu-id="ff4aa-103">正在抓取網路設定的相關資訊</span><span class="sxs-lookup"><span data-stu-id="ff4aa-103">Retrieving Information About Network Configuration</span></span>

<span data-ttu-id="ff4aa-104">IP 協助程式提供本機電腦網路設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ff4aa-104">IP Helper provides information about the network configuration of the local computer.</span></span> <span data-ttu-id="ff4aa-105">若要取出一般設定資訊，請使用 [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) 函數。</span><span class="sxs-lookup"><span data-stu-id="ff4aa-105">To retrieve general configuration information, use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="ff4aa-106">此函數會傳回特定介面卡或介面特有的資訊。</span><span class="sxs-lookup"><span data-stu-id="ff4aa-106">This function returns information that is not specific to a particular adapter or interface.</span></span> <span data-ttu-id="ff4aa-107">例如， **GetNetworkParams** 會傳回本機電腦所使用的 DNS 伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="ff4aa-107">For example, **GetNetworkParams** returns a list of the DNS servers that are used by the local computer.</span></span>

-   <span data-ttu-id="ff4aa-108">如需涉及 [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) 的程式碼範例，請參閱 [使用 GetNetworkParams 抓取資訊](retrieving-information-using-getnetworkparams.md)。</span><span class="sxs-lookup"><span data-stu-id="ff4aa-108">For code samples involving [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) see [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md).</span></span>

 

 




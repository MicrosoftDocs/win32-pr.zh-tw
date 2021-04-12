---
description: IP 協助程式可延伸您管理網路介面的能力。 指定電腦上的介面和介面卡之間有一對一的對應關係。 介面是一個 IP 層級的抽象概念，而介面卡是一個交叉連結層級的抽象概念。
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: 管理介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192663"
---
# <a name="managing-interfaces"></a><span data-ttu-id="2f67b-105">管理介面</span><span class="sxs-lookup"><span data-stu-id="2f67b-105">Managing Interfaces</span></span>

<span data-ttu-id="2f67b-106">IP 協助程式可延伸您管理網路介面的能力。</span><span class="sxs-lookup"><span data-stu-id="2f67b-106">IP Helper extends your abilities to manage network interfaces.</span></span> <span data-ttu-id="2f67b-107">指定電腦上的介面和介面卡之間有一對一的對應關係。</span><span class="sxs-lookup"><span data-stu-id="2f67b-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="2f67b-108">介面是一個 IP 層級的抽象概念，而介面卡是一個交叉連結層級的抽象概念。</span><span class="sxs-lookup"><span data-stu-id="2f67b-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="2f67b-109">使用下列段落中所述的功能來管理本機電腦上的介面。</span><span class="sxs-lookup"><span data-stu-id="2f67b-109">Use the functions described in the following paragraphs to manage interfaces on the local computer.</span></span>

<span data-ttu-id="2f67b-110">[**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces)函數會傳回本機電腦上的介面數目。</span><span class="sxs-lookup"><span data-stu-id="2f67b-110">The [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) function returns the number of interfaces on the local computer.</span></span>

<span data-ttu-id="2f67b-111">[**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)函數會傳回一個資料表，其中包含本機電腦上介面的名稱和對應的索引。</span><span class="sxs-lookup"><span data-stu-id="2f67b-111">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function returns a table that contains the names and corresponding indexes for the interfaces on the local computer.</span></span> <span data-ttu-id="2f67b-112">如需涉及 **GetInterfaceInfo** 的程式碼範例，請參閱 [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)。</span><span class="sxs-lookup"><span data-stu-id="2f67b-112">For code samples involving **GetInterfaceInfo** see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="2f67b-113">[**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex)函式會接受介面索引，並傳回回溯相容的介面索引，也就是只使用較低24位的介面索引。</span><span class="sxs-lookup"><span data-stu-id="2f67b-113">The [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) function takes an interface index and returns a backward-compatible interface index, that is, one that uses only the lower 24 bits.</span></span> <span data-ttu-id="2f67b-114">這種類型的索引有時稱為「易記」介面索引。</span><span class="sxs-lookup"><span data-stu-id="2f67b-114">This type of index is sometimes referred to as a "friendly" interface index.</span></span>

<span data-ttu-id="2f67b-115">[**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry)函數會傳回 [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow)結構，其中包含本機電腦上特定介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f67b-115">The [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) function returns a [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) structure that contains information about a particular interface on the local computer.</span></span> <span data-ttu-id="2f67b-116">此函式需要呼叫端提供介面的索引。</span><span class="sxs-lookup"><span data-stu-id="2f67b-116">This function requires the caller to supply the index of the interface.</span></span>

<span data-ttu-id="2f67b-117">[**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable)函式會傳回 [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow)專案的資料表，也就是電腦上的每個介面各一個。</span><span class="sxs-lookup"><span data-stu-id="2f67b-117">The [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) function returns a table of [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) entries, one for each interface on the computer.</span></span>

<span data-ttu-id="2f67b-118">您可以使用 [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) 函數來修改特定介面的設定。</span><span class="sxs-lookup"><span data-stu-id="2f67b-118">Use the [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) function to modify the configuration of a particular interface.</span></span>

 

 

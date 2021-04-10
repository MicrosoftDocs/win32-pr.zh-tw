---
description: 多播 COM 介面可讓您存取網路功能，以在多播位址上配置、更新和釋放租用。
ms.assetid: d4da9616-bdb4-4919-96aa-9e45582b05dd
title: 多播 COM 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01370372e3ea05b27dc789f90918b148075c28f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689443"
---
# <a name="multicast-com-interfaces"></a><span data-ttu-id="dd69b-103">多播 COM 介面</span><span class="sxs-lookup"><span data-stu-id="dd69b-103">Multicast COM Interfaces</span></span>

<span data-ttu-id="dd69b-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="dd69b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dd69b-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="dd69b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dd69b-106">多播 COM 介面可讓您存取網路的功能，以在多播位址上配置、更新和釋放租用。</span><span class="sxs-lookup"><span data-stu-id="dd69b-106">The multicast COM interfaces allow access to the network's facility for allocating, renewing, and releasing leases on multicast addresses.</span></span> <span data-ttu-id="dd69b-107">它們會封裝一組函數和資料結構定義。</span><span class="sxs-lookup"><span data-stu-id="dd69b-107">They encapsulate a set of function and data structure definitions.</span></span> <span data-ttu-id="dd69b-108">COM 介面讓程式設計師免于理解和操作這些資料結構的負擔。</span><span class="sxs-lookup"><span data-stu-id="dd69b-108">The COM interfaces free the programmer from the burden of understanding and manipulating these data structures.</span></span> <span data-ttu-id="dd69b-109">此外，因為 TAPI 3 本身是以 COM 為基礎，所以這些介面可讓您以與 TAPI 3 所提供的其他功能一致的方式來存取多播位址配置。</span><span class="sxs-lookup"><span data-stu-id="dd69b-109">Moreover, because TAPI 3 itself is COM-based, these interfaces make multicast address allocation accessible in a way that is consistent with the other facilities provided by TAPI 3.</span></span> <span data-ttu-id="dd69b-110">使用 Visual Basic、JAVA 或指令碼語言所撰寫的應用程式通常無法直接存取 Windows API，因此能夠使用這些介面。</span><span class="sxs-lookup"><span data-stu-id="dd69b-110">Applications written using Visual Basic, Java, or scripting languages that cannot normally access the Windows API directly are able to use these interfaces.</span></span>

<span data-ttu-id="dd69b-111">多播位址配置目前是 IETF 工作群組的主體。</span><span class="sxs-lookup"><span data-stu-id="dd69b-111">Multicast address allocation is currently the subject of an IETF working group.</span></span> <span data-ttu-id="dd69b-112">若要存取目前的資訊，請使用任何網際網路搜尋引擎來查詢 "MDHCP" 或 "MADCAP" 和 "Internet draft"。</span><span class="sxs-lookup"><span data-stu-id="dd69b-112">To access current information, query on "MDHCP" or "MADCAP" and "Internet draft" using any Internet search engine.</span></span> <span data-ttu-id="dd69b-113">除了 MADCAP，建議的架構還包含網域內的伺服器對伺服器協調通訊協定，以及用於領域間協調的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="dd69b-113">In addition to MADCAP, the proposed architecture includes a protocol for server-to-server coordination within a domain or AS, as well as a protocol for interdomain coordination.</span></span> <span data-ttu-id="dd69b-114">雖然此架構目前不斷演進，但用戶端不需要關注此配置的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dd69b-114">While this architecture is currently evolving, the client need not concern itself with the details of this scheme.</span></span>

<span data-ttu-id="dd69b-115">此元件目前僅支援 IP 第4版位址。</span><span class="sxs-lookup"><span data-stu-id="dd69b-115">This component currently supports only IP version 4 addresses.</span></span>

> [!Note]  
> <span data-ttu-id="dd69b-116">用於這些介面的通訊協定目前名為 MADCAP。</span><span class="sxs-lookup"><span data-stu-id="dd69b-116">The protocol used for these interfaces is currently named MADCAP.</span></span> <span data-ttu-id="dd69b-117">在先前的版本中，它稱為 MDHCP。</span><span class="sxs-lookup"><span data-stu-id="dd69b-117">In previous versions it was known as MDHCP.</span></span>

 

<span data-ttu-id="dd69b-118">多播物件是藉由在 [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)介面上呼叫 **CoCreateInstance** 所建立。</span><span class="sxs-lookup"><span data-stu-id="dd69b-118">The multicast object is created by calling **CoCreateInstance** on the [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation) interface.</span></span> <span data-ttu-id="dd69b-119">**IMcastAddressAllocation** 介面會公開 [**EnumerateScopes**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes)方法，可讓應用程式取得所有可用多播範圍的清單。</span><span class="sxs-lookup"><span data-stu-id="dd69b-119">The **IMcastAddressAllocation** interface exposes the [**EnumerateScopes**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-enumeratescopes) method, which allows an application to get a list of all available multicast scopes.</span></span>

<span data-ttu-id="dd69b-120">一旦取得工作範圍，就會使用 [**RequestAddress**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) 方法向伺服器要求多播位址。</span><span class="sxs-lookup"><span data-stu-id="dd69b-120">Once a working scope has been obtained, the [**RequestAddress**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastaddressallocation-requestaddress) method is used to request a multicast address from the server.</span></span> <span data-ttu-id="dd69b-121">如果要求成功，則會傳回 [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) 指標。</span><span class="sxs-lookup"><span data-stu-id="dd69b-121">If the request is successful, an [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo) pointer is returned.</span></span> <span data-ttu-id="dd69b-122">然後，您可以使用此介面公開的 [**EnumerateAddresses**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) 方法來取得位址。</span><span class="sxs-lookup"><span data-stu-id="dd69b-122">The [**EnumerateAddresses**](/windows/desktop/api/Mdhcp/nf-mdhcp-imcastleaseinfo-enumerateaddresses) method exposed by this interface can then be used to obtain the addresses.</span></span>

<span data-ttu-id="dd69b-123">與會議相關聯的每個媒體物件都會公開 [**ITConnection**](itconnection.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="dd69b-123">Each Media object associated with the conference exposes an [**ITConnection**](itconnection.md) interface.</span></span> <span data-ttu-id="dd69b-124">[**ITConnection：： SetAddressInfo**](itconnection-setaddressinfo.md)方法允許指派取得給會議媒體的多播位址。</span><span class="sxs-lookup"><span data-stu-id="dd69b-124">The [**ITConnection::SetAddressInfo**](itconnection-setaddressinfo.md) method allows assignment of the multicast addresses obtained to the media of the conference.</span></span> <span data-ttu-id="dd69b-125">您必須為與會議相關聯之每個媒體物件的每個 **ITConnection** 介面設定位址。</span><span class="sxs-lookup"><span data-stu-id="dd69b-125">The address must be set for each **ITConnection** interface of every Media object associated with the conference.</span></span>

 

 




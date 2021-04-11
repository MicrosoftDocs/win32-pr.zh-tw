---
title: SNMP 服務
description: 簡易網路管理通訊協定 (SNMP) 的 Microsoft Windows 將會用來設定遠端裝置、監視網路效能、審核網路使用量，以及偵測網路錯誤或不適當的存取。重要事項： Microsoft Windows SNMP API 僅支援最多 SNMPv2C 的通訊協定版本。 它不支援任何較新版本的通訊協定。
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP，起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023973"
---
# <a name="snmp-service"></a><span data-ttu-id="af812-106">SNMP 服務</span><span class="sxs-lookup"><span data-stu-id="af812-106">SNMP Service</span></span>

<span data-ttu-id="af812-107">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="af812-107">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af812-108">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="af812-108">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="af812-109">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="af812-109">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

## <a name="purpose"></a><span data-ttu-id="af812-110">目的</span><span class="sxs-lookup"><span data-stu-id="af812-110">Purpose</span></span>

<span data-ttu-id="af812-111">簡易網路管理通訊協定 (SNMP) 的 Microsoft Windows 將會用來設定遠端裝置、監視網路效能、審核網路使用量，以及偵測網路錯誤或不適當的存取。</span><span class="sxs-lookup"><span data-stu-id="af812-111">The Microsoft Windows implementation of the Simple Network Management Protocol (SNMP) is used to configure remote devices, monitor network performance, audit network usage, and detect network faults or inappropriate access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af812-112">Microsoft Windows SNMP API 僅支援最多 SNMPv2C 的通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="af812-112">The Microsoft Windows SNMP API only supports protocol versions up to SNMPv2C.</span></span> <span data-ttu-id="af812-113">它不支援任何較新版本的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="af812-113">It does not support any later versions of the protocol.</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="af812-114">適用時</span><span class="sxs-lookup"><span data-stu-id="af812-114">Where applicable</span></span>

<span data-ttu-id="af812-115">SNMP 使用由管理應用程式和代理程式應用程式所組成的分散式架構。</span><span class="sxs-lookup"><span data-stu-id="af812-115">SNMP uses a distributed architecture consisting of management applications and agent applications.</span></span> <span data-ttu-id="af812-116">SNMP 服務會實行 SNMP 代理程式。</span><span class="sxs-lookup"><span data-stu-id="af812-116">The SNMP service implements an SNMP agent.</span></span> <span data-ttu-id="af812-117">若要使用 SNMP 服務所提供的資訊，您必須至少有一部執行 SNMP 管理應用程式的主機。</span><span class="sxs-lookup"><span data-stu-id="af812-117">To use the information the SNMP service provides, you must have at least one host that is running an SNMP management application.</span></span> <span data-ttu-id="af812-118">您可以使用協力廠商 SNMP 管理軟體，也可以開發自己的 SNMP 管理軟體應用程式。</span><span class="sxs-lookup"><span data-stu-id="af812-118">You can use third-party SNMP management software, or you can develop your own SNMP management software application.</span></span> <span data-ttu-id="af812-119">下列 Api 適用于此用途：</span><span class="sxs-lookup"><span data-stu-id="af812-119">The following APIs are available for this purpose:</span></span>

-   <span data-ttu-id="af812-120">SNMP 管理 API，這組函式可用來快速開發基本的 SNMP 管理系統</span><span class="sxs-lookup"><span data-stu-id="af812-120">SNMP Management API, a set of functions that can be used to quickly develop basic SNMP management systems</span></span>
-   <span data-ttu-id="af812-121">WinSNMP API，版本2.0，一組用來編碼、解碼、傳送和接收 SNMP 訊息的函數</span><span class="sxs-lookup"><span data-stu-id="af812-121">WinSNMP API, version 2.0, a set of functions for encoding, decoding, sending, and receiving SNMP messages</span></span>

<span data-ttu-id="af812-122">此外，SNMP 延伸模組代理程式 API 會定義 SNMP 服務與協力廠商 SNMP 延伸代理程式 Dll 之間的介面。</span><span class="sxs-lookup"><span data-stu-id="af812-122">Additionally, the SNMP Extension Agent API defines the interface between the SNMP service and third-party SNMP extension agent DLLs.</span></span> <span data-ttu-id="af812-123">SNMP 公用程式 API 函數可以用來簡化 SNMP 訊息的處理。</span><span class="sxs-lookup"><span data-stu-id="af812-123">The SNMP Utility API functions can be used to simplify the processing of SNMP messages.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="af812-124">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="af812-124">Developer audience</span></span>

<span data-ttu-id="af812-125">上一節所列的 Api 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="af812-125">The APIs listed in the preceding section are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="af812-126">您必須熟悉 SNMP 和 SNMPv2C，以及網路和網路管理概念的實用知識。</span><span class="sxs-lookup"><span data-stu-id="af812-126">Familiarity with SNMP and SNMPv2C, as well as a working knowledge of networking and network management concepts, are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="af812-127">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="af812-127">Run-time requirements</span></span>

<span data-ttu-id="af812-128">如需有關使用特定功能所需之作業系統的詳細資訊，請參閱該函式之參考頁面的需求一節。</span><span class="sxs-lookup"><span data-stu-id="af812-128">For more information about the operating system required to use a particular function, see the Requirements section of the reference page for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="af812-129">本節內容</span><span class="sxs-lookup"><span data-stu-id="af812-129">In this section</span></span>



| <span data-ttu-id="af812-130">主題</span><span class="sxs-lookup"><span data-stu-id="af812-130">Topic</span></span>                                                                                                | <span data-ttu-id="af812-131">描述</span><span class="sxs-lookup"><span data-stu-id="af812-131">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af812-132">SNMP 的新功能</span><span class="sxs-lookup"><span data-stu-id="af812-132">New in SNMP</span></span>](new-in-snmp.md)<br/>                                                            | <span data-ttu-id="af812-133">SNMP 更新的資訊。</span><span class="sxs-lookup"><span data-stu-id="af812-133">Information on updates to SNMP.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="af812-134">簡易網路管理通訊協定 (SNMP)</span><span class="sxs-lookup"><span data-stu-id="af812-134">Simple Network Management Protocol (SNMP)</span></span>](simple-network-management-protocol-snmp-.md)<br/> | <span data-ttu-id="af812-135">SNMP 的資訊和 API 參考，包括 SNMP 管理 API、SNMP 延伸模組代理程式 API，以及 SNMP 公用程式 API 函式。</span><span class="sxs-lookup"><span data-stu-id="af812-135">Information and API reference for SNMP, including the SNMP Management API, SNMP Extension Agent API, and SNMP Utility API functions.</span></span><br/> |
| [<span data-ttu-id="af812-136">WinSNMP API</span><span class="sxs-lookup"><span data-stu-id="af812-136">WinSNMP API</span></span>](snmp-reference.md)<br/>                                                         | <span data-ttu-id="af812-137">Microsoft Windows SNMP 應用程式開發介面的資訊和 API 參考 (的 WinSNMP API) 。</span><span class="sxs-lookup"><span data-stu-id="af812-137">Information and API reference for the Microsoft Windows SNMP Application Programming Interface (WinSNMP API).</span></span> <br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="af812-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="af812-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af812-139">動態主機設定通訊協定 (DHCP)</span><span class="sxs-lookup"><span data-stu-id="af812-139">Dynamic Host Configuration Protocol (DHCP)</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="af812-140">網路管理</span><span class="sxs-lookup"><span data-stu-id="af812-140">Network Management</span></span>](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[<span data-ttu-id="af812-141">路由及遠端存取服務</span><span class="sxs-lookup"><span data-stu-id="af812-141">Routing and Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 


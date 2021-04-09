---
title: 關於 SNMP
description: SNMP 使用由管理員和代理程式所組成的分散式架構。
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023920"
---
# <a name="about-snmp"></a><span data-ttu-id="a1c99-104">關於 SNMP</span><span class="sxs-lookup"><span data-stu-id="a1c99-104">About SNMP</span></span>

<span data-ttu-id="a1c99-105">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a1c99-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a1c99-106">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a1c99-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a1c99-107">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="a1c99-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="a1c99-108">SNMP 使用由管理員和代理程式所組成的分散式架構。</span><span class="sxs-lookup"><span data-stu-id="a1c99-108">SNMP uses a distributed architecture consisting of managers and agents.</span></span> <span data-ttu-id="a1c99-109">代理程式是從 SNMP 管理員應用程式回應查詢的 SNMP 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a1c99-109">An agent is an SNMP application that responds to queries from SNMP manager applications.</span></span> <span data-ttu-id="a1c99-110">SNMP 代理程式負責根據 SNMP 管理程式的要求，擷取與更新本機管理資訊。</span><span class="sxs-lookup"><span data-stu-id="a1c99-110">The SNMP agent is responsible for retrieving and updating local management information based on the requests of the SNMP manager.</span></span> <span data-ttu-id="a1c99-111">當發生重大事件或陷阱被觸發時，代理程式也會通知已登錄的管理程式。</span><span class="sxs-lookup"><span data-stu-id="a1c99-111">The agent also notifies registered managers when significant events or traps occur.</span></span> <span data-ttu-id="a1c99-112">管理員是 SNMP 應用程式，可產生 SNMP 代理程式應用程式的查詢，並接收來自 SNMP 代理程式應用程式的陷阱。</span><span class="sxs-lookup"><span data-stu-id="a1c99-112">A manager is an SNMP application that generates queries to SNMP agent applications and receives traps from SNMP agent applications.</span></span>

<span data-ttu-id="a1c99-113">在執行 Microsoft Windows XP/Windows 2000/Windows NT 的電腦上，snmp 代理程式是由 SNMP 服務 (SNMP.EXE) 所執行。</span><span class="sxs-lookup"><span data-stu-id="a1c99-113">On computers running Microsoft Windows XP/Windows 2000/Windows NT, the SNMP agent is implemented by the SNMP service (SNMP.EXE).</span></span> <span data-ttu-id="a1c99-114">SNMP 管理員通常是協力廠商 SNMP 管理主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="a1c99-114">The SNMP manager is typically a third-party SNMP management console application.</span></span> <span data-ttu-id="a1c99-115">管理主控台應用程式不需要在與 SNMP 代理程式相同的主機上執行。</span><span class="sxs-lookup"><span data-stu-id="a1c99-115">The management console application does not need to run on the same host as the SNMP agent.</span></span> <span data-ttu-id="a1c99-116">若要使用 Microsoft SNMP 服務所提供的資訊，您至少需要一個 SNMP 管理主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="a1c99-116">To use the information the Microsoft SNMP service provides, you need at least one SNMP management console application.</span></span> <span data-ttu-id="a1c99-117">系統包含支援 SNMP 管理主控台應用程式的程式庫，但目前不包含 SNMP 管理主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="a1c99-117">The system includes libraries that support SNMP management console applications, but it does not include an SNMP management console application at this time.</span></span>

 

 
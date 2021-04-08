---
title: SNMP 的新功能
description: 從 Windows Vista 開始，SNMP 支援使用 IPv6。
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682978"
---
# <a name="new-in-snmp"></a><span data-ttu-id="5f2be-103">SNMP 的新功能</span><span class="sxs-lookup"><span data-stu-id="5f2be-103">New in SNMP</span></span>

<span data-ttu-id="5f2be-104">\[SNMP 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5f2be-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5f2be-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="5f2be-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5f2be-106">相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]</span><span class="sxs-lookup"><span data-stu-id="5f2be-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="5f2be-107">從 Windows Vista 開始，SNMP 支援使用 IPv6。</span><span class="sxs-lookup"><span data-stu-id="5f2be-107">SNMP supports the use of IPv6 starting with Windows Vista.</span></span> <span data-ttu-id="5f2be-108">不過，SNMP 僅針對執行 Windows Server 2008 和 Windows Vista 的網路支援 IPv6。</span><span class="sxs-lookup"><span data-stu-id="5f2be-108">However, SNMP supports IPv6 only for networks running Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="5f2be-109">這是因為 SNMP 需要在這些作業系統中提供更新的通訊協定堆疊，才能支援其 IPv6。</span><span class="sxs-lookup"><span data-stu-id="5f2be-109">This is because SNMP requires the updated protocol stack available in these operating systems for its IPv6 support.</span></span>

<span data-ttu-id="5f2be-110">除非您的網路只是 Windows Server 2008 網路，否則 IPv6 通訊會失敗，即使在執行舊版 Windows 的電腦上個別安裝 IPv6 通訊協定堆疊也是如此。</span><span class="sxs-lookup"><span data-stu-id="5f2be-110">Unless your network is solely a Windows Server 2008 network, IPv6 communications will fail, even if an IPv6 protocol stack is separately installed on those computers that run earlier versions of Windows.</span></span> <span data-ttu-id="5f2be-111">例如，在 Windows Server 2003、Windows XP 或 Windows 2000 上執行的 SNMP 代理程式，只會回應對其 IPv4 位址所做的查詢。</span><span class="sxs-lookup"><span data-stu-id="5f2be-111">For example, SNMP agents that run on Windows Server 2003, or Windows XP, or Windows 2000, respond only to queries that are made to their IPv4 addresses.</span></span>

 

 
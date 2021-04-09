---
title: Network List Manager 的角色
description: Network List Manager 的角色
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840824"
---
# <a name="the-role-of-network-list-manager"></a><span data-ttu-id="e599d-103">Network List Manager 的角色</span><span class="sxs-lookup"><span data-stu-id="e599d-103">The Role of Network List Manager</span></span>

<span data-ttu-id="e599d-104">在 Windows XP 與 Windows Server 2003 之前，應用程式必須呼叫一些不相關的 Api，以取得網路屬性的相關資料，例如 IP 位址、網域控制站或網域名稱系統 (DNS) 。</span><span class="sxs-lookup"><span data-stu-id="e599d-104">Prior to Windows XP and Windows Server 2003, applications were required to call a number of unrelated APIs to obtain data about network attributes such as the IP address, the domain controller, or the Domain Name System (DNS).</span></span> <span data-ttu-id="e599d-105">從 Windows XP 和 Windows Server 2003 開始，網路定位感知 Winsock API 會提供一組有限的網路位置功能。</span><span class="sxs-lookup"><span data-stu-id="e599d-105">Starting with Windows XP and Windows Server 2003, the Network Location Awareness Winsock API featured a limited set of network location functionality.</span></span> <span data-ttu-id="e599d-106">在 Windows Server 2008 和 Windows Vista 中，網路覺察服務會在一個位置中捕捉網路屬性，並讓應用程式查詢及取出特定的網路和屬性。</span><span class="sxs-lookup"><span data-stu-id="e599d-106">In Windows Server 2008 and Windows Vista, the Network Awareness service captures the network attributes in one location and allows applications to query and retrieve specific networks and attributes.</span></span> <span data-ttu-id="e599d-107">網路清單管理員會以 Winsock 命名空間提供者取代舊版 Winsock API (的功能，) 同時使用 Winsock API 維持與繼承應用程式的相容性。</span><span class="sxs-lookup"><span data-stu-id="e599d-107">Network List Manager replaces the functionality of the previous Winsock API (available as a Winsock Name Space Provider) while maintaining compatibility with older applications using the Winsock API.</span></span>

 

 





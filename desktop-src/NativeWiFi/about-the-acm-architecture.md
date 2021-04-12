---
description: 關於當的架構
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: 關於當的架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f037a1823f7045ccaf1dc573c6d213beeebe0a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194943"
---
# <a name="about-the-acm-architecture"></a><span data-ttu-id="f90e6-103">關於當的架構</span><span class="sxs-lookup"><span data-stu-id="f90e6-103">About the ACM Architecture</span></span>

<span data-ttu-id="f90e6-104">自動設定模組 (的配置) 是適用于 Windows Vista 的新無線設置元件。</span><span class="sxs-lookup"><span data-stu-id="f90e6-104">The Auto Configuration Module (ACM) is the new wireless configuration component for Windows Vista.</span></span> <span data-ttu-id="f90e6-105">Windows XP Service Pack 3 (SP3) 和適用于 Windows XP Service Pack 2 (SP2 的無線區域網路 API) 改為使用無線零設定 (WZC) 服務。</span><span class="sxs-lookup"><span data-stu-id="f90e6-105">Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2) use the Wireless Zero Configuration (WZC) service instead.</span></span>

<span data-ttu-id="f90e6-106">當該網路有啟用自動連線的介面時，會定期掃描網路，並使用反復的程式來選取並聯機到範圍內最慣用的網路。</span><span class="sxs-lookup"><span data-stu-id="f90e6-106">The ACM scans networks periodically and uses an iterative process to select and connect to the most preferred network in the range, if that network has an interface enabled for auto-connection.</span></span> <span data-ttu-id="f90e6-107">此設定檔也會儲存並取出網路設定檔，其中包含配置配置、媒體特定模組 (MSM) 、安全性和獨立硬體廠商 (IHV) 設定。</span><span class="sxs-lookup"><span data-stu-id="f90e6-107">The ACM also saves and retrieves network profiles, which contain ACM, Media Specific Module (MSM), security, and independent hardware vendor (IHV) settings.</span></span> <span data-ttu-id="f90e6-108">這些網路設定檔適用于自動設定。</span><span class="sxs-lookup"><span data-stu-id="f90e6-108">These network profiles are for auto configuration.</span></span>

<span data-ttu-id="f90e6-109">自動設定同時支援全域和個別介面設定和網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="f90e6-109">Auto configuration supports both global and per-interface settings and network profiles.</span></span> <span data-ttu-id="f90e6-110">如果電腦已加入具有群組原則物件的網域 (GPO) 在網域層級或組織單位 (OU) 層級的 Active Directory (AD) 階層中，就會設定全域設定和網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="f90e6-110">The global settings and network profiles are configured if the machine has joined a domain with a group policy object (GPO) either at the domain level or the organizational unit (OU) level in the Active Directory (AD) hierarchy.</span></span> <span data-ttu-id="f90e6-111">這些群組原則設定和設定檔是唯讀的，會套用至系統中的每個802.11 介面，且一律優先于每個介面和個別使用者的設定和網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="f90e6-111">These group policy settings and profiles are read-only, applied to each 802.11 interface in the system, and always take precedence over the per-interface and per-user settings and network profiles.</span></span> <span data-ttu-id="f90e6-112">群組原則設定檔會放在每個802.11 網路介面上慣用網路設定檔案清單的頂端。</span><span class="sxs-lookup"><span data-stu-id="f90e6-112">The group policy profiles are placed at the top of the preferred network profile list on each 802.11 network interface.</span></span>

<span data-ttu-id="f90e6-113">可延伸的架構是可延伸的。</span><span class="sxs-lookup"><span data-stu-id="f90e6-113">The ACM architecture is extensible.</span></span> <span data-ttu-id="f90e6-114">Ihv 可以實行專屬的無線功能，而不需要改變所提供的原生802.11 架構。</span><span class="sxs-lookup"><span data-stu-id="f90e6-114">IHVs can implement proprietary wireless functionality without altering the provided native 802.11 framework.</span></span> <span data-ttu-id="f90e6-115">公開的 IHV 控制函式和結構可啟用此擴充性。</span><span class="sxs-lookup"><span data-stu-id="f90e6-115">The exposed IHV control functions and structures enable this extensibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f90e6-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="f90e6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f90e6-117">關於原生 Wifi</span><span class="sxs-lookup"><span data-stu-id="f90e6-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 




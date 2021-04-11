---
description: Windows XP Service Pack 2 (SP2) 和 Windows XP Service Pack 3 (SP3) ，支援原生 Wifi API 功能的子集。
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Windows XP 上的原生 Wifi API 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319380"
---
# <a name="native-wifi-api-support-on-windows-xp"></a><span data-ttu-id="47054-103">Windows XP 上的原生 Wifi API 支援</span><span class="sxs-lookup"><span data-stu-id="47054-103">Native Wifi API Support on Windows XP</span></span>

<span data-ttu-id="47054-104">Windows XP Service Pack 2 (SP2) 和 Windows XP Service Pack 3 (SP3) ，支援原生 Wifi API 功能的子集。</span><span class="sxs-lookup"><span data-stu-id="47054-104">A subset of the Native Wifi API functionality is supported on Windows XP with Service Pack 2 (SP2) and Windows XP with Service Pack 3 (SP3).</span></span> <span data-ttu-id="47054-105">這項功能預設包含在 Windows XP SP3 中。</span><span class="sxs-lookup"><span data-stu-id="47054-105">This functionality is included in Windows XP with SP3 by default.</span></span> <span data-ttu-id="47054-106">在 Windows XP （含 SP2）中，藉由套用可在 Windows XP Service Pack 2 (SP2) 的無線區域網路 API 的修正程式來新增此功能。</span><span class="sxs-lookup"><span data-stu-id="47054-106">In Windows XP with SP2, this functionality can be added by applying a hotfix, which is known as Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="47054-107">如需詳細資訊或下載此修正程式，請參閱說明及支援知識庫中的「開發人員無法建立可透過 Microsoft Windows XP Service Pack 2 中的無線零設定服務管理無線設定檔和連線 (SP2) 」的無線用戶端程式 [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) 。</span><span class="sxs-lookup"><span data-stu-id="47054-107">For more information or to download the hotfix, see "Developers cannot create wireless client programs that manage wireless profiles and connections over the Wireless Zero Configuration service in Microsoft Windows XP Service Pack 2 (SP2)" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997).</span></span>

<span data-ttu-id="47054-108">由於 Windows XP 中的基礎架構差異，原生 Wifi API 有一些限制。</span><span class="sxs-lookup"><span data-stu-id="47054-108">Because of underlying architectural differences in Windows XP, the Native Wifi API on has some limitations.</span></span> <span data-ttu-id="47054-109">以下是限制清單：</span><span class="sxs-lookup"><span data-stu-id="47054-109">Here is a list of limitations:</span></span>

-   <span data-ttu-id="47054-110">最多可以有一個與設定檔相關聯的 SSID。</span><span class="sxs-lookup"><span data-stu-id="47054-110">At most one SSID can be associated with a profile.</span></span>
-   <span data-ttu-id="47054-111">基礎結構網路一律會出現在配置檔案清單中的特定網路之前。</span><span class="sxs-lookup"><span data-stu-id="47054-111">Infrastructure networks always appear before ad hoc networks in the profile list.</span></span>
-   <span data-ttu-id="47054-112">設定檔名稱衍生自 SSID，使用者無法將其設定為任一字元串。</span><span class="sxs-lookup"><span data-stu-id="47054-112">Profile names are derived from the SSID, and cannot be set by the user to an arbitrary string.</span></span>
-   <span data-ttu-id="47054-113">不支援 PHY 類型。</span><span class="sxs-lookup"><span data-stu-id="47054-113">PHY types are not supported.</span></span>
-   <span data-ttu-id="47054-114">不支援將 (PMK) 快取成對的主要金鑰。</span><span class="sxs-lookup"><span data-stu-id="47054-114">Pairwise master key (PMK) caching is not supported.</span></span>
-   <span data-ttu-id="47054-115">獨立硬體廠商 (IHV) 擴充功能不受支援。</span><span class="sxs-lookup"><span data-stu-id="47054-115">Independent hardware vendor (IHV) extensibility functions are not supported.</span></span>
-   <span data-ttu-id="47054-116">不支援設定檔許可權。</span><span class="sxs-lookup"><span data-stu-id="47054-116">Profile permissions are not supported.</span></span>
-   <span data-ttu-id="47054-117">只有 wlan 通知進行中的連線 \_ \_ \_ \_ 完成，而且有 \_ 提供 wlan 通知的 \_ \_ 已中斷連線通知。</span><span class="sxs-lookup"><span data-stu-id="47054-117">Only the wlan\_notification\_acm\_connection\_complete and the wlan\_notification\_acm\_disconnected notifications are available.</span></span>
-   <span data-ttu-id="47054-118">不支援 Global 802.1 X 和 EAPOL configuration 設定。</span><span class="sxs-lookup"><span data-stu-id="47054-118">Global 802.1X and EAPOL configuration settings are not supported.</span></span>

<span data-ttu-id="47054-119">Windows XP 含 SP3 和適用于 Windows XP SP2 的無線區域網路 API 支援下列功能：</span><span class="sxs-lookup"><span data-stu-id="47054-119">The following functions are supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:</span></span>

-   [<span data-ttu-id="47054-120">**WLAN \_ 通知 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="47054-120">**WLAN\_NOTIFICATION\_CALLBACK**</span></span>](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [<span data-ttu-id="47054-121">**WlanAllocateMemory**</span><span class="sxs-lookup"><span data-stu-id="47054-121">**WlanAllocateMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [<span data-ttu-id="47054-122">**WlanCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="47054-122">**WlanCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [<span data-ttu-id="47054-123">**WlanConnect**</span><span class="sxs-lookup"><span data-stu-id="47054-123">**WlanConnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [<span data-ttu-id="47054-124">**WlanDeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="47054-124">**WlanDeleteProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [<span data-ttu-id="47054-125">**WlanDisconnect**</span><span class="sxs-lookup"><span data-stu-id="47054-125">**WlanDisconnect**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [<span data-ttu-id="47054-126">**WlanEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="47054-126">**WlanEnumInterfaces**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [<span data-ttu-id="47054-127">**WlanFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="47054-127">**WlanFreeMemory**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [<span data-ttu-id="47054-128">**WlanGetAvailableNetworkList**</span><span class="sxs-lookup"><span data-stu-id="47054-128">**WlanGetAvailableNetworkList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [<span data-ttu-id="47054-129">**WlanGetProfile**</span><span class="sxs-lookup"><span data-stu-id="47054-129">**WlanGetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [<span data-ttu-id="47054-130">**WlanGetProfileList**</span><span class="sxs-lookup"><span data-stu-id="47054-130">**WlanGetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [<span data-ttu-id="47054-131">**WlanOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="47054-131">**WlanOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [<span data-ttu-id="47054-132">**WlanQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="47054-132">**WlanQueryInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [<span data-ttu-id="47054-133">**WlanReasonCodeToString**</span><span class="sxs-lookup"><span data-stu-id="47054-133">**WlanReasonCodeToString**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [<span data-ttu-id="47054-134">**WlanRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="47054-134">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [<span data-ttu-id="47054-135">**WlanScan**</span><span class="sxs-lookup"><span data-stu-id="47054-135">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [<span data-ttu-id="47054-136">**WlanSetInterface**</span><span class="sxs-lookup"><span data-stu-id="47054-136">**WlanSetInterface**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [<span data-ttu-id="47054-137">**WlanSetProfile**</span><span class="sxs-lookup"><span data-stu-id="47054-137">**WlanSetProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [<span data-ttu-id="47054-138">**WlanSetProfileEapXmlUserData**</span><span class="sxs-lookup"><span data-stu-id="47054-138">**WlanSetProfileEapXmlUserData**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [<span data-ttu-id="47054-139">**WlanSetProfileList**</span><span class="sxs-lookup"><span data-stu-id="47054-139">**WlanSetProfileList**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [<span data-ttu-id="47054-140">**WlanSetProfilePosition**</span><span class="sxs-lookup"><span data-stu-id="47054-140">**WlanSetProfilePosition**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a><span data-ttu-id="47054-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="47054-141">Related topics</span></span>

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[<span data-ttu-id="47054-142">關於原生 Wifi</span><span class="sxs-lookup"><span data-stu-id="47054-142">About Native Wifi</span></span>](about-native-wifi.md)
</dt> </dl>

 

 

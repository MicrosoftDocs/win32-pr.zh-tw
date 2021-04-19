---
description: 示範無線託管網路功能的使用。
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: 無線託管網路範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974061"
---
# <a name="wireless-hosted-network-sample"></a><span data-ttu-id="09cf9-103">無線託管網路範例</span><span class="sxs-lookup"><span data-stu-id="09cf9-103">Wireless Hosted Network Sample</span></span>

<span data-ttu-id="09cf9-104">Microsoft Windows 軟體開發套件 (SDK) 隨附的無線裝載網路範例，示範如何使用無線裝載的網路功能。</span><span class="sxs-lookup"><span data-stu-id="09cf9-104">A wireless Hosted Network sample that demonstrates the use of wireless Hosted Network functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="09cf9-105">您可以從 [下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)取得最新版本的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="09cf9-105">The latest version of the Windows SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span>

<span data-ttu-id="09cf9-106">根據預設，無線裝載的網路範例原始程式碼會安裝在下列目錄中：</span><span class="sxs-lookup"><span data-stu-id="09cf9-106">By default, the wireless Hosted Network sample source code is installed in the following directory:</span></span>

<span data-ttu-id="09cf9-107">**C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ NetDs \\ Wlan**</span><span class="sxs-lookup"><span data-stu-id="09cf9-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="09cf9-108">無線 Hosted Network 範例位於下列資料夾底下：</span><span class="sxs-lookup"><span data-stu-id="09cf9-108">The wireless Hosted Network sample is located under the following folder:</span></span>

<span data-ttu-id="09cf9-109">**WirelessHostedNetwork**</span><span class="sxs-lookup"><span data-stu-id="09cf9-109">**WirelessHostedNetwork**</span></span>

<span data-ttu-id="09cf9-110">您可以在 Windows 7 的 Windows SDK 上編譯無線裝載的網路範例。</span><span class="sxs-lookup"><span data-stu-id="09cf9-110">The Wireless Hosted Network sample can be compiled on the Windows SDK for Windows 7.</span></span> <span data-ttu-id="09cf9-111">無線裝載的網路範例可以在已安裝無線局域網路服務的 Windows 7 和 Windows Server 2008 R2 上執行。</span><span class="sxs-lookup"><span data-stu-id="09cf9-111">The Wireless Hosted Network sample can be run on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span>

<span data-ttu-id="09cf9-112">在 Windows 7 上，以及安裝了無線局域網路服務的 Windows Server 2008 R2 上，如果電腦上有具備網路功能的無線介面卡，作業系統會安裝一個虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="09cf9-112">On Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine.</span></span> <span data-ttu-id="09cf9-113">如果電腦具有單一無線網路介面卡，此虛擬裝置通常會在 [網路連線] 資料夾中顯示為「無線網路連線2」，且裝置名稱為「Microsoft 虛擬 WiFi 微型網路介面卡」。</span><span class="sxs-lookup"><span data-stu-id="09cf9-113">This virtual device normally shows up in the "Network Connections Folder" as "Wireless Network Connection 2" with a Device Name of "Microsoft Virtual WiFi Miniport adapter" if the computer has a single wireless network adapter.</span></span> <span data-ttu-id="09cf9-114">此虛擬裝置專門用來執行軟體存取點 (SoftAP) 連接。</span><span class="sxs-lookup"><span data-stu-id="09cf9-114">This virtual device is used exclusively for performing software access point (SoftAP) connections.</span></span> <span data-ttu-id="09cf9-115">此虛擬裝置的存留期會系結至實體無線介面卡。</span><span class="sxs-lookup"><span data-stu-id="09cf9-115">The lifetime of this virtual device is tied to the physical wireless adapter.</span></span> <span data-ttu-id="09cf9-116">如果實體無線介面卡已停用，此虛擬裝置也會一併移除。</span><span class="sxs-lookup"><span data-stu-id="09cf9-116">If the physical wireless adapter is disabled, this virtual device will be removed as well.</span></span>

<span data-ttu-id="09cf9-117">無線裝載的網路功能可用來啟動和停止無線裝載的網路、設定或變更設定，或查詢資訊。</span><span class="sxs-lookup"><span data-stu-id="09cf9-117">The wireless Hosted Network functions are used to start and stop the wireless Hosted Network, configure or change settings, or query for information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09cf9-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="09cf9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09cf9-119">關於無線託管網路</span><span class="sxs-lookup"><span data-stu-id="09cf9-119">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="09cf9-120">使用託管網路和網際網路連線共用</span><span class="sxs-lookup"><span data-stu-id="09cf9-120">Using Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[<span data-ttu-id="09cf9-121">**WlanHostedNetworkForceStart**</span><span class="sxs-lookup"><span data-stu-id="09cf9-121">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[<span data-ttu-id="09cf9-122">**WlanHostedNetworkInitSettings**</span><span class="sxs-lookup"><span data-stu-id="09cf9-122">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[<span data-ttu-id="09cf9-123">**WlanHostedNetworkQueryProperty**</span><span class="sxs-lookup"><span data-stu-id="09cf9-123">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[<span data-ttu-id="09cf9-124">**WlanHostedNetworkQuerySecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="09cf9-124">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[<span data-ttu-id="09cf9-125">**WlanHostedNetworkQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="09cf9-125">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[<span data-ttu-id="09cf9-126">**WlanHostedNetworkRefreshSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="09cf9-126">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[<span data-ttu-id="09cf9-127">**WlanHostedNetworkSetProperty**</span><span class="sxs-lookup"><span data-stu-id="09cf9-127">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[<span data-ttu-id="09cf9-128">**WlanHostedNetworkSetSecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="09cf9-128">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[<span data-ttu-id="09cf9-129">**WlanHostedNetworkStartUsing**</span><span class="sxs-lookup"><span data-stu-id="09cf9-129">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[<span data-ttu-id="09cf9-130">**WlanHostedNetworkStopUsing**</span><span class="sxs-lookup"><span data-stu-id="09cf9-130">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[<span data-ttu-id="09cf9-131">**WlanRegisterVirtualStationNotification**</span><span class="sxs-lookup"><span data-stu-id="09cf9-131">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 




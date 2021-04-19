---
description: 示範基本無線網路管理功能的使用。
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: 原生 Wifi API 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993119"
---
# <a name="native-wifi-api-sample"></a><span data-ttu-id="6a677-103">原生 Wifi API 範例</span><span class="sxs-lookup"><span data-stu-id="6a677-103">Native Wifi API Sample</span></span>

<span data-ttu-id="6a677-104">示範如何使用基本無線網路管理功能的原生 Wifi API 範例，隨附于 Microsoft Windows 軟體開發套件 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="6a677-104">A Native Wifi API sample that demonstrates the use of basic wireless network management functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6a677-105">您可以從 [下載中心](https://developer.microsoft.com/windows/downloads)取得最新版本的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="6a677-105">The latest version of the Windows SDK is available from the [Download Center](https://developer.microsoft.com/windows/downloads).</span></span>

<span data-ttu-id="6a677-106">原生 Wifi 範例原始程式碼預設會安裝在下列目錄中：</span><span class="sxs-lookup"><span data-stu-id="6a677-106">By default, the Native Wifi sample source code is installed in the following directory:</span></span>

<span data-ttu-id="6a677-107">**C： \\ Program Files \\ Microsoft sdk \\ Windows \\ <version number> \\ 範例 \\ NetDs \\ Wlan**</span><span class="sxs-lookup"><span data-stu-id="6a677-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="6a677-108">原生 Wifi API 範例位於下列資料夾底下：</span><span class="sxs-lookup"><span data-stu-id="6a677-108">The Native Wifi API sample is located under the following folder:</span></span>

<span data-ttu-id="6a677-109">**wlan**</span><span class="sxs-lookup"><span data-stu-id="6a677-109">**autoconfig**</span></span>

<span data-ttu-id="6a677-110">原生 Wifi 範例可在 Windows Vista 和更新版本、windows XP Service Pack 3 (SP3) 和適用于 Windows XP Service Pack 2 (SP2) 的無線區域網路 API 上進行編譯和執行。</span><span class="sxs-lookup"><span data-stu-id="6a677-110">The Native Wifi sample can be compiled and run on Windows Vista and later, Windows XP with Service Pack 3 (SP3), and Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="6a677-111">Windows XP （含 SP3）和適用于 Windows XP SP2 的無線區域網路 API 不支援範例的部分功能。</span><span class="sxs-lookup"><span data-stu-id="6a677-111">Some features of the sample are not supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="6a677-112">如需 windows XP 含 SP3 以及適用于 Windows XP SP2 的無線區域網路 API 所支援的功能清單，請參閱 [WINDOWS xp 上的原生 WIFI Api 支援](about-wireless-lan-api-for-windows-xp-service-pack-2.md)。</span><span class="sxs-lookup"><span data-stu-id="6a677-112">For a list of functions supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, see [Native Wifi API Support on Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span></span>

<span data-ttu-id="6a677-113">原生 Wifi 範例會示範如何執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="6a677-113">The Native Wifi sample demonstrates how to perform the following tasks:</span></span>

-   <span data-ttu-id="6a677-114">列舉無線介面。</span><span class="sxs-lookup"><span data-stu-id="6a677-114">Enumerate wireless interfaces.</span></span> <span data-ttu-id="6a677-115">請參閱 [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)。</span><span class="sxs-lookup"><span data-stu-id="6a677-115">See [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span></span>
-   <span data-ttu-id="6a677-116">取得介面的功能。</span><span class="sxs-lookup"><span data-stu-id="6a677-116">Get the capabilities of an interface.</span></span> <span data-ttu-id="6a677-117">請參閱 [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability)。</span><span class="sxs-lookup"><span data-stu-id="6a677-117">See [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span></span>

    <span data-ttu-id="6a677-118">\* \* Windows XP 含 SP3 以及適用于 Windows XP SP2 的無線區域網路 API： \* \* 這項功能不受支援。</span><span class="sxs-lookup"><span data-stu-id="6a677-118">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* This feature is not supported.</span></span>

-   <span data-ttu-id="6a677-119">查詢介面。</span><span class="sxs-lookup"><span data-stu-id="6a677-119">Query an interface.</span></span> <span data-ttu-id="6a677-120">請參閱 [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)。</span><span class="sxs-lookup"><span data-stu-id="6a677-120">See [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span></span>
-   <span data-ttu-id="6a677-121">設定網路介面的參數。</span><span class="sxs-lookup"><span data-stu-id="6a677-121">Set parameters for a network interface.</span></span> <span data-ttu-id="6a677-122">請參閱 [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)。</span><span class="sxs-lookup"><span data-stu-id="6a677-122">See [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span></span> <span data-ttu-id="6a677-123">此功能可用來開啟和關閉無線無線電 (，因此可啟用或停用無線網路連線) 。</span><span class="sxs-lookup"><span data-stu-id="6a677-123">This function can be used to turn the wireless radio on and off (and therefore enable or disable wireless network connectivity).</span></span>
-   <span data-ttu-id="6a677-124">掃描可用的無線網路。</span><span class="sxs-lookup"><span data-stu-id="6a677-124">Scan for available wireless networks.</span></span> <span data-ttu-id="6a677-125">請參閱 [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)。</span><span class="sxs-lookup"><span data-stu-id="6a677-125">See [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span></span>
-   <span data-ttu-id="6a677-126">取得可用或可見無線網路的清單。</span><span class="sxs-lookup"><span data-stu-id="6a677-126">Get the list of available or visible wireless networks.</span></span> <span data-ttu-id="6a677-127">請參閱 [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)。</span><span class="sxs-lookup"><span data-stu-id="6a677-127">See [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span></span>
-   <span data-ttu-id="6a677-128">取得、儲存或刪除設定檔。</span><span class="sxs-lookup"><span data-stu-id="6a677-128">Get, save, or delete a profile.</span></span> <span data-ttu-id="6a677-129">請參閱 [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)、 [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)和 [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)。</span><span class="sxs-lookup"><span data-stu-id="6a677-129">See [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), and [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span></span>
-   <span data-ttu-id="6a677-130">連線到無線網路或中斷其連接。</span><span class="sxs-lookup"><span data-stu-id="6a677-130">Connect to or disconnect from a wireless network.</span></span> <span data-ttu-id="6a677-131">請參閱 [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) 和 [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)。</span><span class="sxs-lookup"><span data-stu-id="6a677-131">See [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) and [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a677-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="6a677-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a677-133">使用原生 Wifi</span><span class="sxs-lookup"><span data-stu-id="6a677-133">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="6a677-134">Windows Vista 無線 SDK 論壇</span><span class="sxs-lookup"><span data-stu-id="6a677-134">Windows Vista Wireless SDK Forum</span></span>](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

<span data-ttu-id="6a677-135">[針對 Windows Vista 802.11 無線連線進行疑難排解](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6a677-135">[Troubleshooting Windows Vista 802.11 Wireless Connections](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span></span>
</dt> </dl>

 

 

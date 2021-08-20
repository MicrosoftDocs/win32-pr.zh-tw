---
title: 使用無線託管網路、網際網路連線共用
description: 使用無線託管網路和網際網路連線共用
ms.assetid: 56e86ef8-f759-4e56-a591-74e03430125a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62103074cfa6e84ef764e506a724b17a4e2d770ec656f09d1200af21e463536f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984698"
---
# <a name="use-wireless-hosted-network-internet-connection-sharing"></a>使用無線託管網路、網際網路連線共用

無線託管網路是 Windows 7 和 Windows 8 支援的新 WLAN 功能。 在安裝了無線局域網路服務的 Windows Server 2012 和 Windows Server 2008 R2 上也支援此功能。 這項功能會實現兩個主要功能：

-   將實體無線介面卡虛擬化為一個以上的虛擬無線介面卡，有時又稱為虛擬 Wi-fi。
-   以軟體為基礎的無線存取點 (AP) 有時稱為 SoftAP，使用指定的虛擬無線介面卡。

網際網路連線共用 (ICS) 是透過 win2k3 sharedaccess 服務提供 Windows 中的一項功能。 嚴格來說，Win2k3 sharedaccess 透過共用網路存取不一定提供網際網路存取權的電腦，來啟用網路共用。 因為網際網路連線共用是無線裝載網路的主要案例，且使用者群體更知道 ICS 詞彙，所以我們會在本節中交替使用「ICS」和「Win2k3 sharedaccess」一詞。

無線裝載的網路緊密地系結至 ICS，讓無線個人區域網路 (平移) 和網際網路共用案例。 本節提供應用程式開發人員的一般建議，說明如何使用公用無線裝載網路和 ICS Api 來整合無線裝載的網路和 ICS。

## <a name="internet-connection-sharing"></a>網際網路連線共用

ICS 服務可在兩種可能的模式下運作：

-   獨立模式

    只有當叫用 ICS 服務時，才會操作 DHCPv4 伺服器功能。 這是適用于 ICS 的特殊操作模式，只能透過無線裝載的網路使用。 使用者或應用程式無法透過公用 ICS Api 或 **netsh** 命令直接啟動及停止獨立 ics。 啟動無線裝載的網路通常牽涉到以獨立模式啟動 ICS，以使用 DHCPv4 伺服器功能為連線的裝置提供私人 IPv4 位址。 連線裝置的網路通訊限制為在連線的裝置與裝載無線裝載網路的本機電腦之間，以及連線裝置本身之間傳送和接收網路封包。 這可有效地啟用無線裝載網路的無線個人區域網路案例。

-   完整模式

    當叫用服務時，ICS 的所有功能都是運作中的，例如 IPv4 與 IPv6 的網路位址轉譯和 DHCP 伺服器功能。 這是適用于 ICS 的正常操作模式。 使用者或應用程式可以透過公用 Api 或 netshell 命令來啟動和停止完整的 ICS 模式。 例如，您可以從提升許可權的命令提示字元使用 net stop win2k3 sharedaccess 來停止此服務。 將無線裝載的網路與完整的 ICS 結合，連接裝置的網路通訊不限於無線 PAN。 任何連線的裝置都可以存取網路 (例如，從執行無線裝載網路的電腦透過共用網路連線來) 網際網路。 這可有效地啟用無線託管網路的網路共用案例。

在本節中，我們會使用「完整 ICS」一詞來表示在 ICS 服務中叫用所有 ICS 功能的情況，以提供無線託管網路的所有完整 ICS 功能存取權。

這兩個 ICS 作業模式與具有較高優先順序的完整 ICS 相互排斥。 ICS 服務可以從獨立模式轉換為完整模式，但無法從完整模式轉換成獨立模式。 ICS 獨立模式是在 Windows 7 和 Windows Server 2008 R2 中引進，而且無線局域網路服務與無線裝載的網路功能一起安裝。 在舊版 Windows 中無法使用。

任何完整的 ICS 操作都牽涉到系統中的兩個不同網路介面卡：

-   公用介面。 這是可存取網際網路的網路介面。 這是執行 ICS 的本機電腦用來與透過 SoftAP 連接到它的用戶端和裝置共用網際網路的介面。
-   私用介面。 這是其他裝置用來連接到執行 ICS 之本機電腦的網路介面。 在此私人介面上執行的 DHCPv4 伺服器，可將私人本機 IP 位址提供給其他遠端電腦。

當公用介面沒有網際網路存取權時，私人介面上的 DHCP 伺服器會繼續提供本機 IP 位址給連線的裝置。 獨立 ICS 只牽涉到 SoftAP 執行所在的私用介面;它不包含任何公用介面。

在本機電腦上，最多隻會執行一個完整的 ICS 實例。 如果本機電腦上已有完整的 ICS 正在執行，則啟動另一個完整的 ICS 會出現下列功能行為：

-   如果新的完整 ICS 的公用和私用介面與現有的完整 ics 相同，則啟動第二個完整的 ICS 相當於無作業。
-   如果新的公用介面與舊的公用介面不同，但新的私用介面與舊的私用介面相同，則啟動第二個完整的 ICS 對相同私用介面上的連線裝置不會有很大的影響。 存取網際網路的能力可能會隨著新的公用介面而改變。
-   如果新的私用介面與舊的私用介面不同，ICS 函式將會停止使用舊的私用介面，並開始套用至新的私用介面。 使用舊的私人介面連接到本機電腦的任何遠端裝置，將會失去與本機電腦的 IP 連線能力。

當完整的 ICS 已在執行時，只要第二個 ICS 整合使用不同的新私用介面，叫用第二個完整的 ICS 將會干擾使用舊私用介面從遠端連線的裝置。

若要管理和使用 ICS 服務以支援與無線託管網路的 ICS 整合，軟體應用程式必須先取得 [**INetSharingManager**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager) 介面。 **INetSharingManager** 介面可讓您直接或間接存取 ICS API 中的所有其他 COM 介面。 **INetSharingManager** 介面上的 [**get \_ SharingInstalled**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_sharinginstalled)方法會報告本機電腦是否支援連接共用。 **INetSharingManager** 介面上的 [**get \_ EnumEveryConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection)方法會抓取連接資料夾中所有連接的列舉介面。 [**Get \_ INetSharingConfigurationForINetConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection)方法會抓取指定連接的 [**INetSharingConfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration)介面。 **INetSharingConfiguration** 介面上的方法可以用來查詢和變更 ICS 設定。

在呼叫 [**INetSharingManager**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager)介面上的 [**get \_ EnumEveryConnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection)方法之前，必須先啟動無線裝載的網路，以列舉 [連接] 資料夾中的所有連接。

如需有關可用來查詢及變更 ICS 設定之 ICS 和公用介面和方法的詳細資訊，請參閱 [有關網際網路連線共用和網際網路連線防火牆](/previous-versions/windows/desktop/ics/about-internet-connection-sharing-and-internet-connection-firewall)的檔。

## <a name="hosted-network-and-ics-integration"></a>Hosted Network and ICS 整合

當完整 ICS 未執行時，啟動無線裝載的網路也會在內部以獨立模式啟動 ICS 服務，只使用 DHCPv4 伺服器函式，為無線裝載網路介面上的連線裝置配置 IP 位址。 獨立的 DHCPv4 伺服器的子網位址範圍是 192.168.173.0/24。 這與搭配 full ICS 使用的 192.168.137.0/24 子網範圍不同。

使用 full ICS 啟動無線裝載的網路時，會採用下列邏輯：

-   如果完整的 ICS 尚未執行，則啟動無線裝載的網路也會啟動具有獨立 DHCPv4 伺服器的 ICS 服務。
-   如果完整的 ICS 已經在執行，而且私用介面是無線裝載的網路介面，只要啟動無線裝載的網路即可。
-   如果完整的 ICS 已經在執行，但私用介面不是無線裝載的網路介面，則無線裝載的網路將會啟動，而不需要在無線裝載的網路介面上執行 DHCPv4 伺服器功能。

上述邏輯的影響反白顯示下列事實：

-   ICS 不會從完整模式轉換成獨立模式。
-   只有當 ICS 未以完整模式執行時，無線裝載的網路才能叫用獨立模式。
-   如果 ICS 以獨立模式執行，則如果使用者或應用程式以完整模式啟動 ICS，它就會被搶先成為完整模式。
-   如果完整 ICS 的私用介面與 SoftAP 的私用介面不同，則在 ICS 中從獨立模式轉換成完整模式將會干擾無線 PAN 中的連線裝置。

在本機電腦上以完整或獨立模式啟動或停止 ICS 服務需要一些時間。 應用程式應該使用 **NotifyServiceStatusChange** 函式來檢查 ics 服務的狀態，以確定 ics 服務不是處於啟動/停止擱置狀態，然後才啟動或停止無線託管網路以與 ICS 整合搭配使用。

## <a name="starting-and-stopping-the-wireless-hosted-network"></a>啟動和停止無線託管網路

Windows 提供一個平臺，讓一個以上的並行應用程式可以同時管理無線裝載的網路。 具體而言，每個應用程式都可以自行啟動及停止無線裝載的網路，而不需要事先瞭解其他應用程式。

有兩組函式可以啟動和停止託管網路。

多個應用程式可能需要使用無線託管網路。 [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)和 [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)函式會啟動和停止無線裝載網路輸入與其他並行應用程式相容的方式。 **WlanHostedNetworkStartUsing** 和 **WlanHostedNetworkStopUsing** 函式可讓應用程式擁有無線託管網路的參考。 這項機制會讓無線裝載的網路維持執行狀態，前提是至少有一個其他應用程式具有無線裝載網路的目前參考。 任何使用者都可以呼叫這些函式。 成功呼叫 **WlanHostedNetworkStartUsing** 必須透過呼叫 **WlanHostedNetworkStopUsing** 函式來進行比對。 **WlanHostedNetworkStartUsing** 函式所造成的任何裝載網路狀態變更都會自動復原，因為呼叫端應用程式會使用傳遞至 **WlanHostedNetworkStartUsing**) 的相同 *hClientHandle* 參數來呼叫 WlanCloseHandle，或在進程結束時呼叫 [](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) ，藉以關閉其呼叫控制碼 (。

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)和 [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)函式會強制啟動及停止無線裝載的網路。 只有當使用者具有適當的提高許可權時，才可以呼叫這些函式。 **WlanHostedNetworkForceStart** 的成功呼叫最後可能會透過呼叫 **WlanHostedNetworkForceStop** 函式來比對，視應用程式設計而定。 這些函式會轉換無線裝載的網路狀態，而不會將要求與應用程式的呼叫控制碼產生關聯。 **WlanHostedNetworkForceStart** 函式所造成的任何裝載網路狀態變更將不會自動復原，因為呼叫端應用程式會使用傳遞至 [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)) 的相同 *hClientHandle* 參數來呼叫 WlanCloseHandle，或在進程結束時呼叫 [](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) ，以關閉其呼叫控制碼 (。 如果呼叫 **WlanHostedNetworkForceStart** 函式的應用程式在未呼叫其中一個函式的情況下關閉，以停止無線裝載的網路，則裝載的網路會保持執行狀態。 應用程式可能會在確定較高的系統使用者接受執行無線裝載網路所需的增加電源需求時，呼叫 **WlanHostedNetworkForceStart** 函式的時間延長一段時間。

要呼叫哪些函式來啟動及停止無線裝載網路的一般建議如下：

-   使用應用程式內的 [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) 和 [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) 函式來啟動及停止無線裝載的網路。
-   除非應用程式絕對需要，否則請勿使用 [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) 函式來啟動無線裝載網路。 **WlanHostedNetworkForceStart** 函式也需要較高的許可權。
-   只使用 [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) 函式做為修復方法。 **WlanHostedNetworkForceStop** 函式會導致無線託管網路立即停止。 其他接聽無線託管網路通知的應用程式可能需要採取修復動作。 如需詳細資訊，請參閱下面的討論，以瞭解無線託管網路的復原順序。

## <a name="start-sequence-for-wireless-hosted-network"></a>無線託管網路的開始順序

對於使用完整 ICS 啟動無線裝載網路的應用程式，建議您啟動無線裝載的網路，然後啟動完整的 ICS。 如果無線裝載的網路已在執行中，應用程式應該使用 [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) 函式，只有在需要完整 ICS 但未在啟動託管網路之前啟用時，才能使用函式來停止無線託管網路。 這可讓其他應用程式從完整 ICS 啟動所造成的潛在中斷中復原。 如需詳細資訊，請參閱下面的討論，以瞭解無線託管網路的復原順序。 合併作業應該會成功，並整體失敗。

> [!Note]  
> 在嘗試使用 [**IEnumNetSharingEveryConnection**](/windows/win32/api/netcon/nn-netcon-ienumnetsharingeveryconnection) 介面列舉對應的介面卡之前，必須先啟動無線託管網路。

 

以下是在使用具有完整 ICS 的無線託管網路的應用程式中，建議的起始順序：

-   呼叫 [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) 函式，以確定無線裝載的網路已設定且可供使用。
-   呼叫 [**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus) 和 [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty) 函式，以判斷是否允許和提供無線裝載的網路。 如果不允許無線裝載的網路且無法使用，則會傳回錯誤。
-   測試以查看是否允許針對完整 ICS 使用的 ICS 服務。 如果無法啟動 ICS 服務，則傳回錯誤。
-   呼叫 [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) 函式來強制停止無線裝載的網路。
-   呼叫 [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) 函式以啟動無線裝載的網路。
-   如果無線裝載的網路無法啟動，則會傳回錯誤。
-   如果完整的 ICS 已經在執行，而且目前的公用或私用介面與要使用的新介面不同，請快取目前的公用和私用介面。 如果已在執行 ICS 整合，應用程式也可以選擇傳回錯誤或提示使用者。
-   使用公用和私用介面的新設定來啟動完整的 ICS。
-   如果完整 ICS 無法以這些設定啟動，請嘗試使用快取的公用和私用介面啟動完整的 ICS 服務（如果已有完整的 ICS）。 呼叫 [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) 函式來停止無線裝載的網路，並傳回錯誤。
-   傳回無線裝載的網路與完整 ICS 成功的成功。

## <a name="stop-sequence-for-wireless-hosted-network"></a>無線託管網路的停止順序

使用具有完整 ICS 的無線託管網路時，已完成其工作的應用程式可能會想要停止無線裝載的網路，以及用於完整 ICS 的 ICS 服務。 在此情況下，建議呼叫 [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) 函式來停止裝載的網路，而不是呼叫 [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) 函數。 **WlanHostedNetworkForceStop** 函式會停止無線裝載的網路，也可讓其他應用程式復原。 如需詳細資訊，請參閱下面的討論，以瞭解無線託管網路的復原順序。

下列已排序的步驟是在使用無線裝載網路和完整 ICS 的應用程式中建議的停止順序：

-   停止完整 ICS。
-   呼叫 [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) 函式以停止無線裝載的網路。

使用無線裝載網路的應用程式（沒有完整的 ICS）已完成其工作，只需要呼叫 [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) 或 [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) 函式來停止無線裝載的網路。 如果呼叫 [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) 函式來啟動無線裝載的網路，則應用程式應該呼叫 **WlanHostedNetworkStopUsing** 函式來停止無線裝載的網路。 如果無線裝載的網路在應用程式或呼叫 [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) 函式來強制啟動無線裝載網路之前已啟動，則應用程式可以呼叫 **WlanHostedNetworkForceStop** 函式來停止無線裝載的網路，或不執行任何動作 (讓無線裝載的網路) 啟動，視案例而定。

## <a name="recovery-sequence-for-wireless-hosted-network"></a>無線託管網路的復原順序

使用無線託管網路的應用程式可能會受到其他應用程式的動作影響。 ICS 服務和用於管理 ICS 的介面不提供任何方法讓應用程式註冊 ICS 變更通知。 如果另一個應用程式呼叫 [**INetSharingConfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration)介面上的 [**EnableSharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-enablesharing)或 [**DisableSharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-disablesharing)方法來啟用或停用連接上的共用，則會將訊息傳送至使用者介面， (本機電腦上的螢幕) 不是其他應用程式。 如此一來，應用程式就必須依賴無線裝載的網路通知，以在發生 ICS 或無線裝載的網路變更時執行修復動作。

使用無線裝載網路的應用程式應該呼叫 [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)，以註冊無線裝載的網路通知。 如果只需要無線裝載網路的通知，應用程式應該在傳遞至 **WlanRegisterNotification** 的 *dwNotifSource* 參數中傳遞 **WLAN \_ 通知 \_ 來源 \_ HNWK** 。 如果也需要其他無線 gcm，則應該將 [ **WLAN \_ 通知 \_ 來源 \_ HNWK** ] 與其他所需的無線通知類型的通知來源常數結合，並在 *dwNotifSource* 參數中傳遞此值。

如果應用程式不想再次啟動 ICS 服務，則具有或不含完整 ICS 的應用程式復原順序會相同。 收到託管網路已停止的無線託管網路通知時，請執行下列動作：

-   如果名為 [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) 的應用程式啟動無線裝載的網路，則呼叫 **WlanHostedNetworkForceStart** 以重新開機託管的網路。 否則，請呼叫 [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) 以重新開機無線裝載的網路。

## <a name="recovery-sequence-for-connected-devices"></a>已連線裝置的復原順序

遠端裝置或連線到無線裝載網路的電腦，可能會受到影響 ICS 和無線裝載網路之其他應用程式的動作所影響。 幸運的是，大部分的裝置在裝置應用程式中都有內建的重試邏輯，以處理暫時遺失的信號或漫遊。

如果裝置或電腦連線到無線裝載網路而失去聯繫，則可能的復原順序如下所示：

-   無線設備磁碟機表示媒體中斷連線至裝置上網路堆疊的上層。
-   裝置應用程式會定期檢查無線託管網路的可用性。
-   一旦裝置應用程式再次偵測到無線裝載的網路，裝置就會起始無線連線。
-   成功連線到無線託管網路時，裝置應用程式會據以更新其 IP 設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於無線託管網路](about-the-wireless-hosted-network.md)
</dt> <dt>

[無線託管網路範例](wireless-hosted-network-sample.md)
</dt> <dt>

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 

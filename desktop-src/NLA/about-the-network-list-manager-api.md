---
title: 關於網路清單管理員 API
description: 關於網路清單管理員 API
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675259"
---
# <a name="about-the-network-list-manager-api"></a>關於網路清單管理員 API

Microsoft Windows 網路環境可讓多重主目錄電腦同時連線到多個網路。 可能有多個無線網路可用，以及區域網路和撥號連線。 網路清單管理員會識別可用的網路，並將網路屬性資料傳回給應用程式。

網路清單管理員 API 會與網路清單管理員服務互動，以找出並抓取電腦所連線之每個網路的屬性。 每個網路都會使用網路簽章來唯一識別，並以該網路的可唯一識別屬性為基礎。 當應用程式註冊網路清單管理員通知時，應用程式會收到新網路連線可用性或現有網路連線變更的相關通知。 應用程式可以根據下列程式來調整其邏輯：它們所連線的網路：它們所連線的網路連接;或網路屬性的內容。 透過此資訊，應用程式可以根據目前的網路狀況微調其動作

Windows Vista 引進了新的介面，可用來取得這些網路特性及更多的詳細資訊。 有了 [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) 介面，您就可以輕鬆地列舉所有網路 ([**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) 電腦上的所有網路，或只是連線的網路，或只是已中斷連線的網路。 **INetworkListManager** 介面也可讓您輕鬆地列舉電腦上的網路介面。

[**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)介面是用來判斷網路連線的屬性：名稱、描述、識別碼、受管理/已驗證、連線/中斷連線等等。 單一網路可能會連接到數個介面，因此透過 **INetwork** 介面，您也可以列舉正在使用之 **INetwork** 介面的實例。

[**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)介面會告訴您介面的相關屬性：識別碼、GUID、類型 (受控、已驗證的) ，以及狀態 (連線、中斷連線、V4 本機、V4 網際網路、v6 本機、v6 網際網路) 。 V4 區域表示第四版網際網路協定 (IPv4) 本機存取。 V4 網際網路指的是 IPv4 與網際網路的存取。 V6 本機和 V6 網際網路平均 IPv6。

網路位置的物件樹狀結構根目錄是 [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) 介面。 此介面會在 **CLSID \_ NetworkListManager** coclass 上執行。 若要使用此介面，您必須建立 NetworkListManager COM 物件的 **CLSID \_** ，如下所示：


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 





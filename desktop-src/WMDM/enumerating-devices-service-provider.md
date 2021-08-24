---
title: " (WMDM) 列舉裝置"
description: Windows媒體裝置管理員會維護已連線裝置的快取。 瞭解 Windows 媒體裝置管理員如何維護或更新其快取。
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows媒體裝置管理員，列舉裝置
- 裝置管理員，列舉裝置
- 程式設計指南，列舉裝置
- 服務提供者，列舉裝置
- 建立服務提供者，列舉裝置
- 列舉裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500375f01e718ab6f9824868ffabd7c83e11c3e812ce0288f0c15186bc1d2de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767048"
---
# <a name="enumerating-devices-wmdm"></a> (WMDM) 列舉裝置

Windows媒體裝置管理員會維護已連線裝置的快取，當 Windows 媒體裝置管理員應用程式啟動、隨插即用 (PnP) 裝置連線或中斷連線，或應用程式呼叫 [**IWMDeviceManager2：：重新初始化**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize)時，就會更新這些裝置。 當應用程式呼叫 [**IWMDeviceManager：： EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) 或 [**IWMDeviceManager2：： EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2)時，此快取會公開給應用程式。 每個裝置都會以 [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) 介面的形式公開給應用程式。 如果已註冊服務提供者來處理 PnP 裝置，Windows 媒體裝置管理員將會察覺目前連線的裝置清單。 如果服務提供者已註冊來處理非 PnP 裝置，則服務提供者負責探索連接的裝置。 服務提供者只能針對 PnP 或非 PnP 裝置註冊，且不能同時註冊。

下列動作顯示 Windows 媒體裝置管理員如何維護或更新其快取。 請注意，當非 PnP 裝置連接或中斷連線時，快取永遠不會更新。

Windows 媒體裝置管理員應用程式啟動

-   Windows媒體裝置管理員從 PnP 子系統抓取附加的 PnP 裝置清單，並在為每個連線裝置註冊的 SP 上呼叫 [**IMDServiceProvider2：： CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) 。  (它會藉由查詢負責此裝置之服務提供者類別識別碼的 WMDMSPCLSID 裝置參數，來探索正確的服務提供者。 如需詳細資訊，請參閱[裝置參數](device-parameters.md)。 ) 所有傳回的裝置都會新增至 Windows 媒體裝置管理員快取裝置。
-   Windows媒體裝置管理員會尋找所有註冊的非 PnP 服務提供者，並在每個服務提供者上呼叫 [**IMDServiceProvider：： EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) ，以取得每個服務提供者的清單裝置。 所有傳回的裝置都會新增至快取。

應用程式會呼叫 IWMDeviceManager/2：： EnumDevices/2

-   WindowsMedia 裝置管理員會傳回其快取的裝置清單。

PnP 裝置連接

-   Windows媒體裝置管理員會尋找相關的服務提供者並呼叫 **IMDServiceProvider2：： CreateDevice**，並將裝置新增至其快取。
-   如果應用程式會執行 [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)，Windows Media 裝置管理員就會呼叫 [**IWMDMNotification：： WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage)與抵達通知。

PnP 裝置中斷連線

-   Windows媒體裝置管理員從其快取中移除專案。
-   如果應用程式會執行 IWMDMNotification，Windows Media 裝置管理員會呼叫 IWMDMNotification：： WMDMMessage 與起飛通知。

應用程式會呼叫 IWMDeviceManager2：：重新初始化

-   重新整理所有已連線裝置的快取。

非 PnP 裝置連接或中斷連線

-   Windows媒體裝置管理員不會收到抵達或離職的通知，也不會採取任何動作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立服務提供者**](creating-a-service-provider.md)
</dt> </dl>

 

 





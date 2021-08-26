---
title: 關於合作關係
description: 關於合作關係
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player，合作關係
- Windows Media Player 物件模型，合作關係
- 物件模型，合作關係
- Windows Media Player ActiveX 控制，合作關係
- ActiveX 控制，合作關係
- Windows Media PlayerMobile ActiveX 控制，合作關係
- Windows Media Player行動、合作關係
- 同步處理裝置，合作關係
- 裝置同步處理，合作關係
- 裝置與 Windows Media Player 之間的合作關係
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c018934ed06e5872d5866a463bdd909ea2501a1872ded29231be222572b2ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004488"
---
# <a name="about-partnerships"></a>關於合作關係

合作關係是可攜式裝置與 Windows Media Player 之間的特殊關聯性。 使用者可以使用 Windows Media Player 使用者介面，建立特定裝置的合作關係。 您可以使用 [IWMPSyncDevice：： createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) 和 [IWMPSyncDevice：:d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership)，以程式設計方式管理合作關係。 **CreatePartnership** 方法會啟動非同步進程，該進程會在透過 **IWMPEvents2** 介面收到 **CreatePartnershipComplete** 事件時結束。

Windows Media Player 10 或更新版本支援建立與最多16部裝置的合作關係。 每個合作關係都有相關聯的合作關係索引。 您可以藉由呼叫 [IWMPSyncDevice：： get \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)，來取得特定裝置的合作關係索引。 合作關係索引的編號是從1到16。 當特定裝置與 Windows Media Player 沒有合作關係時， **getPartnershipIndex** 會針對索引傳回零。

您可以藉由呼叫 [IWMPSyncDevice：： get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) ，然後檢查已抓取的 [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) 值，來取得特定裝置的合作關係狀態。 Windows Media Player 可讓每個裝置在一部電腦上有一個使用者的程式庫合作。 這表示建立新的合作關係會終結目前裝置可能與另一部電腦之間的任何現有合作關係。 若要知道裝置狀態變更的時間，您可以接收 **DeviceStatusChange** 事件。

Windows Media Player 無法與狀態為 **wmpdsManualDevice** 的裝置建立合作關係。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於裝置同步處理**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**使用可攜式裝置**](working-with-portable-devices.md)
</dt> </dl>

 

 





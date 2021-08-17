---
title: 關於裝置
description: 關於裝置
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Windows Media Player，同步處理裝置
- Windows Media Player 物件模型，同步處理裝置
- 物件模型，同步處理裝置
- Windows Media Player ActiveX 控制，同步處理裝置
- ActiveX 控制，同步處理裝置
- Windows Media Player行動 ActiveX 控制，同步處理裝置
- Windows Media Player行動裝置，同步處理裝置
- 正在同步處理裝置，關於
- 裝置同步處理，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66383082bae772b48f913f6bd4615724de8f7b7735e387ba93407a9848f17074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956918"
---
# <a name="about-devices"></a>關於裝置

可攜式裝置是一種硬體裝置，當使用者離開電腦時，使用者就能享受數位媒體內容。 通常，可攜式裝置是以電池運作。 有些裝置只能播放音樂。 其他裝置可以播放影片和音樂。

某些裝置支援自動同步處理數位媒體內容與 Windows Media Player。 其他裝置僅支援手動傳送。 您可以藉由呼叫 [IWMPSyncDevice：： get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) ，然後檢查已抓取的 [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) 值，來判斷特定裝置是否支援自動同步處理。 如果取出的值是 **wmpdsManualDevice**，則裝置不支援自動同步處理。

您可以列舉連接到使用者電腦的裝置。 若要這樣做，請先使用 [IWMPSyncServices：： get \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) 取得裝置計數。 然後，在迴圈中呼叫 [IWMPSyncServices：： getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice)，每次傳遞適當的索引值。 您可以使用 [IWMPSyncDevice：： get \_ connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) 來評估特定裝置目前是否已連接。

若要知道裝置連接或中斷連線的時間，您可以接收 **>deviceconnect** 和 **DeviceDisconnect** 事件。 這些事件會透過 **IWMPEvents2** 介面接收。

**IWMPSyncDevice** 介面提供了其他方法，可讓您取得或設定裝置的相關資訊。 例如：

-   **取得 \_ friendlyname** 和 **put \_ friendlyname** 方法可讓您取得並指定使用者定義的裝置名稱。
-   **get \_ deviceName** 方法可讓您取得使用者在 Windows XP shell 中看到的裝置名稱。
-   **GetItemInfo** 方法可讓您從裝置取得中繼資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於裝置同步處理**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**IWMPSyncDevice 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**使用可攜式裝置**](working-with-portable-devices.md)
</dt> </dl>

 

 





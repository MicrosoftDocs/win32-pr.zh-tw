---
title: 關於同步處理引擎
description: 關於同步處理引擎
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player，同步處理引擎
- Windows Media Player 物件模型，同步處理引擎
- 物件模型，同步處理引擎
- Windows Media Player ActiveX 控制，同步處理引擎
- ActiveX 控制項，同步處理引擎
- Windows Media PlayerMobile ActiveX control，同步處理引擎
- Windows Media Player行動，同步處理引擎
- 同步處理裝置，同步處理引擎
- 裝置同步處理，同步處理引擎
- 同步處理引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ccac14f6416b080ae22407930d720df84bd5b4dc399892b9a2d8678d03eee6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903068"
---
# <a name="about-the-synchronization-engine"></a>關於同步處理引擎

同步處理引擎是管理將數位媒體內容複寫到可攜式裝置的 Windows Media Player 元件。 Windows Media Player 支援每個裝置的單一同步處理引擎實例。 您必須使用 Windows Media Player 控制項的遠端實例，以程式設計的方式執行同步處理工作。 實際上，您的程式會與 Windows Media Player 以及使用播放程式介面進行裝置同步處理的所有其他程式共用同步處理引擎實例。

您可以使用 [IWMPSyncDevice：： start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) 和 [IWMPSyncDevice：： stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) 來控制同步處理引擎執行其工作的時間。 在大多數情況下，您不應該使用這些方法。 相反地，您應該讓同步處理引擎自動排程其工作。 如果您的程式是設計來取代 Windows Media Player 的使用者介面，則會有 **start** 和 **stop** 方法，因此您可以使用這些方法。 在此情況下，您可能會想要提供與 [**裝置**] 索引標籤中所提供的 [啟動/停止] 按鈕類似的 Windows Media Player。

您可以藉由輪詢 [IWMPSyncDevice：： get \_ 進度](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)來監視裝置的同步處理進度。 這個方法會使用特定裝置來抓取整個同步處理常式的進度值。 抓取的值是代表同步處理完成百分比的數位。 您可以接收與同步處理相關的兩個事件。 **DeviceSyncError** 事件會在發生問題時通知您。 當同步處理引擎變更目前裝置的狀態時， **DeviceSyncStateChange** 事件會發出警示。

您可以藉由呼叫 [IWMPSyncDevice2：： setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo)與 **PercentSpaceReserved** 屬性，限制 Windows Media Player 用於同步處理的裝置儲存空間量。 使用這個介面需要 Windows Media Player 11。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於裝置同步處理**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**顯示同步處理進度**](showing-synchronization-progress.md)
</dt> </dl>

 

 





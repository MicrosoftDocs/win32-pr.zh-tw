---
description: 系統電源管理事件是系統電源狀態的變更、裝置或系統的操作模式，或是電源設定的值。
ms.assetid: f73b072a-1f69-4e26-9712-dab428edca18
title: 系統電源管理事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0558dfe0c846c6b48125a382d14f03181d7f18fb2d11deb4783af975e57c4cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032928"
---
# <a name="system-power-management-events"></a>系統電源管理事件

系統電源管理事件是系統電源狀態的變更、裝置或系統的操作模式，或是電源設定的值。 因為這些事件可能會影響應用程式和可安裝驅動程式的操作，所以系統會廣播每個事件的通知，以通知所有應用程式和可安裝的驅動程式。 應用程式和服務會使用 [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) 函數來註冊通知。 通知是透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收，其中包含電源管理事件和任何相關聯的事件特定資料。

## <a name="system-power-status-events"></a>系統電源狀態事件

電源供應器或系統電池狀態發生變更時，就會發生 *系統電源狀態事件* 。 例如，每當使用者從電池切換至 AC 電源時，系統就會廣播 [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) 事件，反之亦然。 當剩餘電池的電力下滑至使用者所指定的臨界值之下，或是如果電池的電力由指定百分比來變更時，系統也會廣播這個事件。

## <a name="operational-mode-events"></a>操作模式事件

當耗電量有所變更時，例如系統因為閒置而切換到睡眠狀態，或是使用者手動讓系統進入睡眠狀態時，就會發生 *操作模式事件* 。 系統會在進行耗電量的變更之前，先將這些變更的相關事件廣播。 例如，如果系統判斷它處於閒置狀態，它就會廣播 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件，通知應用程式和驅動程式即將暫停操作和睡眠，以節省電力。 應用程式和驅動程式可以藉由關閉檔案並儲存資料來準備睡眠，以避免潛在的資料遺失。

當系統執行 *重要* 的暫止時，系統會立即進入睡眠狀態，因為有重大的狀況，例如嚴重的電池警報。 相較于一般睡眠轉換，系統不會在執行重大暫停之前通知應用程式和驅動程式。 因此，應用程式必須準備好處理重要的暫停。

當系統作業在暫止之後還原時，系統會通知所有的應用程式和驅動程式。 它也會指出系統是否正在從重大暫停中繼續，讓應用程式或驅動程式可以採取適當的步驟來還原其資料，並繼續操作。

應用程式應該在不需要使用者介入的情況下，每次嘗試處理轉換進入睡眠狀態，因為使用者可能無法回應。 例如，筆記本電腦上的蓋可能會關閉。 當應用程式收到系統即將進入睡眠狀態的通知時，它應該會快速執行任何必要的作業，並傳回訊息迴圈。 系統在處理此訊息前，每個應用程式最多允許2秒的時間。

## <a name="power-setting-change-events"></a>電源設定變更事件

當電源設定的值有所變更時，就會發生電源設定變更事件。 例如，使用者在主控台的電源選項應用程式中，將電源計劃從高效能變更為平衡。 在此情況下，系統會廣播指出電源計劃已變更的事件。 此事件包含電源設定的新值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於電源管理](about-power-management.md)
</dt> </dl>

 

 




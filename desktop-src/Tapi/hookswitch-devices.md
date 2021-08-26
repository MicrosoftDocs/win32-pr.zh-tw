---
description: 電話裝置可以有多個 hookswitch 裝置。
ms.assetid: 39e3f24d-55d8-4830-8599-383954c8a107
title: Hookswitch 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ca5c9f605731780068b9ad5a5b35d913213006c62d127e6a3b15d1ffc5fe1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013098"
---
# <a name="hookswitch-devices"></a>Hookswitch 裝置

電話裝置可以有多個 hookswitch 裝置。 Hookswitch 是連接或中斷裝置與電話線連線的交換器。 例如，在電話上，當使用者從底座中提起接收器以取得新的撥號音時，就會自動啟用此參數。 TAPI 為電話定義三種類型的 hookswitch 裝置：話筒、話筒和耳機。 每個 hookswitch 裝置都有一個喇叭和一個麥克風元件，並以四種 hookswitch 模式的其中一種運作：

-   **Onhook** Hookswitch 裝置是 onhook，而且其麥克風和喇叭都已停用。
-   **僅限麥克風** Hookswitch 裝置為 offhook、其麥克風已啟用，且其喇叭為靜音。
-   **僅限說話者** Hookswitch 裝置是 offhook，其麥克風為靜音，並已啟用其喇叭。
-   **麥克風和喇叭** Hookswitch 裝置是 offhook，而且會啟用麥克風和喇叭。

[**PhoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch)函式是用來設定一或多個開啟的電話裝置 hookswitch 裝置的 hookswitch 模式。 例如，若要將 hookswitch 裝置的麥克風或喇叭元件靜音或取消靜音，請使用 **phoneSetHookSwitch** 搭配適當的 hookswitch 模式。 [**PhoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch)函式可用來查詢 open phone 裝置之 hookswitch 裝置的 hookswitch 模式。

以手動方式變更手機 hookswitch 裝置的模式時（例如從其底座中取出話筒），會將 [**電話 \_ 狀態**](phone-state.md) 消息傳送至應用程式，以通知應用程式狀態變更。 此訊息的參數提供了變更的指示。

Hookswitch 裝置的喇叭元件數量可以使用 [**phoneSetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume)來設定。 音量設定不同于靜音的喇叭和更新版本靜音它會保留喇叭的音量設定。 [**PhoneGetVolume**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume)函式可用來傳回開啟的電話裝置之 hookswitch 裝置喇叭的目前磁片區設定。

Hookswitch 裝置的麥克風元件也可以獲得控制。 [增益] 設定不同于靜音的麥克風和後續靜音它將會保留麥克風的 [增益] 設定。 使用 [**phoneSetGain**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) 來設定 hookswitch 裝置麥克風的 open phone 裝置，並使用 [**phoneGetGain**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) 來傳回已開啟之手機的 hookswitch 裝置麥克風增益設定。

當行動電話的音量或增益變更時， \_ 就會將電話狀態訊息傳送至應用程式函式，以通知應用程式狀態變更。 此訊息的參數提供了變更的指示。

 

 




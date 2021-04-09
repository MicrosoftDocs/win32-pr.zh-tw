---
title: 控制裝置
description: 以 UPnP 為基礎的裝置是由其公開的服務所控制。
ms.assetid: 4edca439-f767-41e6-97bb-ead751930714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a72a4ffdf91bca358124dbb0a0d95ff9a61e30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840532"
---
# <a name="controlling-devices"></a>控制裝置

以 UPnP 為基礎的裝置是由其公開的服務所控制。 UPnP 服務是 UPnP 架構中最小的可控制實體。 裝置會針對其執行的每個主要功能公開一個服務。 複雜裝置通常是由數個簡單的服務和其他裝置所組成。

服務包含一組狀態變數和一組動作，可讓應用程式在這些狀態變數上運作。 在具有 UPnP 技術的控制點 API 中，服務會以公開 [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)介面的 **服務** 物件來表示。

服務類型會定義特定服務所支援的狀態變數和動作。 例如，時鐘服務的服務類型會定義 **GetTime** 和 **SetTime** 動作，以及 **時間** 狀態變數。

服務識別碼會區分單一裝置內的多個常見服務類型。 例如，警示時鐘中可以有兩個時鐘服務，一個用於正常時鐘，另一個用於警示。 需要有一種方式來區別兩個具有相同服務類型的服務。 服務識別碼提供唯一的方法來識別服務類型的實例。 然後，此服務識別碼會用來從 [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) 集合存取正確的服務，因為服務類型不是唯一的識別碼。 [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)介面也可讓應用程式向服務物件註冊回呼函數。 當服務的狀態變數值變更時，服務物件會叫用已註冊的回呼，以通知應用程式變更。 UPnP 架構也會叫用此回呼，以在服務實例變成無法使用時通知應用程式。 服務可能因各種原因而變成無法使用，包括暫時性的網路失敗。

如需詳細資訊，請參閱下列主題：

-   [取得服務物件](obtaining-service-objects.md)
-   [註冊回呼](registering-a-callback.md)
-   [查詢狀態變數](querying-state-variables.md)
-   [叫用動作](invoking-actions.md)

 

 





---
title: 裝置提供者
description: 裝置提供者是電腦在每次系統啟動時啟動的註冊物件。
ms.assetid: 80c08993-0a8b-4ee9-93cd-bcc3c00e843b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fac270342830045fc3bac9f0573f283d87dc6a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092787"
---
# <a name="device-providers"></a>裝置提供者

裝置提供者是電腦在每次系統啟動時啟動的註冊物件。 裝置提供者會向裝置主機註冊及取消註冊執行中的裝置，以回應某個事件。 這些裝置是系統啟動時自動啟動的裝置。 基於安全性理由，裝置提供者通常會以 [LocalService](/windows/desktop/Services/localservice-account)的形式執行，而不是 [LocalSystem](/windows/desktop/Services/localsystem-account)。

裝置提供者可用於暫時性裝置。 裝置提供者也可以用來將裝置橋接到輪詢的媒體。 例如，像是數位音樂播放機的周邊裝置，會透過序列埠連接到電腦。 若要以 UPnP 型裝置的形式公開音樂播放機，則需要裝置控制物件和一組服務物件。 這些物件會以序列命令的形式來執行以 UPnP 為基礎的音樂播放機動作。 不過，在註冊這些物件之前，必須先將音樂播放機插入序列埠，並可進行控制。

由於序列埠在裝置連線時不會提供明確的通知機制，因此需要輪詢程式碼。 此程式碼可以在裝置提供者物件、服務或獨立應用程式中執行。 當電腦啟動時，裝置主機會將裝置提供者物件具現化，然後再叫用其 [**Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) 方法。 當裝置提供者偵測到有音樂播放機裝置時，它會具現化適當的裝置控制物件，並藉由呼叫 [**IUPnPRegistrar：： RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)來註冊它。 此方法會發佈裝置，並將其發佈至以 UPnP 為基礎的網路。

您也可以藉由執行輪詢序列埠的服務來達成相同的功能。 不過，裝置提供者只需要執行核心功能（輪詢）來簡化專案，因為裝置提供者依賴裝置主機來啟動和停止它們。 使用裝置提供者比執行服務更簡單。

在註冊期間，以及每次後續的系統啟動時，電腦會將裝置提供者物件具現化，然後再叫用其 [**IUPnPDeviceProvider：： Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) 方法，並將註冊期間指定的初始化字串傳遞給它。

一旦呼叫 [**Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) 方法，裝置提供者會執行任何必要的處理，並在必要時，藉由呼叫 [**IUPnPRegistrar：： RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)來註冊裝置，如向 [裝置主機註冊託管裝置](registering-a-hosted-device-with-the-device-host.md)一節中所述。

當電腦關機時，裝置主機會叫用 [**IUPnPDeviceProvider：： Stop**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-stop) 方法，以指出裝置提供者終止其作業。

 

 
---
title: 如何向裝置主機註冊裝置
description: 您可以註冊正在執行的裝置或非執行中的裝置。
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8425578dbd5ccc76685c2a142bee8d2167c4058341c32e4b03bcedca15041579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867578"
---
# <a name="how-to-register-a-device-with-the-device-host"></a>如何向裝置主機註冊裝置

您可以註冊正在執行的裝置或非執行中的裝置。

## <a name="registering-a-running-device"></a>註冊正在執行的裝置

裝置是使用 [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) 介面註冊的。 只有系統管理員才可以註冊執行中的裝置。 若要註冊具有正在執行之裝置控制物件的裝置，應用程式必須叫用 [**IUPnPRegistrar：： RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)，並傳遞下列各項：

-   裝置描述的文字。
-   裝置控制物件的 **IUnknown** 指標。
-   傳遞至裝置控制項物件之 [**IUPnPDeviceControl：： Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) 方法的初始化字串。
-   資原始目錄的位置。
-   裝置的存留期。
-   裝置識別碼參數 (OUT 參數) ，也就是此呼叫的傳回值;在 c + + 中會傳回裝置識別碼的指標。

## <a name="registering-a-non-running-device"></a>註冊非執行中的裝置

依預設，只允許系統管理員和互動式使用者註冊非執行中的裝置。 若要向未執行的裝置控制項物件註冊裝置，應用程式會使用 [**IUPnPRegistrar：： >registerdevice.js**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) 方法。

若要以程式設計方式向未執行的裝置控制物件註冊裝置，應用程式必須叫用 [**IUPnPRegistrar：： >registerdevice.js**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) ，並將下列參數傳遞給它：

-   裝置描述的文字。
-   裝置控制物件的 ProgID。
-   傳遞至裝置控制項物件之 [**IUPnPDeviceControl：： Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) 方法的初始化字串。
-   容器識別碼。
-   資原始目錄的位置。
-   裝置的存留期。
-   裝置識別碼參數 (OUT 參數) ，也就是此呼叫的傳回值;在 c + + 中會傳回裝置識別碼的指標。

未執行裝置的註冊可設定為跨系統開機， (在關閉階段) 期間未發佈裝置。 因此，如果以這種方式設定，則會在每次電腦開機時發佈並宣告裝置。

 

 





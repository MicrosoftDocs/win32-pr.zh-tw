---
title: Difxapi.h
description: 本節包含 Difxapi 標頭的參考主題。
ms.assetid: 84da7e54-0677-495e-9dc5-aca4ac12c0b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c549ed3fd781d9fde4e6ab48703e1df425986d0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186006"
---
# <a name="difxapih"></a>Difxapi.h

本節包含 Difxapi 標頭的參考主題。

## <a name="in-this-section"></a>本節內容



| 主題                                                                 | 描述                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*DIFLOGCALLBACK*](/previous-versions/windows/hardware/difxapi/diflogcallback)<br/>                     | **DIFLOGCALLBACK** 型別函式是應用程式提供的回呼函式，應用程式會呼叫 [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback)來註冊它。 DIFxAPI 會呼叫回呼函式，以記錄在 DIFxAPI 作業期間發生的事件。<br/>                        |
| [*DIFXAPILOGCALLBACK*](/previous-versions/windows/hardware/difxapi/difxapilogcallback)<br/>             | **DIFXAPILOGCALLBACK** 型別函式是應用程式提供的回呼函式，可讓應用程式藉由呼叫 [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback)向 DIFxAPI 註冊。 DIFxAPI 會呼叫回呼函式，以記錄在 DIFxAPI 作業期間發生的事件。<br/> |
| [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback)<br/>     | **DIFXAPISetLogCallback** 函式會註冊呼叫端提供的回呼函式，此函式會 DIFxAPI 呼叫，以記錄有關 DIFxAPI 作業期間發生之事件的記錄資訊。 <br/>                                                                                                            |
| [**DriverPackageGetPath**](/previous-versions/windows/hardware/difxapi/driverpackagegetpath)<br/>       | **DriverPackageGetPath** 函式會為預先安裝的 [驅動程式套件](/windows-hardware/drivers/install/driver-packages)抓取 [INF](/windows-hardware/drivers/install/overview-of-inf-files)檔案的完整路徑。<br/>                                                                                                               |
| [**DriverPackageInstall**](/previous-versions/windows/hardware/difxapi/driverpackageinstall)<br/>       | **DriverPackageInstall** 函數會預先安裝 [驅動程式套件](/windows-hardware/drivers/install/driver-packages)，然後在系統中安裝驅動程式。<br/>                                                                                                                                                 |
| [**DriverPackagePreinstall**](/previous-versions/windows/hardware/difxapi/driverpackagepreinstall)<br/> | **DriverPackagePreinstall** 函式會預先安裝隨插即用 (PnP) 函式 [驅動程式](/windows-hardware/drivers/kernel/function-drivers)的 [驅動程式套件](/windows-hardware/drivers/install/driver-packages)，並在系統 INF 檔案目錄中安裝驅動程式套件的 [INF](/windows-hardware/drivers/install/overview-of-inf-files)檔案。<br/>             |
| [**DriverPackageUninstall**](/previous-versions/windows/hardware/difxapi/driverpackageuninstall)<br/>   | **DriverPackageUninstall** 函式會從系統卸載指定的 [驅動程式套件](/windows-hardware/drivers/install/driver-packages)，並移除驅動程式套件。 <br/>                                                                                                                               |
| [**INSTALLERINFO**](/previous-versions/windows/hardware/difxapi/installerinfo)<br/>                     | INSTALLERINFO 結構包含 DIFxAPI 與 [驅動程式套件](/windows-hardware/drivers/install/driver-packages)相關聯之應用程式的相關資訊。 <br/>                                                                                                                                          |
| [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback)<br/>           | **SetDifxLogCallback** 函式會註冊呼叫端提供的回呼函式，此函式會 DIFxAPI 呼叫，以記錄有關 DIFxAPI 作業期間發生之事件的記錄資訊。 <br/>                                                                                                               |



 

 

 

[將關於本主題的意見傳送給 Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Difxapi.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "將關於本主題的意見傳送給 Microsoft")
---
description: 下列函式會在 Ws232.dll 中執行，並可供在 \_ 電腦上安裝 Windows 通訊端傳輸和命名空間服務提供者的應用程式使用。
ms.assetid: 3289737a-77b6-45d1-9c0a-3ed05b3475c2
title: 安裝和設定功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0731eff882c614c19c20d8323d012a7656fc2d8c15072aaafef3d7c91e46e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097858"
---
# <a name="installation-and-configuration-functions"></a>安裝和設定功能

下列函式會在 Ws232.dll 中執行，並可供在 \_ 電腦上安裝 Windows 通訊端傳輸和命名空間服務提供者的應用程式使用。 這些函式不會影響目前正在執行的應用程式，也不會對目前正在執行的應用程式顯示這些函式所做的變更。

針對所有提供者，提供者識別碼是由提供者開發人員所產生的 GUID， (使用 Uuidgen.exe 公用程式) 並提供給 Ws2 \_32.dll。



| 函式                                                                      | 描述                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)                        | 從登錄中移除傳輸服務提供者。                                                                                                  |
| [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)                      | 從64位平臺上的登錄中移除指定的32位傳輸服務提供者。                                                          |
| [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)                                | 抓取可用傳輸通訊協定的相關資訊。                                                                                               |
| [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)                              | 取得64位平臺上32位目錄中可用傳輸通訊協定的相關資訊。                                                     |
| [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider)                            | 註冊新的傳輸服務提供者。                                                                                                              |
| [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32)                   | 在64位平臺上，將新的傳輸服務提供者註冊至32位和64位的系統設定資料庫。                               |
| [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)            | 在32位平臺上，將新的32位傳輸服務提供者以及其特定的通訊協定鏈註冊到系統設定資料庫。   |
| [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32) | 在64位平臺上，將新的傳輸提供者及其特定的通訊協定鏈登錄到32位和64位的系統設定資料庫。 |



 

 

 




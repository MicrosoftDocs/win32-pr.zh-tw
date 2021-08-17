---
description: 安裝新的服務類別時，必須備妥和提供 WSASERVICECLASSINFO 結構。 此結構也包含子結構，其中包含一系列適用于特定命名空間的參數。
ms.assetid: fb225e0c-a0c7-44e1-80fb-7b924b371afa
title: SPI 中的服務類別資料結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53eb2fd61c5ec6295b65128048bc9fe477ae63f78f89bfba4be73798002ead88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993561"
---
# <a name="service-class-data-structures-in-the-spi"></a>SPI 中的服務類別資料結構

安裝新的服務類別時，必須備妥和提供 [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) 結構。 此結構也包含子結構，其中包含一系列適用于特定命名空間的參數。

![此圖顯示適用于特定命名空間的 WSASERVICECLASSINFO 結構、子結構和參數。](images/ovrvw3-3.png)

每個服務類別都有一個 [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) 結構。 在 **WSASERVICECLASSINFO** 結構內，服務類別的唯一識別碼會包含在 **lpServiceClassId** 中，而 **lpServiceClassName** 會參考相關聯的顯示字串。

[**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)結構中的 **lpClassInfos** 成員會參考 [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)結構的陣列，其中每個結構都會提供套用至指定命名空間的具名引數和具類型參數。 **LpszName** 成員的值範例包括： SAPID、TCPPORT、UDPPORT 等等。這些字串通常是在 **dwNameSpace** 中所識別的命名空間特有。 **DwValueType** 的一般值可能是 reg \_ DWORD、reg \_ SZ 等等。**DwValueSize** 成員會指出 **lpValue** 所指向之資料項目的長度。

[**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)結構中所表示的整個資料集合，都會透過 [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)提供給每個命名空間提供者。 接著，每個個別的命名空間提供者會 sifts [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) 結構的清單，並保留適用的資訊。 此架構也構思了特殊命名空間提供者的未來存在，該提供者會保留所有命名空間的所有服務類別架構資訊。 Ws2 \_32.dll 會查詢此提供者，以在叫用 [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)叫用以起始查詢，以及叫用 [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)以註冊服務時，取得提供給命名空間提供者所需的 **WSASERVICECLASSINFO** 資料。 命名空間提供者不應依賴這項功能，而應該改為取得提供者特定的方法，以取得任何所需的服務類別架構資訊。 如果沒有任何提供者儲存所有命名空間的所有服務類別架構，Ws2 \_32.dll 將會使用 [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) ，從每個個別的命名空間提供者取得這類資訊。

 

 




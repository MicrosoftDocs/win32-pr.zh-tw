---
description: 服務類別的安裝、服務實例的註冊和基本查詢作業都會直接從 API 對應到 SPI。
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: API 與 SPI 函數之間的名稱解析對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad02896ea15fb1b7c7e2aa2e01d9ec0727492da43d0446819dd1f2e04ad591d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733622"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>API 與 SPI 函數之間的名稱解析對應

服務類別的安裝、服務實例的註冊和基本查詢作業都會直接從 API 對應到 SPI。 [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)函式在 SPI 中沒有對應的函式，因為此函式是在 Ws2 \_32.dll 藉由呼叫 [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)來執行。

Helper 函式 [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) 和 [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) 會對應到傳輸 API 中的對應函式，因為只有傳輸提供者一定會知道如何在 [**sockaddr**](sockaddr-2.md) 結構上執行轉譯。

 

 




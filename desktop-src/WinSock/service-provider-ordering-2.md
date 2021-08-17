---
description: 最初安裝傳輸服務提供者的順序，會控制在服務提供者介面上透過 WSCEnumProtocols 和 WSCEnumProtocols32 列舉的順序，或透過應用程式介面上的 WSAEnumProtocols 來進行列舉的順序。 更重要的是，當用戶端要求根據地址系列、類型和通訊協定識別碼建立通訊端時，此順序也會控制通訊協定和服務提供者的順序。
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: 服務提供者排序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445fcc0cadafae8fd61ee2e34a872485b67466037c1dc71e34ab173156c8d9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740579"
---
# <a name="service-provider-ordering"></a>服務提供者排序

最初安裝傳輸服務提供者的順序，會控制在服務提供者介面上透過 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) 和 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 列舉的順序，或透過應用程式介面上的 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) 來進行列舉的順序。 更重要的是，當用戶端要求根據地址系列、類型和通訊協定識別碼建立通訊端時，此順序也會控制通訊協定和服務提供者的順序。

Windows通訊端2包含名為 Sporder.exe 的小程式，可讓已安裝的通訊協定目錄在安裝通訊協定之後以互動方式重新排序。 Winsock 也包含 Sporder.dll 的輔助 DLL，可匯出重新排列通訊協定的程式性介面。 這個程式介面是由稱為 [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder)的單一程式所組成。

介面定義可以透過 include 檔 Sporder 匯入 C 或 c + + 程式。 您可以使用 lib 檔案 Sporder 連結進入點。

 

 




---
title: 探索藍牙裝置和服務
description: 為了協助探索藍牙裝置和服務，Windows 將藍牙服務探索通訊協定 (SDP) 對應到 Windows 通訊端命名空間介面。
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- 藍牙、工作、探索裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae18f8f7ff8e7c2fcf2623ef9554bc77ec84d4b1d4ea56eced289cc86c12f0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004038"
---
# <a name="discovering-bluetooth-devices-and-services"></a>探索藍牙裝置和服務

為了協助探索藍牙裝置和服務，Windows 將藍牙服務探索通訊協定 (SDP) 對應到 Windows 通訊端命名空間介面。 用於此對應的主要函式為 [**WSASetService**](bluetooth-and-wsasetservice.md)、 [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)、 [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)和 [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) 函數。 [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)結構也會與這些函式一起使用。

由於藍牙 SDP 的特定概念和參數不一定會直接對應至 [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)結構，因此必須支付其成員建立和使用方式的相關注意事項。 針對許多複雜的藍牙作業，例如建立 SDP 記錄，會使用 **WSAQUERYSET** 的 **lpBlob** 成員。 當需要這類特殊考慮時，會特別說明，例如 [**藍牙和 WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)等參考頁面。

請務必瞭解，SDP 註冊與通訊端控制不同。 準備好要接受用戶端連線的伺服器應用程式時，它應該呼叫 [**WSASetService**](bluetooth-and-wsasetservice.md)函式來註冊與該服務對應的藍牙 SDP 記錄。 藍牙應用程式必須在關閉之前再次呼叫 **WSASetService** 函式，以取消註冊藍牙的 SDP 記錄。

使用此頁面所述的對應函式時， \_ 會指派 NS BTH 命名空間。

如需探索裝置和服務的詳細資訊，請參閱下列參考頁面：

-   [**藍牙和 WSASetService**](bluetooth-and-wsasetservice.md)
-   [**裝置查詢的藍牙和 WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**服務探索藍牙和 WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**藍牙和 WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**藍牙和 WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**藍牙和 BLOB**](bluetooth-and-blob.md)
-   [**藍牙和 WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

您也可以下載[藍牙的連接範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)，以取得完整的範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[藍牙使用 Windows 通訊端進行程式設計](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[藍牙連接範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 





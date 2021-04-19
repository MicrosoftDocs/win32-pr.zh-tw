---
title: 探索藍牙裝置和服務
description: 為了協助探索藍牙裝置和服務，Windows 會將藍牙服務探索通訊協定 (SDP) 對應至 Windows 通訊端命名空間介面。
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- 藍牙，工作，探索裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/07/2020
ms.locfileid: "106966025"
---
# <a name="discovering-bluetooth-devices-and-services"></a>探索藍牙裝置和服務

為了協助探索藍牙裝置和服務，Windows 會將藍牙服務探索通訊協定 (SDP) 對應至 Windows 通訊端命名空間介面。 用於此對應的主要函式為 [**WSASetService**](bluetooth-and-wsasetservice.md)、 [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)、 [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)和 [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) 函數。 [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)結構也會與這些函式一起使用。

由於藍牙 SDP 的特定概念和參數不一定會直接對應至 [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) 結構，因此必須將注意的方式納入其成員的建立與使用方式。 針對許多複雜的藍牙作業（例如建立 SDP 記錄），會使用 **WSAQUERYSET** 的 **lpBlob** 成員。 當需要這類特殊考慮時，會特別說明，例如在 [**藍牙和 WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)等參考頁面中。

請務必瞭解，SDP 註冊與通訊端控制不同。 當伺服器應用程式準備接受用戶端連接時，它應該呼叫 [**WSASetService**](bluetooth-and-wsasetservice.md) 函式來登錄與該服務對應的藍牙 SDP 記錄。 藍牙應用程式必須在關閉之前再次呼叫 **WSASetService** 函式，以取消註冊藍牙 SDP 記錄。

使用此頁面所述的對應函式時， \_ 會指派 NS BTH 命名空間。

如需探索裝置和服務的詳細資訊，請參閱下列參考頁面：

-   [**藍牙和 WSASetService**](bluetooth-and-wsasetservice.md)
-   [**適用于裝置查詢的藍牙和 WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**適用于服務探索的藍牙和 WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**藍牙和 WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**藍牙和 WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**藍牙和 BLOB**](bluetooth-and-blob.md)
-   [**藍牙和 WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

您也可以下載 [藍牙連線範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) ，以取得完整的範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Windows 通訊端進行藍牙程式設計](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[藍牙連接範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 





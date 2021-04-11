---
description: MTP/藍牙連接介面
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: MTP/藍牙連接介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027403"
---
# <a name="mtpbluetooth-connection-interfaces"></a>MTP/藍牙連接介面

下列介面可讓應用程式僅列舉支援媒體傳輸通訊協定的裝置，並將其連線到透過藍牙 (MTP/藍牙)  (MTP) 。 WPD 驅動程式（、集合和用戶端介面）不受 MTP/Bluetooth 通訊協定限制。



| 介面                                                              | 描述                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**IConnectionRequestCallback**](iconnectionrequestcallback.md)       | 定義單一回呼方法，讓應用程式用來接收已完成和已取消之要求的通知。 |
| [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) | 列舉 **IPortableDeviceConnector** 介面。                                                                 |
| [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | 支援應用程式呼叫的方法，以建立與 MTP 藍牙裝置的連線。                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](programming-reference.md)
</dt> </dl>

 

 




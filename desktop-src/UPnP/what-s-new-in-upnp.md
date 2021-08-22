---
title: UPnP Api 的新功能
description: UPnP™ api 提供 Windows XP SP2 的新功能和更新的檔。 下表識別新的檔集。
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68ab872eab498e80ec8d30f996f839c73432875d02ec8d32060595ce8d6482b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057996"
---
# <a name="whats-new-in-the-upnp-apis"></a>UPnP Api 的新功能

UPnP™ api 提供 Windows XP SP2 的新功能和更新的檔。 下表識別新的檔集。



| 功能                                                          | 描述                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | 這個新介面可讓託管裝置取得要求者的相關資訊 (也就是控制點) 和要求。 它包含三種方法，每個方法都提供不同類型的資訊。                                                                                                                                                              |
| [執行裝置行為](implementing-device-behavior.md) | 本主題包含新的章節，說明如何使用新的 [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) 介面取得端點資訊。                                                                                                                                                                                                     |
| [Configuration 設定](configuration-settings.md)             | 此新主題提供影響 UPnP Api 行為之登錄設定的相關資訊。                                                                                                                                                                                                                                                                    |
| [裝置錯誤碼](device-error-codes.md)                     | 這個新的主題說明如何將裝置的錯誤碼轉換成 HRESULT 值，反之亦然。 您必須瞭解此程式，才能評估 [**IUPnPService：： InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) 和 [**IUPnPService：： QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) 方法所傳回的 HRESULT 值。 |



 

 

 





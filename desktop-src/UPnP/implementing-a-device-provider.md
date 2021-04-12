---
title: 執行裝置提供者
description: 若要執行裝置提供者，請建立公開 IUPnPDeviceProvider 介面的物件。
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462449"
---
# <a name="implementing-a-device-provider"></a>執行裝置提供者

若要執行裝置提供者，請建立公開 [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) 介面的物件。 此物件必須使用 [**IUPnPRegistrar：： RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) 方法向裝置主機註冊。 這個方法會採用下列參數：

-   提供者的名稱，在電腦上必須是唯一的。
-   實作為裝置提供者之類別的 ProgID。
-   啟動時傳遞給裝置提供者的初始化字串。
-   容器識別碼。 容器識別碼是識別裝置所屬群組的字串。 所有具有相同容器識別碼的裝置都會裝載在相同的進程中。

 

 





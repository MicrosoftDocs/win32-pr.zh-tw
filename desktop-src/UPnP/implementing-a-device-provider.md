---
title: 執行裝置提供者
description: 若要執行裝置提供者，請建立公開 IUPnPDeviceProvider 介面的物件。
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19823357389a513a095081ce6ca79176af79897273274cc1f0e59a56e29b339f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999648"
---
# <a name="implementing-a-device-provider"></a>執行裝置提供者

若要執行裝置提供者，請建立公開 [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) 介面的物件。 此物件必須使用 [**IUPnPRegistrar：： RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) 方法向裝置主機註冊。 這個方法會採用下列參數：

-   提供者的名稱，在電腦上必須是唯一的。
-   實作為裝置提供者之類別的 ProgID。
-   啟動時傳遞給裝置提供者的初始化字串。
-   容器識別碼。 容器識別碼是識別裝置所屬群組的字串。 所有具有相同容器識別碼的裝置都會裝載在相同的進程中。

 

 





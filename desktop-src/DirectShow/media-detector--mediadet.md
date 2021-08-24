---
description: '媒體偵測器 (MediaDet) '
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: '媒體偵測器 (MediaDet) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a072a5d70cf392a1b81fc8387d976bea1db2ddaa5ca2328df914be96a791d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684968"
---
# <a name="media-detector-mediadet"></a>媒體偵測器 (MediaDet) 

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

媒體偵測器 (MediaDet) 物件會從檔案來源抓取格式資訊和仍然是畫面格。 媒體偵測器不需要篩選 Graph 管理員就能運作。 若要建立這個物件，請呼叫 **CoCreateInstance**。 類別識別碼是 CLSID \_ MediaDet。

若要讀取 Windows 媒體™檔，應用程式必須提供軟體憑證，也稱為金鑰。 透過媒體偵測器的 **IObjectWithSite** 介面，將應用程式註冊為金鑰提供者。 如需詳細資訊，請參閱[解除鎖定 Windows 媒體格式 SDK](unlocking-the-windows-media-format-sdk.md)。

MediaDet 物件會公開下列介面：

-   [**IMediaDet**](imediadet.md)
-   **IObjectWithSite**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用來源](working-with-sources.md)
</dt> </dl>

 

 




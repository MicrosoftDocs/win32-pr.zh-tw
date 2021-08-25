---
description: 具現化編解碼器 DMOs
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: 具現化編解碼器 DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180fcb6a3de7c581f48c7f78981e12b544963cbfb590e521d43413732bcc1e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957548"
---
# <a name="instantiating-codec-dmos"></a>具現化編解碼器 DMOs

您可以藉由呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM 函數來建立編解碼器 DMO。 您必須傳遞 DMO 的類別識別碼、 **IMediaObject** 的介面識別碼，以及指向 **IMediaObject** 指標的指標。

編解碼器 DMOs 的類別識別碼會定義為 wmcodecdsp .h 標頭檔中的常數。

**IMediaObject** 介面識別碼的常數是 IID \_ IMediaObject。

下列程式碼範例示範如何建立編解碼器 DMO 的實例：


```
HRESULT CreateVideoEncoderDMO(IMediaObject** ppDMO)
{
    if(ppDMO == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMediaObject, 
                            (void**)ppDMO);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 

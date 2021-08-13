---
description: 正在初始化媒體基礎
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: 正在初始化媒體基礎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202ab57db5821b252001a723eb8765493eb86362111da5c54e5e16e9fca4219a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268918"
---
# <a name="initializing-media-foundation"></a>正在初始化媒體基礎

使用任何 Microsoft 媒體基礎物件或介面之前，您必須呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 函數。 傳入常數 **MF \_ 版本**。


```C++
    hr = MFStartup(MF_VERSION);
```



[**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)函式會初始化媒體基礎平臺。 如果 **MFStartup** 傳回 MF \_ E \_ 不良 \_ \_ 的啟動版本，這表示您的應用程式是使用不符合系統上媒體基礎 dll 的媒體基礎標頭版本進行編譯。

對於 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)的每個呼叫，您的應用程式都必須呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)。


```C++
MFShutdown();
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎架構](media-foundation-architecture.md)
</dt> <dt>

[媒體基礎平臺 Api](media-foundation-platform-apis.md)
</dt> </dl>

 

 




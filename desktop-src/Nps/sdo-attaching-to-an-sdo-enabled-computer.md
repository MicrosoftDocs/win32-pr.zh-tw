---
title: 附加至 SDO-Enabled 電腦
description: 附加至 SDO-Enabled 電腦
ms.assetid: 434e2e0c-075e-48a9-9617-bbe75716380d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dcf64c087155054e46a5ec22e2b6f01e4db247ac485b1a056cf50e265af414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362196"
---
# <a name="attaching-to-an-sdo-enabled-computer"></a>附加至 SDO-Enabled 電腦

下列程式碼會以 SDO 電腦的形式附加到本機電腦。


```C++
   HRESULT  hr;
   CComPtr<ISdoMachine> pSdoMachine;
   CLSID    clsid;

   hr = CLSIDFromProgID(TEXT("IAS.SdoMachine"), &clsid);
   if (FAILED(hr))
   {
      return hr;
   }

   hr = CoCreateInstance(
      clsid,
      NULL,
      CLSCTX_INPROC_SERVER,
      __uuidof(ISdoMachine),
      (void**)&pSdoMachine
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Pass NULL to specify local computer.
   //
   hr = pSdoMachine->Attach(NULL); 
   if (FAILED(hr))
   {
      return hr;
   }

```



以 SDO 電腦的形式附加至電腦是透過 SDO 管理電腦的第一步。

如需詳細資訊，請參閱 [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)、 [**ISdoMachine：： Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach)。

 

 
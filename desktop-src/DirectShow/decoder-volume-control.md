---
description: 解碼器磁片區控制
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: 解碼器磁片區控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e96ed9efb17a4fb32c41d8b10313edbe015c202b7f7d1f4287e1af20cca559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953147"
---
# <a name="decoder-volume-control"></a>解碼器磁片區控制

應用程式會透過 [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) 介面控制音訊音量。 系統會為 KSProxy 提供 **IBasicAudio** 介面處理常式。 若要讓解碼器處理 KSProxy 中的磁片區命令，它必須在其安裝腳本中新增數個登錄機碼，並支援 **KSPROPSETID \_ Wave** 屬性集。

為驅動程式建立一些新的登錄機碼：


```C++
HKLM\SYSTEM\
  CurrentControlSet\Control
    DeviceClasses
      (decoder guid, eg 2721AE....)
        (Pnp id, eg ##?#VDGENDEV#...)
          #GLOBAL
            Device Parameters
              CLSID      REG_SZ   {17CCA...}
                FriendlyName   REG_SZ   WDM DVD Driver
                  Interfaces <--- create this key
                  {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
    MediaInterfaces
      {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
        (default)  REG_SZ   'KsProxy IBasicAudio handler' // Set this value.
        IID        REG_SZ   56 a8 68 b3 0a d4 11 ce b0 3a 00 20 af 0b a7 70 
                            // Create this key.
```



若要執行磁片區控制，驅動程式也必須支援 **KSPROPSETID \_ wave**，以及 KsProperty.Id = KsProperty \_ Wave \_ 磁片區。 這個屬性會透過 [**IKsPropertySet：： Get**](ikspropertyset-get.md) 和 [**IKsPropertySet：： Set**](ikspropertyset-set.md) 方法傳遞給驅動程式。 LeftAttenuation 和 RightAttentuation 欄位將左/右喇叭磁片區指定為從0x0000 到0xffff 的線性值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[解碼器介面和規格](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 




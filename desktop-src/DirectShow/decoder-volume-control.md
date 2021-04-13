---
description: 解碼器磁片區控制
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: 解碼器磁片區控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ce525f8b39e873d2c0002ac283014a9bcbe87c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385810"
---
# <a name="decoder-volume-control"></a><span data-ttu-id="c3530-103">解碼器磁片區控制</span><span class="sxs-lookup"><span data-stu-id="c3530-103">Decoder Volume Control</span></span>

<span data-ttu-id="c3530-104">應用程式會透過 [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) 介面控制音訊音量。</span><span class="sxs-lookup"><span data-stu-id="c3530-104">Applications control audio volume through the [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) interface.</span></span> <span data-ttu-id="c3530-105">系統會為 KSProxy 提供 **IBasicAudio** 介面處理常式。</span><span class="sxs-lookup"><span data-stu-id="c3530-105">An **IBasicAudio** interface handler is provided for KSProxy.</span></span> <span data-ttu-id="c3530-106">若要讓解碼器處理 KSProxy 中的磁片區命令，它必須在其安裝腳本中新增數個登錄機碼，並支援 **KSPROPSETID \_ Wave** 屬性集。</span><span class="sxs-lookup"><span data-stu-id="c3530-106">For a decoder to handle the volume commands from KSProxy, it must add several registry keys in its setup script and support the **KSPROPSETID\_Wave** property set.</span></span>

<span data-ttu-id="c3530-107">為驅動程式建立一些新的登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="c3530-107">Create some new registry keys for the driver:</span></span>


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



<span data-ttu-id="c3530-108">若要執行磁片區控制，驅動程式也必須支援 **KSPROPSETID \_ wave**，以及 KsProperty.Id = KsProperty \_ Wave \_ 磁片區。</span><span class="sxs-lookup"><span data-stu-id="c3530-108">To implement volume control, the driver also must support **KSPROPSETID\_Wave**, along with KsProperty.Id = KSPROPERTY\_WAVE\_VOLUME.</span></span> <span data-ttu-id="c3530-109">這個屬性會透過 [**IKsPropertySet：： Get**](ikspropertyset-get.md) 和 [**IKsPropertySet：： Set**](ikspropertyset-set.md) 方法傳遞給驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c3530-109">This property is passed to the driver through the [**IKsPropertySet::Get**](ikspropertyset-get.md) and [**IKsPropertySet::Set**](ikspropertyset-set.md) methods.</span></span> <span data-ttu-id="c3530-110">LeftAttenuation 和 RightAttentuation 欄位將左/右喇叭磁片區指定為從0x0000 到0xffff 的線性值。</span><span class="sxs-lookup"><span data-stu-id="c3530-110">The LeftAttenuation and RightAttentuation fields specify the left/right speaker volumes as linear values from 0x0000 to 0xffff.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3530-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3530-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3530-112">解碼器介面和規格</span><span class="sxs-lookup"><span data-stu-id="c3530-112">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 




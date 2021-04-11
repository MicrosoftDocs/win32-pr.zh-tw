---
description: 與動作補償設備磁碟機的操作對應
ms.assetid: bd92a0f4-98d9-497a-99b9-0cf432347daf
title: 與動作補償設備磁碟機的操作對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cca960ed8cbdae212bbe5e9f3b25316125a7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187437"
---
# <a name="operational-correspondence-with-motion-compensation-device-driver"></a>與動作補償設備磁碟機的操作對應

本節包含 DirectX VA 介面之動作補償設備磁碟機端的描述。  (參考： Windows 2000 DDK-圖形驅動程式-設計指南-3.0 DirectDraw DDI-3.12 動作補償。 如需以粗體顯示的結構相關檔，請參閱 Windows DDK。 ) 

下列專案是指透過 **DD \_ MOTIONCOMPCALLBACKS** 結構存取的專案：

1.  在相關的處理開始時，設備磁碟機的 **DdMoCompCreate** 會用來通知驅動程式，軟體解碼器將使用 video 加速物件開始。
2.  從 [**IAMVideoAccelerator：： GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) 收到的 guid 源自設備磁碟機的 **DdMoCompGetGUIDs**。
3.  對下游輸入 pin 的 [**IAMVideoAccelerator：： GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) 的呼叫會從設備磁碟機的 **DdMoCompGetFormats** 傳回資料。
4.  \_從解碼器的 [**IAMVideoAcceleratorNotify：： GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) DXVA ConnectMode 資料結構會傳遞至設備磁碟機的 **DdMoCompCreate**。
5.  從 [**IAMVideoAccelerator：： GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo) 傳回的資料來源自設備磁碟機的 **DdMoCompGetBuffInfo**。
6.  使用 [**IAMVideoAccelerator：： Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) 傳送的緩衝區是由設備磁碟機的 **DdMoCompRender** 所接收。
7.  使用 [**IAMVideoAccelerator：： QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) 會叫用設備磁碟機的 **DdMoCompQueryStatus**。 \_主機解碼器會看到來自 DdMoCompQueryStatus 的 DDERR WASSTILLDRAWING 傳回碼，作為 \_ **IAMVideoAccelerator：： QueryRenderStatus** 暫止之 E 的傳回碼。
8.  傳送至 [**IAMVideoAccelerator：： BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) 的資料是由設備磁碟機的 **DdMoCompBeginFrame** 所接收。 DdMoCompBeginFrame 需要有 E 暫止的傳回碼，才能 \_ 讓 \_ 主機解碼器看到 e 暫止，以回應 **IAMVideoAccelerator：： BeginFrame**。
9.  傳送至 [**IAMVideoAccelerator：： EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) 的資料是由設備磁碟機的 **DdMoCompEndFrame** 所接收。
10. 在相關的處理結束時，設備磁碟機的 **DdMoCompDestroy** 會用來通知驅動程式，將不再使用目前的影片加速物件，讓驅動程式可以執行任何必要的清除。

 

 




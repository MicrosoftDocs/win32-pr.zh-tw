---
description: 核心音訊結構
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: 核心音訊結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078f49ac7abce8fc2773549df26431b780550c1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973149"
---
# <a name="core-audio-structures"></a>核心音訊結構

本節說明 Windows Vista 和更新版本中核心音訊 Api 所使用的結構。



| 結構                                                                     | Description                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**音訊 \_ 大量 \_ 通知 \_ 資料**](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | 描述音訊端點裝置的音量層級或靜音狀態變更。                                                                                 |
| [**DIRECTX \_ 音訊 \_ 啟動 \_ 參數**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | 指定 DirectSound 資料流程的初始化參數。                                                                                                   |
| [**KSJACK \_ 描述**](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | 透過 [**IKsJackDescription：： GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); 抓取描述音訊插孔。                                 |
| [**KSJACK \_ DESCRIPTION2**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | 透過 [**IKsJackDescription2：： GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); 抓取描述音訊插孔。 <br/>                 |
| [**KSJACK \_ 接收 \_ 資訊**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | 透過 [**IKsJackSinkInformation：： GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); 抓取描述音訊插孔接收器。<br/> |
| [**LUID**](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | 儲存影片埠識別碼。<br/>                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計參考](programming-reference.md)
</dt> </dl>

 

 





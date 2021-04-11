---
description: 端點 \_ 硬體 \_ 支援 \_ XXX 常數是音訊端點裝置的硬體支援旗標。
ms.assetid: 54032f75-2287-4589-bda5-e005ee077c41
title: 'ENDPOINT_HARDWARE_SUPPORT_XXX 常數 (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffb5b2255330b205519ce3065ccb5f7eebb6b65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111549"
---
# <a name="endpoint_hardware_support_xxx-constants"></a>端點 \_ 硬體 \_ 支援 \_ XXX 常數

端點 \_ 硬體 \_ 支援 \_ XXX 常數是音訊端點裝置的硬體支援旗標。



| 常數/值                                                                                                                                                                                                                                                                           | Description                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="ENDPOINT_HARDWARE_SUPPORT_VOLUME"></span><span id="endpoint_hardware_support_volume"></span><dl> <dt>**端點 \_硬體 \_ 支援 \_ 磁片**</dt>區 <dt>0x00000001</dt> </dl> | 音訊端點裝置支援硬體磁片區控制。<br/> |
| <span id="ENDPOINT_HARDWARE_SUPPORT_MUTE"></span><span id="endpoint_hardware_support_mute"></span><dl> <dt>**端點 \_硬體 \_ 支援 \_ 靜音**</dt> <dt>0x00000002</dt> </dl>       | 音訊端點裝置支援硬體靜音控制。<br/>   |
| <span id="ENDPOINT_HARDWARE_SUPPORT_METER"></span><span id="endpoint_hardware_support_meter"></span><dl> <dt>**端點 \_硬體 \_ 支援 \_ 計量表**</dt> <dt>0x00000004</dt> </dl>    | 音訊端點裝置支援硬體尖峰計量表。<br/>     |



## <a name="remarks"></a>備註

[**IAudioEndpointVolume：： QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)和 [**IAudioMeterInformation：： QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)方法會使用端點 \_ 硬體 \_ 支援 \_ XXX 常數。

硬體支援遮罩會指出音訊端點裝置在硬體中執行的功能。 遮罩可以是0，或一或多個端點 \_ 硬體 \_ 支援 XXX 常數的位 or 組合 \_ 。 如果在遮罩中設定對應至特定端點 \_ 硬體 \_ 支援 XXX 常數的位，則表示該常數所代表的函式 \_ 會由裝置在硬體中實作為。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[核心音訊常數](core-audio-constants.md)
</dt> <dt>

[**IAudioEndpointVolume::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-queryhardwaresupport)
</dt> <dt>

[**IAudioMeterInformation::QueryHardwareSupport**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-queryhardwaresupport)
</dt> </dl>

 

 





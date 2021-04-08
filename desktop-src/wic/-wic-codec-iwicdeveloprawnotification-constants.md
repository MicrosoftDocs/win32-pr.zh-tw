---
description: IWICDevelopRawNotificationCallback 用來指出哪些成員已變更的旗標。
ms.assetid: 4e94b4f4-abd9-4395-87ec-a08e49a2cf88
title: 'IWICDevelopRawNotificationCallback 常數 (Wincodec) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8bf5d7cb2f4ac0e6fddd1f2e9151c95143b0cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944994"
---
# <a name="iwicdeveloprawnotificationcallback-constants"></a>IWICDevelopRawNotificationCallback 常數

[**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)用來指出哪些成員已變更的旗標。



| 常數/值                                                                                                                                                                                                                                                                                                                                                                                            | Description                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| <span id="WICRawChangeNotification_ExposureCompensation"></span><span id="wicrawchangenotification_exposurecompensation"></span><span id="WICRAWCHANGENOTIFICATION_EXPOSURECOMPENSATION"></span><dl> <dt>**WICRawChangeNotification \_ExposureCompensation**</dt> <dt>0x00000001</dt> </dl>             | 用來報告曝光補償變更的遮罩。<br/>                                                       |
| <span id="WICRawChangeNotification_NamedWhitePoint"></span><span id="wicrawchangenotification_namedwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_NAMEDWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_NamedWhitePoint**</dt> <dt>0x00000002</dt> </dl>                                 | 用來報告 [**WICNamedWhitePoint**](/windows/desktop/api/Wincodec/ne-wincodec-wicnamedwhitepoint) 變更的遮罩。<br/>                 |
| <span id="WICRawChangeNotification_KelvinWhitePoint"></span><span id="wicrawchangenotification_kelvinwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_KELVINWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_KelvinWhitePoint**</dt> <dt>0x00000004</dt> </dl>                             | 用來報告「開氏」點變更的遮罩。<br/>                                                          |
| <span id="WICRawChangeNotification_RGBWhitePoint"></span><span id="wicrawchangenotification_rgbwhitepoint"></span><span id="WICRAWCHANGENOTIFICATION_RGBWHITEPOINT"></span><dl> <dt>**WICRawChangeNotification \_RGBWhitePoint**</dt> <dt>0x00000008</dt> </dl>                                         | 用來報告 RGB 白色點變更的遮罩。<br/>                                                             |
| <span id="WICRawChangeNotification_Contrast"></span><span id="wicrawchangenotification_contrast"></span><span id="WICRAWCHANGENOTIFICATION_CONTRAST"></span><dl> <dt>**WICRawChangeNotification \_對比**</dt> <dt>0x00000010</dt> </dl>                                                             | 用來報告對比變更的遮罩。<br/>                                                                    |
| <span id="WICRawChangeNotification_Gamma"></span><span id="wicrawchangenotification_gamma"></span><span id="WICRAWCHANGENOTIFICATION_GAMMA"></span><dl> <dt>**WICRawChangeNotification \_Gamma**</dt> <dt>0x00000020</dt> </dl>                                                                         | 用來報告 gamma 變更的遮罩。<br/>                                                                       |
| <span id="WICRawChangeNotification_Sharpness"></span><span id="wicrawchangenotification_sharpness"></span><span id="WICRAWCHANGENOTIFICATION_SHARPNESS"></span><dl> <dt>**WICRawChangeNotification \_清晰度**</dt> <dt>0x00000040</dt> </dl>                                                         | 用來報告清晰度變更的遮罩。<br/>                                                                   |
| <span id="WICRawChangeNotification_Saturation"></span><span id="wicrawchangenotification_saturation"></span><span id="WICRAWCHANGENOTIFICATION_SATURATION"></span><dl> <dt>**WICRawChangeNotification \_飽和度**</dt> <dt>0x00000080</dt> </dl>                                                     | 用來報告飽和度變更的遮罩。<br/>                                                                  |
| <span id="WICRawChangeNotification_Tint"></span><span id="wicrawchangenotification_tint"></span><span id="WICRAWCHANGENOTIFICATION_TINT"></span><dl> <dt>**WICRawChangeNotification \_色調**</dt> <dt>0x00000100</dt> </dl>                                                                             | 用來報告色調變更的遮罩。<br/>                                                                        |
| <span id="WICRawChangeNotification_NoiseReduction"></span><span id="wicrawchangenotification_noisereduction"></span><span id="WICRAWCHANGENOTIFICATION_NOISEREDUCTION"></span><dl> <dt>**WICRawChangeNotification \_NoiseReduction**</dt> <dt>0x00000200</dt> </dl>                                     | 用來報告雜訊縮減變更的遮罩。<br/>                                                             |
| <span id="WICRawChangeNotification_DestinationColorContext"></span><span id="wicrawchangenotification_destinationcolorcontext"></span><span id="WICRAWCHANGENOTIFICATION_DESTINATIONCOLORCONTEXT"></span><dl> <dt>**WICRawChangeNotification \_DestinationColorCoNtext**</dt> <dt>0x00000400</dt> </dl> | 用來報告目的色彩內容變更的遮罩。<br/>                                                   |
| <span id="WICRawChangeNotification_ToneCurve"></span><span id="wicrawchangenotification_tonecurve"></span><span id="WICRAWCHANGENOTIFICATION_TONECURVE"></span><dl> <dt>**WICRawChangeNotification \_ToneCurve**</dt> <dt>0x00000800</dt> </dl>                                                         | 用來報告音訊曲線變更的遮罩。<br/>                                                                  |
| <span id="WICRawChangeNotification_Rotation"></span><span id="wicrawchangenotification_rotation"></span><span id="WICRAWCHANGENOTIFICATION_ROTATION"></span><dl> <dt>**WICRawChangeNotification \_旋轉**</dt> <dt>0x00001000</dt> </dl>                                                             | 用來報告 [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) 變更的遮罩。<br/> |
| <span id="WICRawChangeNotification_RenderMode"></span><span id="wicrawchangenotification_rendermode"></span><span id="WICRAWCHANGENOTIFICATION_RENDERMODE"></span><dl> <dt>**WICRawChangeNotification \_RenderMode**</dt> <dt>0x00002000</dt> </dl>                                                     | 用來報告 [**WICRawRenderMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) 變更的遮罩。<br/>                     |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]<br/>                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincodec。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback)
</dt> </dl>

 

 





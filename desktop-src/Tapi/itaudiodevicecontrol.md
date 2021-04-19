---
description: ITAudioDeviceControl 介面會公開方法，讓應用程式取得並設定參數來控制音訊裝置。
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: 'ITAudioDeviceControl 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001618"
---
# <a name="itaudiodevicecontrol-interface"></a>ITAudioDeviceControl 介面

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。 RTC 用戶端 API 提供類似的功能。\]

**ITAudioDeviceControl** 介面會公開方法，讓應用程式取得並設定參數來控制音訊裝置。

此介面是由 [IPCONF msp](ipconf-msp.md) 和 [H323 msp](h323-msp.md)所執行。 當呼叫使用這些服務提供者或協力廠商服務提供者來執行此介面時，就會公開此服務提供者。 若要取得 **ITAudioDeviceControl** 介面的指標，請在 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)介面上呼叫 **QueryInterface** ，以控制對應至資料流程的音訊裝置。 **ITStream** 介面的媒體類型必須是音訊，才能公開 **ITAudioDeviceControl** 介面。

## <a name="members"></a>成員

**ITAudioDeviceControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITAudioDeviceControl** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITAudioDeviceControl** 介面具有這些方法。



| 方法                                              | 描述                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**獲取**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | 取得指定 [音訊裝置屬性](audiodeviceproperty.md)的值。<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | 取得指定 [音訊裝置屬性](audiodeviceproperty.md)的有效值範圍。<br/> |
| [**設定**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | 設定指定 [音訊裝置屬性](audiodeviceproperty.md)的值。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 


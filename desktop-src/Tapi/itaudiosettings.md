---
description: ITAudioSettings 介面會公開方法，讓應用程式取得並設定參數來控制音訊裝置。
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: 'ITAudioSettings 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997023"
---
# <a name="itaudiosettings-interface"></a>ITAudioSettings 介面

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。 RTC 用戶端 API 提供類似的功能。\]

**ITAudioSettings** 介面會公開方法，讓應用程式取得並設定參數來控制音訊裝置。

此介面是由 [IPCONF msp](ipconf-msp.md) 和 [H323 msp](h323-msp.md)所執行。 只有在呼叫使用這些服務提供者時，才會公開此服務提供者。

## <a name="members"></a>成員

**ITAudioSettings** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITAudioSettings** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITAudioSettings** 介面具有這些方法。



| 方法                                              | 描述                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**獲取**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | 取得指定之 [音訊設定屬性](audiosettingsproperty.md)的值。<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | 取得指定之 [音訊設定屬性](audiosettingsproperty.md)的有效值範圍。<br/> |
| [**設定**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | 設定指定之 [音訊設定屬性](audiosettingsproperty.md)的值。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 


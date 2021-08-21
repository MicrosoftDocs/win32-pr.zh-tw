---
description: PKEY \_ AudioEngine \_ DeviceFormat 屬性會指定裝置格式，也就是使用者針對串流在音訊引擎和音訊端點裝置之間流動的格式（當裝置以共用模式運作時）。
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: 'PKEY_AudioEngine_DeviceFormat (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13245d23095c25173a894a7a4c7cc11b2cdc534f6ae7198508b725d0fd1cf0b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018326"
---
# <a name="pkey_audioengine_deviceformat"></a>PKEY \_ AudioEngine \_ DeviceFormat

**PKEY \_ AudioEngine \_ DeviceFormat** 屬性會指定裝置格式，也就是使用者針對串流在音訊引擎和音訊端點裝置之間流動的格式（當裝置以共用模式運作時）。 此格式可能不是獨佔模式應用程式所要使用的最佳預設格式。 一般而言，獨佔模式應用程式會對 [**IAudioClient：： IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) 方法進行一些呼叫，以尋找適合的裝置格式。 如需詳細資訊，請參閱 [裝置格式](device-formats.md)。

**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ BLOB。

**PROPVARIANT** 結構的 **Blob** 成員是 **blob** 類型的結構，其中包含兩個成員。 成員 **blob。 cbSize** 是一個 **DWORD** ，可指定格式描述中的位元組數目。 成員 **blob. pBlobData** 指向包含格式描述的 **WAVEFORMATEX** 結構。 如需 **BLOB** 的詳細資訊，請參閱 Windows SDK 檔。 如需 **WAVEFORMATEX** 的詳細資訊，請參閱 Windows DDK 檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**音訊端點屬性**](audio-endpoint-properties.md)
</dt> <dt>

[核心音訊屬性](core-audio-properties.md)
</dt> </dl>

 

 





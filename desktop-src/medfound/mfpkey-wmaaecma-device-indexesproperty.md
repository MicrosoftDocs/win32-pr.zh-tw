---
description: 指定語音捕獲 DSP 用來捕捉和呈現音訊的音訊裝置。
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: 'MFPKEY_WMAAECMA_DEVICE_INDEXES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848451"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>MFPKEY \_ WMAAECMA \_ 裝置 \_ 索引屬性

指定語音捕獲 DSP 用來捕捉和呈現音訊的音訊裝置。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

 (-1，-1) 。

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

如果您在來源模式中使用 DSP，請設定此屬性。 DSP 會忽略篩選模式中的這個屬性。

屬性的值是封裝成 **DWORD** 的 2 16 位 **字** 組。 上層16位指定音訊轉譯裝置 (通常是喇叭) ，而較低的16位則指定的捕獲裝置 (通常是麥克風) 。 每個裝置都指定為音訊裝置集合的索引。 如果索引為-1，則會使用預設裝置。

裝置索引會對應至 [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) 介面中所使用的集合索引。 應用程式必須透過選取的轉譯裝置來播放最遠的聲音。  (最遠的聲音是電話線另一端的人心聲，會透過使用者電腦上的喇叭播放 ) 。如果選取的轉譯裝置沒有作用中的串流，則 DSP 無法處理任何輸出。

這個屬性的預設值是 (-1，-1) 。

下列範例示範如何初始化這個屬性的 **PROPVARIANT** 。


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[語音捕獲 DSP](voicecapturedmo.md)
</dt> </dl>

 

 

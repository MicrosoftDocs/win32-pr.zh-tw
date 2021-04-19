---
description: 指定音訊解碼器如何將多頻道音訊轉換成身歷聲輸出。 此程式也稱為折迭。
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: 'MF_MT_AUDIO_FOLDDOWN_MATRIX 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977222"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a>MF \_ MT \_ 音訊 \_ FOLDDOWN \_ 矩陣屬性

指定音訊解碼器如何將多頻道音訊轉換成身歷聲輸出。 此程式也稱為 *折* 迭。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

這個屬性會套用到音訊媒體類型。

這個屬性的值是 [**MFFOLDDOWN \_ 矩陣**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) 結構。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 





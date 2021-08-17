---
description: 指定數位客廳網路聯盟 (DLNA) 媒體接收器的最大音訊位速度。
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: 'MF_MP2DLNA_AUDIO_BIT_RATE 屬性 (Mfmp2dlna) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed622a2f826e061dc4b909eec09490974fe83a7ac850cd0fcdfcede0abd578b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104764"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a>MF \_ MP2DLNA \_ 音訊 \_ 位 \_ 速率屬性

指定數位客廳網路聯盟 (DLNA) 媒體接收器的最大音訊位速度。

## <a name="data-type"></a>資料類型

**UINT32**

值是編碼音訊串流的目標最大位元速率，以每秒位數為單位。 此值必須是適用于 DLNA 的 MPEG-2 第2層音訊所允許的位元速率之一。 預設值為 192000 (192 Kbps) 。

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

若要在 DLNA 媒體接收器上設定此屬性，請查詢媒體接收器以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。 開始串流之前，請設定屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mfmp2dlna。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





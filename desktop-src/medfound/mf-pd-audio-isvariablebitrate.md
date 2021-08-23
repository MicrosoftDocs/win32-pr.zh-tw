---
description: 指定簡報中的音訊資料流程是否具有變數位元速率。
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: 'MF_PD_AUDIO_ISVARIABLEBITRATE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb5c8c15c12bcd867342fb11f5e753c196f9954aea0393b2a461e1804f411339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664188"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a>MF \_ PD \_ 音訊 \_ ISVARIABLEBITRATE 屬性

指定簡報中的音訊資料流程是否具有變數位元速率。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>套用至

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>備註

這是表示描述項的選擇性屬性。 如果屬性為 **TRUE** (非零) ，表示簡報至少會包含一個可變位速率 (VBR) 音訊串流。 如果屬性為 **FALSE**，則所有音訊串流都有固定的位元速率。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





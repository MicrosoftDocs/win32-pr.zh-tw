---
description: 指定 Advanced Audio 編碼 (AAC) 資料流程的裝載類型。
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: 'MF_MT_AAC_PAYLOAD_TYPE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994166"
---
# <a name="mf_mt_aac_payload_type-attribute"></a>MF \_ MT \_ AAC \_ 裝載 \_ 類型屬性

指定 Advanced Audio 編碼 (AAC) 資料流程的裝載類型。

## <a name="data-type"></a>資料類型

**UINT32**

可能的值如下。



| 值                                                                        | 意義                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 資料流程只包含原始 \_ 資料 \_ 區塊元素。<br/>                                                                    |
| <dl> <dt>1</dt> </dl> | 音訊資料傳輸串流 (ADTS) 。 資料流程包含 adts \_ 序列（如 mpeg-2 所定義）。<br/>                       |
| <dl> <dt>2</dt> </dl> | 音訊資料交換格式 (ADIF) 。 資料流程包含 adif \_ 序列（如 mpeg-2 所定義）。<br/>                     |
| <dl> <dt>3</dt> </dl> | 此資料流程包含具有同步處理層的 MPEG-2 音訊廣播串流 (LOA) 和多工層 (LATM) 。<br/> |



 

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>套用至

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>備註

MF \_ MT \_ AAC \_ 裝載 \_ 類型是選擇性的。 如果未指定此屬性，則會使用預設值0，這會指定資料流程只包含原始 \_ 資料 \_ 區塊元素。

僅適用于 **MFAudioFormat \_ AAC**。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 





---
description: 包含 [3GP] 檔案的 [範例描述] 方塊。
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: 'MF_MT_MPEG4_SAMPLE_DESCRIPTION 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c59827fa5d2ba6c6621c7e251cf319478fd621d24639e105dcd44863495b364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741785"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a>MF \_ MT \_ MPEG4 \_ 範例 \_ DESCRIPTION 屬性

包含 [3GP] 檔案的 [範例描述] 方塊。

## <a name="data-type"></a>資料類型

**位元組\[\]**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。

## <a name="applies-to"></a>適用於

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>備註

[範例描述] 方塊描述檔案中資料流程所使用的編碼方式。

MPEG 4 檔案來源會在每個資料流程的媒體類型上設定此屬性。 屬性的值是 [範例描述] 方塊中的原始資料。 如果 MPEG 檔來源可以剖析範例描述，也會將格式詳細資料新增至媒體類型。 否則，應用程式或解碼器必須剖析來自 MF \_ MT \_ MPEG4 \_ 範例 \_ description 屬性的範例描述。

當您透過 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) 方法在 MPEG 4 上設定此屬性時，如果 \_ 已將 \_ \_ \_ 一或多個範例傳送至對應資料流程的 [**IMFStreamSink：:P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) 介面上的接收，則不應變更屬性 MF MT MPEG4 範例描述的資料。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 





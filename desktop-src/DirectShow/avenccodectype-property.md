---
description: 指定編碼配置。
ms.assetid: a26951d6-67fb-43fb-849f-331416e9d7c2
title: 'AVEncCodecType 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8643c0624b7d82381e2008f2adbd6804e9af9881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317775"
---
# <a name="avenccodectype-property"></a>AVEncCodecType 屬性

指定編碼配置。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**BSTR** (**VT \_ bstr**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCodecType**

## <a name="property-value"></a>屬性值

這個屬性的值是 **BSTR** ，其中包含 GUID 的字串表示。 定義了下列 Guid。



| GUID                                      | Description                                        |
|-------------------------------------------|----------------------------------------------------|
| CODECAPI \_ GUID \_ AVEncDolbyDigitalConsumer | 杜比數位消費者音訊                       |
| CODECAPI \_ GUID \_ AVEncDolbyDigitalPlus     | 杜比數位加號音訊                           |
| CODECAPI \_ GUID \_ AVEncDolbyDigitalPro      | 杜比數位 Pro 音訊                            |
| CODECAPI \_ GUID \_ AVEncDTS                  | DTS 音訊                                          |
| CODECAPI \_ GUID \_ AVEncDTSHD                | DTS-HD 音訊                                       |
| CODECAPI \_ GUID \_ AVEncDV                   | DV 影片                                           |
| CODECAPI \_ GUID \_ AVEncH264Video            | H.264 影片                                        |
| CODECAPI \_ GUID \_ AVEncMLP                  | 經線無損封裝 (MLP) 音訊              |
| CODECAPI \_ GUID \_ AVEncMPEG1Audio           | MPEG-2 音訊                                       |
| CODECAPI \_ GUID \_ AVEncMPEG1Video           | MPEG-2 影片                                       |
| CODECAPI \_ GUID \_ AVEncMPEG2Audio           | MPEG-2 音訊                                       |
| CODECAPI \_ GUID \_ AVEncMPEG2Video           | MPEG-2 影片                                       |
| CODECAPI \_ GUID \_ AVEncPCM                  | PCM 音訊                                          |
| CODECAPI \_ GUID \_ AVEncSDDS                 | 索尼動態數位音效 (SDD) 音訊            |
| CODECAPI \_ GUID \_ AVEncWMALossless          | Windows Media 音訊9無失真音訊               |
| CODECAPI \_ GUID \_ AVEncWMAPro               | Windows Media 音訊 9 Professional (WMA Pro) 音訊 |
| CODECAPI \_ GUID \_ AVEncWMAVoice             | Windows Media 音訊9語音音訊                  |
| CODECAPI \_ GUID \_ AVEncWMV                  | Windows Media 視訊                                |
| CODECAPI \_ GUID \_ AVEndMPEG4Video           | MPEG 4 影片                                       |



 

## <a name="remarks"></a>備註

應用程式可以設定此屬性，以指定要使用的編碼配置。 編解碼器也可以傳回此屬性作為功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 





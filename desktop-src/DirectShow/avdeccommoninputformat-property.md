---
description: 指定此解碼器的目前輸入格式。
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: 'AVDecCommonInputFormat 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7432d2a48727ec144d4206d4a11bfe65ce2c5d2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467832"
---
# <a name="avdeccommoninputformat-property"></a>AVDecCommonInputFormat 屬性

指定此解碼器的目前輸入格式。

這是唯讀的屬性。

## <a name="data-type"></a>資料類型

**BSTR** (**VT \_ bstr**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecCommonInputFormat**

## <a name="property-value"></a>屬性值

這個屬性的值是 **BSTR** ，其中包含 GUID 的字串表示。 定義了下列 Guid。



| **GUID**                                            | Description                                    |
|-----------------------------------------------------|------------------------------------------------|
| **CODECAPI \_ GUID \_ AVDecAudioInputAAC**              | Advanced Audio 編碼 (AAC)                     |
| **CODECAPI \_ GUID \_ AVDecAudioInputDolbyDigitalPlus** | 杜比數位加號音訊                       |
| **CODECAPI \_ GUID \_ AVDecAudioInputDolby**            | 杜比音訊                                    |
| **CODECAPI \_ GUID \_ AVDecAudioInputDTS**              | DTS 音訊                                      |
| **CODECAPI \_ GUID \_ AVDecAudioInputHEAAC**            | High-Efficiency (AAC) 的 Advanced 音訊編碼 |
| **CODECAPI \_ GUID \_ AVDecAudioInputMPEG**             | MPEG 音訊                                     |
| **CODECAPI \_ GUID \_ AVDecAudioInputPCM**              | PCM 音訊                                      |
| **CODECAPI \_ GUID \_ AVDecAudioInputWMA**              | Windows Media 音訊                            |
| **CODECAPI \_ GUID \_ AVDecAudioInputWMAPro**           | Windows Media 音訊 9 Professional (WMA Pro)    |



 

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

 

 





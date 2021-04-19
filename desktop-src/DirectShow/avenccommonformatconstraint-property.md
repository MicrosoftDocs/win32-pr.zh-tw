---
description: 指定編碼器的目標格式。
ms.assetid: 3d316561-352f-44f9-9978-01301a68e7b6
title: 'AVEncCommonFormatConstraint 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e79536959aaaa0c50403bdd79d005bd48c729e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973554"
---
# <a name="avenccommonformatconstraint-property"></a>AVEncCommonFormatConstraint 屬性

指定編碼器的目標格式。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**BSTR** (**VT \_ bstr**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonFormatConstraint**

## <a name="property-value"></a>屬性值

這個屬性的值是 **BSTR** ，其中包含 GUID 的字串表示。 定義了下列 Guid。



| GUID                                         | Description                     |
|----------------------------------------------|---------------------------------|
| CODECAPI \_ GUID \_ AVEncCommonFormatATSC        | ATSC 纜線電視。          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVB         | DVB-T 有線電視。           |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ DashVR | DVD-VR                          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ PlusVR | DVD + VR                          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V      | DVD-Video                       |
| CODECAPI \_ GUID \_ AVEncCommonFormatHighMAT     | HighMAT                         |
| CODECAPI \_ GUID \_ AVEncCommonFormatHighMPV     | 未記載于此版本中。 |
| CODECAPI \_ GUID \_ AVEncCommonFormatMP3         | MPEG 音訊第3層 (MP3)         |
| CODECAPI \_ GUID \_ AVEncCommonFormatSVCD        | Super 視訊 CD (SVCD)            |
| CODECAPI \_ GUID \_ AVEncCommonFormatUnSpecified | 未指定的格式。             |
| CODECAPI \_ GUID \_ AVEncCommonFormatVCD         | 視訊 CD (VCD)                  |



 

## <a name="remarks"></a>備註

應用程式可以設定此屬性來指定目標格式。 編碼器也可以將此屬性作為功能傳回。

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

 

 





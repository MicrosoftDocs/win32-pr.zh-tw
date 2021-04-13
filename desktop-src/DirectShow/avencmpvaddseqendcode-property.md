---
description: 指定編碼器是否在資料流程結尾新增序列結束代碼。 這個屬性會套用至 MPEG 視頻編碼器。
ms.assetid: ef606207-2ee3-420b-afae-67c764e05e54
title: 'AVEncMPVAddSeqEndCode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a21adcf8b817e0049da3308760e20cdd0e9d473
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510204"
---
# <a name="avencmpvaddseqendcode-property"></a>AVEncMPVAddSeqEndCode 屬性

指定編碼器是否在資料流程結尾新增序列結束代碼。 這個屬性會套用至 MPEG 視頻編碼器。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**變異 \_BOOL** (**VT \_ bool**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncMPVAddSeqEndCode**

## <a name="remarks"></a>備註

如果此值為 **VARIANT \_ TRUE**，編碼器會在資料流程的結尾加入序列結束代碼。

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

 

 





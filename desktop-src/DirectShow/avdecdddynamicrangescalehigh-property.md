---
description: 指定當解碼器在杜比 AC-3 音訊串流上執行動態範圍控制時的高階剪下。
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: 'AVDecDDDynamicRangeScaleHigh 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521cd631d92db73f23c7018adeda9bd321d23c1a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467831"
---
# <a name="avdecdddynamicrangescalehigh-property"></a>AVDecDDDynamicRangeScaleHigh 屬性

指定當解碼器在杜比 AC-3 音訊串流上執行動態範圍控制時的高階剪下。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecDDDynamicRangeScaleHigh**

## <a name="property-value"></a>屬性值

這個屬性的值具有下列範圍。



| 值 | 描述                                                    |
|-------|----------------------------------------------------------------|
| 0     | 沒有動態範圍壓縮。 保留完整的動態範圍。 |
| 100   | 套用完整的動態範圍壓縮。                          |



 

## <a name="remarks"></a>備註

只有當 [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) 屬性的值是 eAVDecDDOperationalMode 行時，才會套用此屬性 \_ 。

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

 

 





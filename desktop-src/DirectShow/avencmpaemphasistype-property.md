---
description: 指定解碼時應該使用的反強調篩選類型。 這個屬性會套用至 MPEG 音訊編碼器。
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: 'AVEncMPAEmphasisType 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3da73e2708acde7a5b388d229a3a82c50a2dff04c4f2873551a992fe738189
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824228"
---
# <a name="avencmpaemphasistype-property"></a>AVEncMPAEmphasisType 屬性

指定解碼時應該使用的反強調篩選類型。 這個屬性會套用至 MPEG 音訊編碼器。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncMPAEmphasisType**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) 列舉的成員。

## <a name="remarks"></a>備註

這個屬性會在框架標題中設定強調位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop apps \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 


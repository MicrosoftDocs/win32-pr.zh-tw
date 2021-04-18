---
description: 將目前的框架標示為 LTR 框架。
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: 'CODECAPI_AVEncVideoMarkLTRFrame 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510818"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a>CODECAPI \_ AVEncVideoMarkLTRFrame 屬性

將目前的框架標示為 LTR 框架。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoMarkLTRFrame**

## <a name="remarks"></a>備註

**H.264/AVC 編碼器：**

此控制項的值是與目前框架相關聯的 h.264 語法 *LongTermFramIdx* 值。 如果目前的框架不在基底圖層中，例如語法元素 *時態 \_ 識別碼* 不等於0，則這個屬性會以編碼順序套用至下一個基底圖層框架。

如果使用 CODECAPI AVEncVideoMarkLTRFrame 屬性來發出標示 LTR 框架的暫止呼叫 \_ ，且編碼器尚未將框架標示為 ltr，則不應呼叫此屬性。 換句話說，編碼器不應將 CODECAPI AVEncVideoMarkLTRFrame 要求排入佇列 \_ 。 如果在 \_ 其他 CODECAPI AVEncVideoMarkLTRFrame 要求仍在擱置中時提交 CODECAPI AVEncVideoMarkLTRFrame 要求 \_ ，則應捨棄較舊的要求。

CODECAPI \_ AVEncVideoMarkLTRFrame 屬性是動態的，可在編碼會話期間設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 





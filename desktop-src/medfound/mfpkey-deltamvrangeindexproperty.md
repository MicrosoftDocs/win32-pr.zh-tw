---
description: 指定用來對動作向量資訊進行編碼的方法。
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: 'MFPKEY_DELTAMVRANGEINDEX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a21ac1a0bdaf859c93bca800d72f5e9ed155919bb07a24f5287b2436e57f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113338"
---
# <a name="mfpkey_deltamvrangeindex-property"></a>MFPKEY \_ DELTAMVRANGEINDEX 屬性

指定用來對動作向量資訊進行編碼的方法。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCDeltaMVRangeIndex

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

如果設定此屬性，則編碼器會在欄位中增加差異動作向量範圍。 動作向量資訊只對交錯式欄位有效。

這個屬性可以設定為下列其中一個值：



| 值 | 描述                                                                          |
|-------|--------------------------------------------------------------------------------------|
| 0     | 使用現有的 delta 動作向量範圍。                                          |
| 1     | 以水準方向按兩下差異動作向量範圍。                    |
| 2     | 以垂直方向按兩下差異動作向量範圍。                      |
| 3     | 以水準和垂直方向，將差異動作向量範圍加倍。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 





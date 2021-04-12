---
description: 指定用於移動搜尋的範圍。
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: 'MFPKEY_MOTIONSEARCHRANGE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192253"
---
# <a name="mfpkey_motionsearchrange-property"></a>MFPKEY \_ MOTIONSEARCHRANGE 屬性

指定用於移動搜尋的範圍。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCMotionSearchRange

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

這個屬性可以設定為下列其中一個值。 H 表示水準範圍，V 表示垂直範圍。 所有範圍都會以圖元為單位。



| 值 | 範圍                                |
|-------|--------------------------------------|
| 0     | + 63.75/-64.0 H、+ 31.75/-32.0 V       |
| 1     | +127.75/-128.0 H, +63.75/-64.0 V     |
| 2     | + 511.75/-512.0 H、+ 127.75/-128.0 V   |
| 3     | + 1023.75/-1024.0 H、+ 255.75/-256.0 V |
| -1    | 巨大區塊-自動調整 (自動)       |



 

這個屬性會控制編解碼器將搜尋可能在畫面格之間呈現動作之元素的框架區域大小。 較大的搜尋視窗將有助於找出更快速的動作，但需要較多的 CPU 時間。 CPU 需求大約是每個層級的兩倍。

自動模式 (-1) 會動態選取最有效率的模式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 





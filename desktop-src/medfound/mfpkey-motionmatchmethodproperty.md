---
description: 指定要用於動作比對的方法。
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: 'MFPKEY_MOTIONMATCHMETHOD 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec0604acc7dc0634be296e5097c3594dc74e5ceb7bdb7563b48a164cd13b164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355728"
---
# <a name="mfpkey_motionmatchmethod-property"></a>MFPKEY \_ MOTIONMATCHMETHOD 屬性

指定要用於動作比對的方法。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCMotionMatchMethod

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

這個屬性可以設定為下列其中一個值。



| 值 | 使用的方法                       |
|-------|-----------------------------------|
| 0     |  (悲傷) 的絕對差異總和 |
| 1     | Hadamard                          |
| -1    | 巨大區塊-適應性。              |



 

 (悲傷) 的絕對差異總和，是比 Hadamard 轉換更快速但較不精確的方法。 Hadamard 轉換更準確，但需要大量計算。 巨大區塊-調適型模式提供兩種方法之間合理的折衷方式，方法是在兩個轉換之間進行動態選擇，只在適當的情況下選取 Hadamard 轉換。

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

 

 





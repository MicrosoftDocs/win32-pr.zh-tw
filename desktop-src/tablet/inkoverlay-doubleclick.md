---
description: 當按兩下 InkCollector 或 InkOverlay 物件時發生。
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: 'DoubleClick 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4baddc89e309b7d64ba2294827b58956b3e6c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194424"
---
# <a name="inkoverlaydoubleclick-event"></a>DoubleClick 事件

當按兩下 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件時發生。

## <a name="syntax"></a>語法


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*取消* \[in、out\]
</dt> <dd>

是否應該取消父控制項的事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID IPEDblClick 識別碼的) \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkOverlay 類別**](inkoverlay-class.md)
</dt> </dl>

 

 





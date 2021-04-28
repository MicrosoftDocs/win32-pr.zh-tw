---
description: InkCollector. TabletAdded 事件-在將 IInkTablet 加入系統時發生。
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: 'InkCollector. TabletAdded 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3088eff151d9857f8a1449d3c99805c949b790
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110006"
---
# <a name="inkcollectortabletadded-event"></a>InkCollector. TabletAdded 事件

[**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)新增至系統時發生。

## <a name="syntax"></a>語法


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*平板* \[ 電腦在\]
</dt> <dd>

已新增至系統的 [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICETabletAdded 識別碼的) \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkCollector 類別**](inkcollector-class.md)
</dt> <dt>

[**IInkTablet 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 





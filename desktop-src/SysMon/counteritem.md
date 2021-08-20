---
title: 'CounterItem 物件 (Isysmon) '
description: 您可以使用這個類別來抓取計數器的路徑和值，並指定用來繪製計數器的色彩。 若要取得這個物件，請呼叫計數器。 Item。
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- CounterItem 物件 SysMon
- CounterItem 物件 SysMon，描述
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a52c9faa6d5ce6acd99921908b178d5a128c18bbdfb69665e929977293ec8fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956795"
---
# <a name="counteritem-object"></a>CounterItem 物件

您可以使用這個類別來抓取計數器的路徑和值，並指定用來繪製計數器的色彩。

若要取得這個物件，請呼叫 [**計數器。 Item**](counters-item.md)。

## <a name="members"></a>成員

**CounterItem** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**CounterItem** 物件有這些方法。



| 方法                                             | 描述                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetDataAt**](counteritem-getdataat.md)         | 從折線圖中的特定點抓取計數器資料。<br/> |
| [**GetStatistics**](counteritem-getstatistics.md) | 抓取計數器的平均值、最大值和最小值。<br/> |
| [**GetValue**](counteritem-getvalue.md)           | 抓取計數器的最後一個值。<br/>                            |



 

### <a name="properties"></a>屬性

**CounterItem** 物件具有這些屬性。



| 屬性                                                  | 描述                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**Color**](counteritem-color.md)<br/>             | 抓取或設定用來繪製計數器值的色彩。<br/>         |
| [**線條樣式**](counteritem-linestyle.md)<br/>     | 抓取或設定用來繪製計數器值的線條樣式。<br/>    |
| [**路徑**](counteritem-path.md)<br/>               | 抓取計數器的路徑。<br/>                                   |
| [**ScaleFactor**](counteritem-scalefactor.md)<br/> | 抓取或設定用來繪製計數器值的比例因數。<br/>  |
| [**已選取**](counteritem-selected.md)<br/>       | 抓取或設定值，這個值會指出是否已選取計數器。<br/> |
| [**值**](counteritem-value.md)<br/>             | 抓取計數器的目前值。<br/>                          |
| [**可見**](counteritem-visible.md)<br/>         | 抓取或設定值，這個值會指出計數器是否為繪圖。<br/>  |
| [**寬度**](counteritem-width.md)<br/>             | 抓取或設定用來繪製計數器值的線條寬度。<br/>    |



 

## <a name="remarks"></a>備註

[**值**](counteritem-value.md) 是 **CounterItem** 的預設屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Isysmon。h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SYSMON 類別](sysmon-classes.md)
</dt> </dl>

 

 






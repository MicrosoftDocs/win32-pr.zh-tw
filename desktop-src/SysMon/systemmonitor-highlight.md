---
title: SystemMonitor：醒目提示屬性
description: 抓取或設定值，指出在圖形中是否反白顯示所選計數器的值。
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- 醒目提示屬性 SysMon
- 醒目提示屬性 SysMon，SystemMonitor 類別
- SystemMonitor 類別 SysMon，醒目提示屬性
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843616"
---
# <a name="systemmonitorhighlight-property"></a>SystemMonitor：醒目提示屬性

抓取或設定值，指出在圖形中是否反白顯示所選計數器的值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a>屬性值

True 表示選取的計數器值在圖形中會反白顯示;否則為 False。 預設值是 False。

## <a name="remarks"></a>備註

若要選取一或多個計數器，可以將 [**CounterItem**](counteritem-selected.md) 設為 True，或使用者可以從圖例中所顯示的計數器清單中選取計數器。

**在 Windows Vista 之前：** 您無法以程式設計方式選取計數器，而且使用者只能從圖例所顯示的計數器清單中選取一個計數器。

醒目提示可以是黑色或白色，視 [**背景**](systemmonitor-backcolor.md) 色彩屬性的值而定。 醒目提示會自動設為色彩，以在反白顯示色彩和背景色彩之間提供足夠的對比。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**CounterItem。已選取**](counteritem-selected.md)
</dt> </dl>

 

 






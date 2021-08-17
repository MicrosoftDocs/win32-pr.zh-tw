---
title: CounterItem. ScaleFactor 屬性
description: 抓取或設定用來繪製計數器值的比例因數。
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- ScaleFactor 屬性 SysMon
- ScaleFactor 屬性 SysMon、CounterItem 類別
- CounterItem 類別 SysMon，ScaleFactor 屬性
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794cd84dd62518cc3089b8644f41b5545aeaf547b275c703a4cb87f5fec2b4a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883660"
---
# <a name="counteritemscalefactor-property"></a>CounterItem. ScaleFactor 屬性

抓取或設定用來繪製計數器值的比例因數。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a>屬性值

用來顯示圖形化計數器值的縮放係數。 有效值的範圍為-9 到 9 (值會對應至 0.000000001-100000000.0) 。

**在 Windows Vista 之前：** 有效值的範圍為-7 到 7 (值對應至 0.0000001-1000000.0) 。

## <a name="remarks"></a>備註

只有當您想要變更計數器的預設縮放比例時，才設定此屬性 (每個計數器都會定義自己的比例因數) 。 如果計數器使用其預設比例因數來繪製值，則這個屬性的值會設定為正整數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**SystemMonitor.ScaleToFit**](systemmonitor-scaletofit.md)
</dt> </dl>

 

 






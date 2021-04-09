---
title: SystemMonitor. YAxisLabel 屬性
description: 抓取或設定圖形垂直 (Y) 軸的標籤。
ms.assetid: aa022be2-99e1-43b4-894a-e4963a4ebf8c
keywords:
- YAxisLabel 屬性 SysMon
- YAxisLabel 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，YAxisLabel 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.YAxisLabel
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dffac6c3a912cd85d1a23ef43cb348e0231d6309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843736"
---
# <a name="systemmonitoryaxislabel-property"></a>SystemMonitor. YAxisLabel 屬性

抓取或設定圖形垂直 (Y) 軸的標籤。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property YAxisLabel As String
```



## <a name="property-value"></a>屬性值

圖形垂直 (Y) 軸的標籤。 標題的長度上限為128個字元。 如果標題超過128個字元，則會截斷標題。

**WINDOWS XP 和 windows 2000：** 標題的長度沒有限制。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 






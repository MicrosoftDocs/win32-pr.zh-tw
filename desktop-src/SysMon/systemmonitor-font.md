---
title: SystemMonitor 字型屬性
description: 抓取或設定控制項中所使用的字型。
ms.assetid: 973ac31e-33e6-4280-ba0b-5b9f5f7563e7
keywords:
- 字型屬性 SysMon
- Font 屬性 SysMon，SystemMonitor 類別
- SystemMonitor 類別 SysMon，字型屬性
topic_type:
- apiref
api_name:
- SystemMonitor.Font
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2abf021000d673474bb006d9d16afa459ddbdb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685941"
---
# <a name="systemmonitorfont-property"></a>SystemMonitor 字型屬性

抓取或設定控制項中所使用的字型。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property Font As stdole.IFontDisp
```



## <a name="property-value"></a>屬性值

用來在控制項中顯示文字的字型。

## <a name="remarks"></a>備註

這是環境屬性。 這個屬性的值是由容器所決定。 設定這個屬性的值可能會影響控制項和容器的假像成為單一應用程式。

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

[**SystemMonitor 的前景**](systemmonitor-forecolor.md)
</dt> </dl>

 

 






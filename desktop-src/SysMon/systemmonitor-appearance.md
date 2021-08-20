---
title: SystemMonitor 外觀屬性
description: 抓取或設定控制項的外觀，以包含或省略三維顯示效果。
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- 外觀屬性 SysMon
- 外觀屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，外觀屬性
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c606ed69bca635fe0f261f64ed4439305dcdfb542edd4c0095e62eaa97266147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956201"
---
# <a name="systemmonitorappearance-property"></a>SystemMonitor 外觀屬性

抓取或設定控制項的外觀，以包含或省略三維顯示效果。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property Appearance As Long
```



## <a name="property-value"></a>屬性值

外觀值，決定是否以立體效果繪製控制項。

您可以將此屬性設定為下列其中一個值。



| 值                                                                        | 意義                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 繪製沒有視覺效果的控制項。<br/>                                    |
| <dl> <dt>1</dt> </dl> | 繪製具有立體效果的控制項。 這是預設值。<br/> |



 

## <a name="exceptions"></a>例外狀況



| 例外狀況類型               | 條件                                    |
|------------------------------|----------------------------------------------|
| **System. ArgumentException** | 指定的外觀值無效。 |



 

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
</dt> </dl>

 

 






---
title: IdleSettings. WaitTimeout 屬性
description: 針對腳本，取得或設定值，這個值會指出工作排程器等候閒置條件發生的時間量。
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- WaitTimeout 屬性工作排程器
- WaitTimeout 屬性工作排程器，IdleSettings 物件
- IdleSettings 物件工作排程器、WaitTimeout 屬性
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025198"
---
# <a name="idlesettingswaittimeout-property"></a>IdleSettings. WaitTimeout 屬性

針對腳本，取得或設定值，這個值會指出工作排程器等候閒置條件發生的時間量。 如果未指定此屬性的值，工作排程器服務將會無限期地等候閒置的條件發生。

## <a name="syntax"></a>Syntax


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a>屬性值

值，指出工作排程器將等候閒置條件發生的時間量。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。 允許的最小時間是1分鐘。 如果這個值為 **Null**，則會將延遲設定為預設值1小時。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) 元素中指定。

如果工作是由閒置觸發程式觸發，則會忽略 **IdleSettings. WaitTimeout** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 






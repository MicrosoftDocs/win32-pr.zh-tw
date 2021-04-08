---
title: IdleSettings. IdleDuration 屬性
description: 針對腳本，取得或設定值，這個值表示電腦在工作執行前必須處於閒置狀態的時間量。
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- IdleDuration 屬性工作排程器
- IdleDuration 屬性工作排程器，IdleSettings 物件
- IdleSettings 物件工作排程器、IdleDuration 屬性
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6eeed4fef540b3a9e13d0f52e3ce1934cb9e220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686146"
---
# <a name="idlesettingsidleduration-property"></a>IdleSettings. IdleDuration 屬性

針對腳本，取得或設定值，這個值表示電腦在工作執行前必須處於閒置狀態的時間量。

## <a name="syntax"></a>Syntax


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a>屬性值

值，這個值表示) 執行工作之前，電腦必須處於閒置狀態的時間量。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。 最小值是一分鐘。 如果這個值為 **Null**，則會將延遲設定為預設值10分鐘。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) 元素中指定。

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

 

 






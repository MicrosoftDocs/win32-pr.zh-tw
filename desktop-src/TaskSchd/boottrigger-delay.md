---
title: BootTrigger Delay 屬性
description: 針對腳本，取得或設定值，這個值表示系統開機和啟動工作之間的時間長度。
ms.assetid: 4e1c4e6f-640a-4e7d-8197-914c58cfae90
keywords:
- Delay 屬性工作排程器
- Delay 屬性工作排程器，BootTrigger 物件
- BootTrigger 物件工作排程器，Delay 屬性
topic_type:
- apiref
api_name:
- BootTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6be91f00b79f2c2a47235a389b82ffb9255d586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104669"
---
# <a name="boottriggerdelay-property"></a>BootTrigger Delay 屬性

針對腳本，取得或設定值，這個值表示系統開機和啟動工作之間的時間長度。

## <a name="syntax"></a>Syntax


```VB
BootTrigger.Delay As String
```



## <a name="property-value"></a>屬性值

值，指出系統開機和啟動工作之間的時間長度。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。

## <a name="remarks"></a>備註

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**delay**](taskschedulerschema-delay-boottriggertype-element.md) 元素指定開機延遲。

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

[**BootTrigger**](boottrigger.md)
</dt> </dl>

 

 






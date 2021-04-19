---
title: EventTrigger Delay 屬性
description: 針對腳本，取得或設定值，這個值表示事件發生時間和工作啟動時間之間的時間量。
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- Delay 屬性工作排程器
- Delay 屬性工作排程器，EventTrigger 物件
- EventTrigger 物件工作排程器，Delay 屬性
topic_type:
- apiref
api_name:
- EventTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb67ca7ef12ca023bcb6c0d9d83880d4abb94af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969593"
---
# <a name="eventtriggerdelay-property"></a>EventTrigger Delay 屬性

針對腳本，取得或設定值，這個值表示事件發生時間和工作啟動時間之間的時間量。 此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。

## <a name="syntax"></a>Syntax


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a>屬性值

值，這個值表示發生事件的時間與啟動工作的時間之間的時間量。

## <a name="remarks"></a>備註

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**delay**](taskschedulerschema-delay-eventtriggertype-element.md) 元素指定事件延遲。

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

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

 






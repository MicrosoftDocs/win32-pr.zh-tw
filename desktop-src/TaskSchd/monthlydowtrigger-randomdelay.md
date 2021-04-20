---
title: MonthlyDOWTrigger. RandomDelay 屬性
description: 針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。 |MonthlyDOWTrigger. RandomDelay 屬性
ms.assetid: e5cb6c1d-8003-43f4-bf35-da490a6097f0
keywords:
- RandomDelay 屬性工作排程器
- RandomDelay 屬性工作排程器，MonthlyDOWTrigger 物件
- MonthlyDOWTrigger 物件工作排程器、RandomDelay 屬性
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e781941e927547a4ea25935fb21299777c34b3ea
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734123"
---
# <a name="monthlydowtriggerrandomdelay-property"></a>MonthlyDOWTrigger. RandomDelay 屬性

針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.RandomDelay As String
```



## <a name="property-value"></a>屬性值

隨機新增至觸發程式開始時間的延遲時間。 此字串的格式為 `P<days>DT<hours>H<minutes>M<seconds>S` (例如，P2DT5S 是2天、5秒的延遲) 。

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

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> </dl>

 

 






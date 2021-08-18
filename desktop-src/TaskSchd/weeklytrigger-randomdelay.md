---
title: WeeklyTrigger. RandomDelay 屬性
description: 針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。 |WeeklyTrigger. RandomDelay 屬性
ms.assetid: 711b188d-b283-4c99-b43d-644f39a31cdc
keywords:
- RandomDelay 屬性工作排程器
- RandomDelay 屬性工作排程器，WeeklyTrigger 物件
- WeeklyTrigger 物件工作排程器、RandomDelay 屬性
topic_type:
- apiref
api_name:
- WeeklyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc17260b33b4f5ca833ae0f2e322a99205b690ad8d54779ea6471db246cc056b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001776"
---
# <a name="weeklytriggerrandomdelay-property"></a>WeeklyTrigger. RandomDelay 屬性

針對腳本，取得或設定隨機加入至觸發程式開始時間的延遲時間。

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.RandomDelay As String
```



## <a name="property-value"></a>屬性值

隨機新增至觸發程式開始時間的延遲時間。 此字串的格式為 `P<days>DT<hours>H<minutes>M<seconds>S` (例如，P2DT5S 是2天、5秒的延遲) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 






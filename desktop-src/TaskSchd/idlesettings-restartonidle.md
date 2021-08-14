---
title: IdleSettings. RestartOnIdle 屬性
description: 針對腳本，取得或設定布林值，這個值會指出當電腦迴圈進入閒置條件超過一次時，是否要重新開機工作。
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- RestartOnIdle 屬性工作排程器
- RestartOnIdle 屬性工作排程器，IdleSettings 物件
- IdleSettings 物件工作排程器、RestartOnIdle 屬性
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa405ce4090a080106ec030acbe0ca7211b1c6f94e5874729226ce6adfafa652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760075"
---
# <a name="idlesettingsrestartonidle-property"></a>IdleSettings. RestartOnIdle 屬性

針對腳本，取得或設定布林值，這個值會指出當電腦迴圈進入閒置條件超過一次時，是否要重新開機工作。

## <a name="syntax"></a>Syntax


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a>屬性值

布林值，指出當電腦迴圈進入閒置條件超過一次時，是否必須重新開機工作。 預設值是 False。

## <a name="remarks"></a>備註

只有當 [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md) 屬性設定為 True 時，才會使用這個屬性。

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) 元素中指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 






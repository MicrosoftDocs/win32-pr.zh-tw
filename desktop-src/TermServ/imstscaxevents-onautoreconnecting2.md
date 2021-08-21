---
title: IMsTscAxEvents OnAutoReconnecting2 方法
description: 當用戶端正在自動重新連接具有遠端桌面工作階段主機 (RD 工作階段主機) server 的會話時呼叫。 |IMsTscAxEvents OnAutoReconnecting2 方法
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- OnAutoReconnecting2 方法遠端桌面服務
- OnAutoReconnecting2 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnAutoReconnecting2 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194c21fc8ddc6f93ac4816752956f8de5a1d5df71b3af98ddadf8aba48e421a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512488"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a>IMsTscAxEvents：： OnAutoReconnecting2 方法

當用戶端正在自動重新連接具有遠端桌面工作階段主機 (RD 工作階段主機) server 的會話時呼叫。 這是 [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) 方法的增強版本。

## <a name="syntax"></a>語法


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*disconnectReason* \[在\]
</dt> <dd>

描述上次會話中斷連接原因的程式碼。

</dd> <dt>

*networkAvailable* \[在\]
</dt> <dd>

指定網路是否可用。

</dd> <dt>

*了 attemptcount* \[在\]
</dt> <dd>

目前自動重新連接程式中所做的嘗試次數。 每次嘗試時，此計數都會增加一個。

</dd> <dt>

*maxAttemptCount* \[在\]
</dt> <dd>

目前自動重新連線程式中將會進行的嘗試次數上限。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 






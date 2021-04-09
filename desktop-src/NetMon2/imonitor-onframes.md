---
description: OnFrames 方法必須由監視器所執行。 當 capture 緩衝區已滿或更新時間通過時，MCSVC 會呼叫這個方法。
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'IMonitor：： OnFrames 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c5b6ff3e9d5b97a228e6e1d865fe4d8f1b5bfc9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690220"
---
# <a name="imonitoronframes-method"></a>IMonitor：： OnFrames 方法

**OnFrames** 方法必須由監視器所執行。 當 capture 緩衝區已滿或更新時間通過時，MCSVC 會呼叫這個方法。

## <a name="syntax"></a>語法


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*活動* \[在\]
</dt> <dd>

[更新 \_](update-event.md)包含用來更新事件的框架資訊的事件結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同。 MCSVC 會將傳回的值傳遞回 NPP 進行處理。

如果此方法不成功，則傳回值會是錯誤碼。 MCSVC 會將傳回的值傳遞回 NPP 進行處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 





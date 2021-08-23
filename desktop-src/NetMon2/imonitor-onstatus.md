---
description: MCSVC 方法會呼叫 OnStatus 方法，以通知監視器有 NPP 狀態事件存在。 此方法必須由監視器所執行。
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'IMonitor：： OnStatus 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 2a82594400bebc8a529290e0e0e881603172aa45c111d2d4d83ebcbd5ebfbeb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779038"
---
# <a name="imonitoronstatus-method"></a>IMonitor：： OnStatus 方法

MCSVC 方法會呼叫 **OnStatus** 方法，以通知監視器有 NPP 狀態事件存在。 此方法必須由監視器所執行。

## <a name="syntax"></a>語法


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*活動* \[在\]
</dt> <dd>

[UPDATE \_ 事件](update-event.md)結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同，而且 MCSVC 會將傳回的值傳回到 NPP 進行處理。

如果方法失敗，則傳回錯誤碼。 發生錯誤時，MCSVC 會將傳回的值傳遞回 NPP 進行處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 





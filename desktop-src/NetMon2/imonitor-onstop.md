---
description: OnStop 方法必須由監視器所執行。 MSCVC 會呼叫這個方法，以通知監視器將會停止該捕獲。
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'IMonitor：： OnStop 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a737aa5bede443b63f2074239eec17ea8a205cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972594"
---
# <a name="imonitoronstop-method"></a>IMonitor：： OnStop 方法

**OnStop** 方法必須由監視器所執行。 MSCVC 會呼叫這個方法，以通知監視器將會停止該捕獲。

## <a name="syntax"></a>語法


```C++
HRESULT OnStop();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同。

如果此方法不成功，則傳回值會是錯誤碼。 傳回錯誤碼時，無法重新開機監視。

## <a name="remarks"></a>備註

MCSVC 會在呼叫 [IRTC：： Stop](irtc-stop.md) 之後呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 





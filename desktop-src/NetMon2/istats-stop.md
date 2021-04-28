---
description: IStats：： Stop 方法-Stop 方法會停止目前的捕捉。
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'IStats：： Stop 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ef51aff870a3193963b3802332112c51f1024826
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114606"
---
# <a name="istatsstop-method"></a>IStats：： Stop 方法

**Stop** 方法會停止目前的捕捉。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                            | Description                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>   | NPP 未連接到網路。 呼叫 [IStats：： connect](istats-connect.md) 方法，將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl>   | NPP 不會捕捉資料。 呼叫 [IStats：： start](istats-start.md) 方法來啟動 capture。<br/>                            |
| <dl> <dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt> </dl> | NPP 已連接到網路，但不是使用 [IStats：： Connect](istats-connect.md) 方法。<br/>                                |



 

## <a name="remarks"></a>備註

在呼叫 **IStats：： Stop** 之後重新開機 capture 時，請務必在每次呼叫 [IStats：： Start](istats-start.md)以重新開機捕獲時，呼叫 [IStats：： Configure](istats-configure.md)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats：： Connect](istats-connect.md)
</dt> <dt>

[IStats：： Configure](istats-configure.md)
</dt> <dt>

[IStats：： Start](istats-start.md)
</dt> </dl>

 

 





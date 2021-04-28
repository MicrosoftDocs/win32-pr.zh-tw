---
description: IStats：： Resume 方法-Resume 方法會重新開機已暫停的捕獲。
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'IStats：： Resume 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ee7818da3d8a02e41488d473d3cf26607d3b84ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114616"
---
# <a name="istatsresume-method"></a>IStats：： Resume 方法

**Resume** 方法會重新開機已暫停的捕獲。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                                | Description                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>       | NPP 未連接到網路。<br/>                                                                                          |
| <dl> <dt>**NMERR \_ CAPTURE \_ 未 \_ 暫停**</dt> </dl> | 捕捉未暫停。 呼叫 [IStats：:P ause](istats-pause.md) 方法以暫時停止捕捉。<br/>                     |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>       | NPP 未連接到網路。 呼叫 [IStats：： connect](istats-connect.md) 方法，將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt> </dl>     | NPP 已連接到網路，但不是使用 [IStats：： Connect](istats-connect.md) 方法。<br/>                                |



 

## <a name="remarks"></a>備註

當捕捉處於暫停狀態時，在呼叫 IStats：： Resume 方法來重新開機 capture 之前，不會捕獲新的資料。

使用 **Pause** 和 **Resume** 方法來控制捕捉時，網路監視器會繼續將 [*對話統計資料*](c.md) 新增至目前 capture 的現有統計資料。

若要停止捕捉，請呼叫 [IStats：： stop](istats-stop.md)。

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

[IStats：:P ause](istats-pause.md)
</dt> <dt>

[IStats：： Stop](istats-stop.md)
</dt> </dl>

 

 





---
description: IDelaydC：： Resume 方法-Resume 方法會重新開機已暫停的捕獲。
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'IDelaydC：： Resume 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9c8c3b505e0e9fb306a444111cce22c8c580d015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109186"
---
# <a name="idelaydcresume-method"></a>IDelaydC：： Resume 方法

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



| 傳回碼                                                                                                | Description                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ 未 \_ 暫停**</dt> </dl> | 捕捉未暫停。 呼叫 [**IDelaydC：:P ause**](idelaydc-pause.md) 暫停捕捉。<br/>                                |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>       | NPP 未連接到網路。 呼叫 [**IDelaydC：： connect**](idelaydc-connect.md) 以將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 未 \_ 延遲**</dt> </dl>         | NPP 已連接到網路，但不是使用 [**IDelaydC：： Connect**](idelaydc-connect.md) 方法。<br/>                     |



 

## <a name="remarks"></a>備註

當捕捉暫停時，不會將新資料新增至目前的 [*capture*](c.md) 檔案，直到呼叫 **IDelaydC：： Resume** 方法來重新開機捕獲為止。 當 [**暫停**](idelaydc-pause.md) 和 **繼續** 用來停止並重新啟動捕獲時，所有捕獲的資訊都會放在相同的捕獲檔案中。

當使用 [ [**暫停**](idelaydc-pause.md) ] 和 [ **繼續** ] 來控制捕捉時，網路監視器會繼續將 [*對話統計資料*](c.md) 加入目前 capture 的現有統計資料。

若要停止捕捉，請呼叫 [**IDelaydC：： stop**](idelaydc-stop.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[**IDelaydC：： Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC：:P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC：： Stop**](idelaydc-stop.md)
</dt> </dl>

 

 





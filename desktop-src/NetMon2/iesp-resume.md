---
description: IESP：： Resume 方法-Resume 方法會重新開機已暫停的捕獲。
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'IESP：： Resume 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: dd39cb83c90c566f0022679e70680e916daeb2a43a4d62e993e096930ee2f14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890468"
---
# <a name="iespresume-method"></a>IESP：： Resume 方法

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



| 傳回碼                                                                                                | 描述                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ 未 \_ 暫停**</dt> </dl> | 捕捉未暫停。 呼叫 [**IESP：:P ause**](iesp-pause.md) 暫停捕捉。<br/>                        |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>       | NPP 未連接到網路。 呼叫 [**IESP：：連線**](iesp-connect.md)連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 非 \_ ESP**</dt> </dl>             | NPP 會連接到網路，但不會使用 [**IESP：：連線**](iesp-connect.md)方法。<br/>            |



 

## <a name="remarks"></a>備註

當捕捉處於暫停狀態時，在呼叫 **IESP：： Resume** 以重新開機 capture 之前，不會將新資料新增至目前的 [*capture*](c.md)檔案。 當 **暫停** 和 **繼續** 用來停止並重新啟動捕獲時，所有捕獲的資訊都會放在相同的捕獲檔案中。

當使用 [ **暫停** ] 和 [ **繼續** ] 來控制捕捉時，網路監視器會繼續將 [*對話統計資料*](c.md) 加入目前 capture 的現有統計資料。

若要停止捕捉，請呼叫 [**IESP：： stop**](iesp-stop.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[**IESP：：連線**](iesp-connect.md)
</dt> <dt>

[**IESP：:P ause**](iesp-pause.md)
</dt> <dt>

[**IESP：： Stop**](iesp-stop.md)
</dt> </dl>

 

 





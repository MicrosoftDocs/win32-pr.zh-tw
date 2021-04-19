---
description: Resume 方法會重新開機已暫停的捕獲。
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'IRTC：： Resume 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 991f70944b44ce13641318219788d9d6122b15c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987480"
---
# <a name="irtcresume-method"></a>IRTC：： Resume 方法

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



| 傳回碼                                                                                                | Description                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ 未 \_ 暫停**</dt> </dl> | 捕捉未暫停。 呼叫 [IRTC：:P ause](irtc-pause.md) 暫停捕捉。<br/>                                |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>       | NPP 未連接到網路。 呼叫 [IRTC：： connect](irtc-connect.md) 以將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 無法 \_ 即時**</dt> </dl>        | NPP 已連接到網路，但不是使用 [IRTC：： Connect](irtc-connect.md) 方法。<br/>                     |



 

## <a name="remarks"></a>備註

當捕捉處於暫停狀態時，在呼叫 [IRTC：： Resume](idelaydc-resume.md) 方法重新開機 capture 之前，不會建立新的資料。

使用 **Pause** 和 **Resume** 方法來控制捕捉時，網路監視器會繼續將 [*對話統計資料*](c.md) 新增至目前 capture 的現有統計資料。

若要停止捕捉，請呼叫 [IRTC：： stop](irtc-stop.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC：： Connect](irtc-connect.md)
</dt> <dt>

[IRTC：:P ause](irtc-pause.md)
</dt> <dt>

[IRTC：： Stop](irtc-stop.md)
</dt> </dl>

 

 





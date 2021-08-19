---
description: IRTC：:P ause 方法-Pause 方法會暫停目前的捕獲。
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: 'IRTC： (Netmon 的:P ause 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1ad7ce342c1e0053622bfb77161ecd1e5d81c25d09af179108065b445dd4dc35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365073"
---
# <a name="irtcpause-method"></a>IRTC：:P ause 方法

**Pause** 方法會暫停目前的捕獲。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                           | 描述                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt> </dl> | 此 capture 已經暫停。<br/>                                                                                     |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl>  | NPP 不會捕捉資料。 呼叫 [IRTC：： start](irtc-start.md) 以開始捕獲。<br/>                            |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>  | NPP 未連接到網路。 呼叫[IRTC：：連線](irtc-connect.md)將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 無法 \_ 即時**</dt> </dl>   | NPP 是連接到網路，但不是使用[IRTC：：連線](irtc-connect.md)方法。<br/>                     |



 

## <a name="remarks"></a>備註

當捕捉處於暫停狀態時，在呼叫 [IRTC：： Resume](irtc-resume.md) 方法以重新開機 capture 之前，不會先建立新的框架。

當您使用 **IRTC：:P ause** 和 **IRTC：： Resume** 方法來控制捕捉時，網路監視器會在每次執行時繼續新增 [*對話統計資料*](c.md) 。

若要重新開機 capture 呼叫 [IRTC：： Resume](irtc-resume.md)。 若要停止捕捉，請呼叫 [IRTC：： stop](irtc-stop.md)。

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

[IRTC：：連線](irtc-connect.md)
</dt> <dt>

[IRTC：： Resume](irtc-resume.md)
</dt> <dt>

[IRTC：： Start](irtc-start.md)
</dt> <dt>

[IRTC：： Stop](irtc-stop.md)
</dt> </dl>

 

 





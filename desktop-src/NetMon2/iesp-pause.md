---
description: IESP：:P ause 方法-Pause 方法會暫停目前的捕獲。
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: 'IESP： (Netmon 的:P ause 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 486c7aedc7092e0dd0f9f68cc1ea2ccad08d9438
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084236"
---
# <a name="iesppause-method"></a>IESP：:P ause 方法

**Pause** 方法會暫停目前的捕獲。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpStats* 
</dt> <dd>

已過時。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                           | Description                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt> </dl> | 此 capture 已經暫停。<br/>                                                                                     |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl>  | NPP 不會捕捉資料。 呼叫 [IESP：： start](iesp-start.md) 以開始捕獲。<br/>                            |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>  | NPP 未連接到網路。 呼叫 [IESP：： connect](iesp-connect.md) 以將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 非 \_ ESP**</dt> </dl>        | NPP 已連接到網路，但不是使用 [IESP：： Connect](iesp-connect.md) 方法。<br/>                     |



 

## <a name="remarks"></a>備註

當捕捉處於暫停狀態時，除非您呼叫 [IESP：： Resume](iesp-resume.md)方法來重新開機 capture，否則新的資料不會加入至目前的 [*capture*](c.md)檔。 當 **暫停** 和 **繼續** 用來停止並重新啟動捕獲時，所有捕獲的資訊都會放在相同的捕獲檔案中。

當您使用 **IESP：:P ause** 和 **IESP：： Resume** 方法來控制捕捉時，網路監視器會在每次執行時繼續新增 [*對話統計資料*](c.md) 。

若要重新開機捕獲，請呼叫 [IESP：： Resume](iesp-resume.md)。 若要停止捕捉，請呼叫 [IESP：： stop](iesp-stop.md)。

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

[IESP：： Connect](iesp-connect.md)
</dt> <dt>

[IESP：： Resume](iesp-resume.md)
</dt> <dt>

[IESP：： Start](iesp-start.md)
</dt> <dt>

[IESP：： Stop](iesp-stop.md)
</dt> </dl>

 

 





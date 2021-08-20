---
description: Pause 方法會暫時停止目前的捕獲。
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: 'IStats： (Netmon 的:P ause 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d1bab0d66a081c175d997e093d7dd1ff2b0d1c9622ecff73e0b3b1473edc885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495208"
---
# <a name="istatspause-method"></a>IStats：:P ause 方法

**Pause** 方法會暫時停止目前的捕獲。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                            | 描述                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt> </dl>  | 此 capture 已經暫停。<br/>                                                                                                    |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl>   | NPP 不會捕捉資料。 呼叫 [IStats：： start](istats-start.md) 方法來啟動 capture。<br/>                            |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>   | NPP 未連接到網路。 呼叫[IStats：：連線](istats-connect.md)方法，以將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt> </dl> | NPP 是連接到網路，但不是使用[IStats：：連線](istats-connect.md)方法。<br/>                                |



 

## <a name="remarks"></a>備註

當捕捉暫停時，除非呼叫 [IStats：： Resume](istats-resume.md) 方法重新開機 capture，否則不會捕獲新的框架。

當您使用 **IStats：:P ause** 和 **IStats：： Resume** 方法來控制捕捉時，網路監視器會在每次執行時繼續新增 [*對話統計資料*](c.md) 。

若要重新開機 capture 呼叫 [IStats：： Resume](istats-resume.md)。 若要停止捕捉，請呼叫 [IStats：： stop](istats-stop.md)。

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

[IStats：：連線](istats-connect.md)
</dt> <dt>

[IStats：： Resume](istats-resume.md)
</dt> <dt>

[IStats：： Start](istats-start.md)
</dt> <dt>

[IStats：： Stop](istats-stop.md)
</dt> </dl>

 

 





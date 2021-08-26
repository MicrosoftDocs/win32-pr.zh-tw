---
description: IStats：： Start 方法-Start 方法會啟動 capture。
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'IStats：： Start 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 494ec12a0bb9c5c312f34e9cc53e82bfcbe155f90c38b98b2ba807e9c87b6945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037148"
---
# <a name="istatsstart-method"></a>IStats：： Start 方法

**Start** 方法會啟動 capture。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                            | 描述                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt> </dl>  | Capture 已暫停，必須先停止，才能重新開機。 呼叫 [IStats：： stop](istats-stop.md) 方法以停止捕捉。<br/> |
| <dl> <dt>**NMERR \_ 捕獲**</dt> </dl>        | 已啟動 capture。<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>   | NPP 未連接到網路。 呼叫[IStats：：連線](istats-connect.md)方法，以將 NPP 連接到網路。<br/>           |
| <dl> <dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt> </dl> | NPP 是連接到網路，但不是使用[IStats：：連線](istats-connect.md)方法。<br/>                                          |



 

## <a name="remarks"></a>備註

使用 IStats：： Start 和 [IStats：： Stop](istats-stop.md) 方法重新開機捕捉時，您必須呼叫 [IStats：： Configure](istats-configure.md) 方法，以在每次呼叫 IStats：： start 重新開機資料捕獲時重新設定連接。

> [!Note]  
> 您也可以使用 [IStats：:P ause](istats-pause.md) 和 [IStats：： Resume](istats-resume.md) 方法來啟動和停止捕捉。 當您使用這些方法時，所捕獲的資料會儲存在相同的捕獲檔案中。

 

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

[IStats：： Configure](istats-configure.md)
</dt> <dt>

[IStats：：連線](istats-connect.md)
</dt> <dt>

[IStats：:P ause](istats-pause.md)
</dt> <dt>

[IStats：： Resume](istats-resume.md)
</dt> <dt>

[IStats：： Stop](istats-stop.md)
</dt> </dl>

 

 





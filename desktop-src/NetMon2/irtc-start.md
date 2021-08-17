---
description: Start 方法會啟動 capture。
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'IRTC：： Start 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 17ccb07a97112cab4390dc1eece2bf6fce51acf1c80244ed03253b5a2f6112b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132917"
---
# <a name="irtcstart-method"></a>IRTC：： Start 方法

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



| 傳回碼                                                                                           | 描述                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt> </dl> | 捕捉處於暫停狀態，必須先停止，才能重新開機。 呼叫 [IRTC：： stop](idelaydc-stop.md) 以停止捕捉。<br/> |
| <dl> <dt>**NMERR \_ 捕獲**</dt> </dl>       | 已啟動 capture。<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>  | NPP 未連接到網路。 呼叫[IRTC：：連線](irtc-connect.md)將 NPP 連接到網路。<br/>                         |
| <dl> <dt>**NMERR \_ 無法 \_ 即時**</dt> </dl>   | NPP 是連接到網路，但不是使用[IRTC：：連線](irtc-connect.md)方法。<br/>                                             |



 

## <a name="remarks"></a>備註

當您使用 IRTC：： Start 和 [IRTC：： Stop](irtc-stop.md) 方法重新開機捕捉時，您必須呼叫 [IRTC：： Configure](irtc-configure.md) 方法，以在每次呼叫 IRTC：： start 重新開機資料捕獲時重新設定連接。

> [!Note]  
> 您也可以使用 [IRTC：:P ause](irtc-pause.md) 和 [IRTC：： Resume](irtc-resume.md) 方法來啟動和停止捕捉。

 

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

[IRTC：： Configure](irtc-configure.md)
</dt> <dt>

[IRTC：：連線](irtc-connect.md)
</dt> <dt>

[IRTC：:P ause](irtc-pause.md)
</dt> <dt>

[IRTC：： Resume](irtc-resume.md)
</dt> <dt>

[IRTC：： Stop](irtc-stop.md)
</dt> </dl>

 

 





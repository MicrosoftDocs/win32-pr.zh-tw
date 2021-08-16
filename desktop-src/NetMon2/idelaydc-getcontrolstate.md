---
description: IDelaydC：： GetControlState 方法-GetControlState 方法會抓取 capture 的狀態，以指出正在執行或暫停捕捉。
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: 'IDelaydC：： GetControlState 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 34302215cf0e773d7713f56233d38462071f1dde725a85478688cfb9ca2a4f45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365891"
---
# <a name="idelaydcgetcontrolstate-method"></a>IDelaydC：： GetControlState 方法

**GetControlState** 方法會 [*抓取 capture*](c.md)的狀態，以指出 capture 是否正在執行或已暫停。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IsRunnning* \[擴展\]
</dt> <dd>

目前正在執行之捕捉的指標，包括是否暫停捕捉。

</dd> <dt>

*IsPaused* \[擴展\]
</dt> <dd>

指標，表示目前的捕獲已暫停。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                          | Description                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl> | NPP 未連接到網路。 呼叫[IDelaydC：：連線](idelaydc-connect.md)將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 未 \_ 延遲**</dt> </dl>   | NPP 是連接到網路，但不是使用[IDelaydC：：連線](idelaydc-connect.md)方法。<br/>                     |



 

## <a name="remarks"></a>備註

只要使用 [IDelaydC](idelaydc.md) 介面將 NPP 連接到網路，就可以呼叫這個方法。 您可以使用這個方法來找出正在執行的捕捉、捕捉是否已暫停，或是已停止 capture 但 NPP 未中斷連線。

用來啟動、暫停和停止捕捉的方法會列在下列 [另請參閱] 清單中。

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

[IDelaydC：：連線](idelaydc-connect.md)
</dt> <dt>

[IDelaydC：:P ause](idelaydc-pause.md)
</dt> <dt>

[IDelaydC：： Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC：： Stop](idelaydc-stop.md)
</dt> </dl>

 

 





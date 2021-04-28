---
description: IDelaydC：:P ause 方法-Pause 方法會暫停目前的捕獲。
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: 'IDelaydC： (Netmon 的:P ause 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 21b4cd7b6cb921f7bd71b8670a37da12b2239b92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098496"
---
# <a name="idelaydcpause-method"></a>IDelaydC：:P ause 方法

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



| 傳回碼                                                                                           | Description                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE 已 \_ 暫停**</dt> </dl> | 此捕獲已處於暫停狀態。<br/>                                                                                  |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl>  | NPP 不會捕捉資料。 呼叫 [IDelaydC：： start](idelaydc-start.md) 以開始捕獲。<br/>                            |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>  | NPP 未連接到網路。 呼叫 [IDelaydC：： connect](idelaydc-connect.md) 以將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 未 \_ 延遲**</dt> </dl>    | NPP 已連接到網路，但不是使用 [IDelaydC：： Connect](idelaydc-connect.md) 方法。<br/>                     |



 

## <a name="remarks"></a>備註

當捕捉處於暫停狀態時，在呼叫 **IDelaydC：： Resume** 方法來重新開機 capture 之前，不會將新的資料加入至目前的 [*capture*](c.md)檔。 當 **暫停** 和 **繼續** 用來停止並重新啟動捕獲時，所有捕獲的資訊都會放在相同的捕獲檔案中。

使用 **IDelaydC：:P ause** 和 **IDelaydC：： Resume** 來控制捕捉時，網路監視器會在每次執行時繼續新增 [*對話統計資料*](c.md) 。

若要重新開機捕獲，請呼叫 [IDelaydC：： Resume](idelaydc-resume.md)。

若要停止捕捉，請呼叫 [IDelaydC：： stop](idelaydc-stop.md)。

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

[IDelaydC：： Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC：： Resume](idelaydc-resume.md)
</dt> <dt>

[IDelaydC：： Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC：： Stop](idelaydc-stop.md)
</dt> </dl>

 

 





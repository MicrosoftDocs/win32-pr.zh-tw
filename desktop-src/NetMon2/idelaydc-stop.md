---
description: IDelaydC：： Stop 方法-Stop 方法會停止目前的捕捉。
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'IDelaydC：： Stop 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b5fb6442481574de6732aef1359cf9586b9cdcc1815d9f0b206a1f8a597f1967
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365998"
---
# <a name="idelaydcstop-method"></a>IDelaydC：： Stop 方法

**Stop** 方法會停止目前的捕捉。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpStats* \[擴展\]
</dt> <dd>

[統計資料](statistics.md)結構的指標，其中包含網路統計資料，例如總畫面格總數和已捕獲的位元組總數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                          | Description                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl> | NPP 未連接到網路。 呼叫[IDelaydC：：連線](idelaydc-connect.md)將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl> | NPP 不會捕捉資料。 呼叫 [IDelaydC：： start](idelaydc-start.md) 以開始捕獲。<br/>                            |
| <dl> <dt>**NMERR \_ 未 \_ 延遲**</dt> </dl>   | NPP 是連接到網路，但不是使用[IDelaydC：：連線](idelaydc-connect.md)方法。<br/>                     |



 

## <a name="remarks"></a>備註

當呼叫 **IDelaydC：： Stop** 時，網路監視器會停止捕獲資料並關閉 [*capture*](c.md)檔案。  (在呼叫 [IDelaydC：： Start](idelaydc-start.md) 時傳回的 capture 檔名稱) 。 您現在可以查看 capture 檔案的內容。

當您停止並開始進行捕捉時，請務必在每次呼叫[IDelaydC：： start](idelaydc-start.md)以重新開機捕獲時呼叫[IDelaydC：： Configure](idelaydc-configure.md)方法。

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

[IDelaydC：： Configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC：： Start](idelaydc-start.md)
</dt> <dt>

[統計](statistics.md)
</dt> </dl>

 

 





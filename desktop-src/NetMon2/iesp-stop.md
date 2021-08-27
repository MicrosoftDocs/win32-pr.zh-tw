---
description: IESP：： Stop 方法-Stop 方法會停止目前的捕捉。
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'IESP：： Stop 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d22333bcaad688fa9ebb805857db3673f48e70591e1d8953274598acef2b368b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037508"
---
# <a name="iespstop-method"></a>IESP：： Stop 方法

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



| 傳回碼                                                                                          | 描述                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl> | NPP 未連接到網路。 呼叫[IESP：：連線](iesp-connect.md)將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl> | NPP 不會捕捉資料。 呼叫 [IESP：： start](iesp-start.md) 以開始捕獲。<br/>                            |
| <dl> <dt>**NMERR \_ 非 \_ ESP**</dt> </dl>       | NPP 是連接到網路，但不是使用[IESP：：連線](iesp-connect.md)方法。<br/>                     |



 

## <a name="remarks"></a>備註

呼叫 **IESP：： Stop** 方法時，網路監視器會停止捕捉資料並關閉 capture 檔案 [*。*](c.md)  (在呼叫 [IESP：： Start](iesp-start.md) 時傳回的 capture 檔名稱。 ) 您現在可以查看 capture 檔案的內容。

當您停止並重新啟動捕捉時，請務必在每次呼叫[IESP：： Start](iesp-start.md)以重新開機捕獲時，呼叫[IESP：： Configure](iesp-configure.md)方法。

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

[IESP：：連線](iesp-connect.md)
</dt> <dt>

[IESP：： Start](iesp-start.md)
</dt> <dt>

[統計](statistics.md)
</dt> </dl>

 

 





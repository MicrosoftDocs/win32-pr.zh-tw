---
description: IRTC：： Stop 方法-Stop 方法會停止目前的捕捉。
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'IRTC：： Stop 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 10bf0886032c93288435ade05fec46077d53753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113516"
---
# <a name="irtcstop-method"></a>IRTC：： Stop 方法

**Stop** 方法會停止目前的捕捉。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                          | Description                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl> | NPP 未連接到網路。 呼叫 [IRTC：： connect](irtc-connect.md) 以將 NPP 連接到網路。<br/> |
| <dl> <dt>**NMERR \_ 未 \_ 捕獲**</dt> </dl> | NPP 不會捕捉資料。 呼叫 [IRTC：： start](irtc-start.md) 以開始捕獲。<br/>                            |
| <dl> <dt>**NMERR \_ 無法 \_ 即時**</dt> </dl>  | NPP 已連接到網路，但不是使用 [IRTC：： Connect](irtc-connect.md) 方法。<br/>                     |



 

## <a name="remarks"></a>備註

當您在呼叫 **IRTC：： Stop** 方法之後重新開機 capture 時，請務必在每次呼叫 [IRTC：： Start](irtc-start.md)以重新開機捕獲時，呼叫 [IRTC：： Configure](irtc-configure.md) 。

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

[IRTC：： Configure](irtc-configure.md)
</dt> <dt>

[IRTC：： Start](irtc-start.md)
</dt> </dl>

 

 





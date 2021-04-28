---
description: IRTC：:D isconnect 方法-中斷連線方法會中斷 NPP 與網路的連線。
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: 'IRTC： (Netmon 的:D isconnect 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 43acb88e2c7b6108a162c4715de02375121021f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110716"
---
# <a name="irtcdisconnect-method"></a>IRTC：:D isconnect 方法

**中斷** 連線方法會中斷 NPP 與網路的連線。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值是下列其中一個錯誤碼：



| 傳回碼                                                                                          | Description                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 捕獲**</dt> </dl>      | NPP 正在捕獲資料。 當資料捕捉正在進行中時，您無法中斷與網路的連線。<br/> |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl> | NPP 未連接到網路。<br/>                                                                 |
| <dl> <dt>**NMERR \_ 無法 \_ 即時**</dt> </dl>  | NPP 已連接到網路，但不是使用 [IRTC：： Connect](irtc-connect.md) 方法。<br/>           |



 

## <a name="remarks"></a>備註

當 NPP 正在捕捉資料時，無法呼叫這個方法。 呼叫 IRTC：:D isconnect 之前，您必須先呼叫 [IRTC：： Stop](irtc-stop.md) 方法。

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

[IRTC：： Stop](irtc-stop.md)
</dt> </dl>

 

 





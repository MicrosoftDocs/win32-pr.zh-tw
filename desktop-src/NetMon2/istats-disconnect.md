---
description: 中斷 NPP 與網路的連線。
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: 'IStats： (Netmon 的:D isconnect 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a5fa56c05036380b5dba42089979b43d776a4b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997850"
---
# <a name="istatsdisconnect-method"></a>IStats：:D isconnect 方法

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



| 傳回碼                                                                                            | Description                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 捕獲**</dt> </dl>        | NPP 目前正在捕獲資料。 當資料捕捉正在進行中時，您無法中斷與網路的連線。<br/> |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl>   | NPP 未連接到網路。<br/>                                                                         |
| <dl> <dt>**NMERR \_ 不是 \_ 統計資料 \_**</dt> </dl> | NPP 已連接到網路，但不是使用 [**IStats：： Connect**](istats-connect.md) 方法。<br/>          |



 

## <a name="remarks"></a>備註

當 NPP 正在捕捉資料時，無法呼叫這個方法。 先呼叫 **IStats：:D isconnect** 方法，然後呼叫 [**IStats：： Stop**](istats-stop.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats：： Connect**](istats-connect.md)
</dt> <dt>

[**IStats：： Stop**](istats-stop.md)
</dt> </dl>

 

 





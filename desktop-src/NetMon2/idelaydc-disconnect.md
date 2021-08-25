---
description: IDelaydC：:D isconnect 方法-中斷連線方法會中斷 NPP 與網路的連線。
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: 'IDelaydC： (Netmon 的:D isconnect 方法) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ad24ad2557401509c1bc1e076a545f05d1c03dd79fbcf73a05d3efccfdfb8886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910668"
---
# <a name="idelaydcdisconnect-method"></a>IDelaydC：:D isconnect 方法

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



| 傳回碼                                                                                          | 描述                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 捕獲**</dt> </dl>      | NPP 正在捕獲資料。 在捕捉期間，您無法中斷 NPP 與網路的連線。<br/>            |
| <dl> <dt>**NMERR \_ 未 \_ 連接**</dt> </dl> | NPP 未連接到網路。<br/>                                                               |
| <dl> <dt>**NMERR \_ 未 \_ 延遲**</dt> </dl>   | NPP 是連接到網路，但不是使用[IDelaydC：：連線](idelaydc-connect.md)方法。<br/> |



 

## <a name="remarks"></a>備註

當 NPP 正在捕捉資料時，無法呼叫這個方法。 呼叫 **中斷連接** 之前，您必須先呼叫 **IDelaydC：： Stop** 方法。

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

[IDelaydC：： Stop](idelaydc-stop.md)
</dt> </dl>

 

 





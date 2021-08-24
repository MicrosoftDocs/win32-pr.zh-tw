---
description: SetAddressInfo 方法會設定位址資訊。
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: 'ITConnection：： SetAddressInfo 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d90fd6e92e115966df709626b7b58c739d292fedca4fb855999bc3fd8cd853b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774928"
---
# <a name="itconnectionsetaddressinfo-method"></a>ITConnection：： SetAddressInfo 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**SetAddressInfo** 方法會設定位址資訊。

## <a name="syntax"></a>語法


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStartAddress* \[在\]
</dt> <dd>

包含起始位址之 **BSTR** 的指標。

</dd> <dt>

*NumAddresses* \[在\]
</dt> <dd>

要用於會話的位址數目。

</dd> <dt>

*Ttl* \[在\]
</dt> <dd>

 (TTL) 位址上的傳輸範圍的生存 [*時間*](t-tapgloss.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PStartAddress*、 *NumAddresses* 或 *Ttl* 參數無效。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>                  |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                                    |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                                   |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pStartAddress* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 


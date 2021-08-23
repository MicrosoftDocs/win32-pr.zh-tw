---
description: Put \_ MachineAddress 方法會設定來源主機的電腦位址。
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: 'ITSdp：:p ut_MachineAddress 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974286e846268686423d0ebdbbd083d07e9946401cb0192713b200b2354b89c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060796"
---
# <a name="itsdpput_machineaddress-method"></a>ITSdp：:p 的 \_ MachineAddress 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Put \_ MachineAddress** 方法會設定來源主機的電腦位址。

## <a name="syntax"></a>語法


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMachineAddress* \[在\]
</dt> <dd>

包含會議主機之電腦位址之 **BSTR** 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                       |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PMachineAddress* 參數不是有效的指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>    |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                      |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                     |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pMachineAddress* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。

*PMachineAddress* 參數可以是 DNS 名稱 ( "JohnSmith.workinghard.microsoft.com" ) 或 ( "10.111.222.111" ) 的 IP 位址。

此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。 使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp：： get \_ MachineAddress**](itsdp-get-machineaddress.md)
</dt> </dl>

 


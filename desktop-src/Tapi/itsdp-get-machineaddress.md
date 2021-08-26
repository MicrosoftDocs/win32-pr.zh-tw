---
description: Get \_ MachineAddress 方法會取得來源主機的電腦位址。
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: 'ITSdp：： get_MachineAddress 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4e4d849c17d6c371a6edc927679e2ba6af344fbf8515310eb22b27ba4abeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012928"
---
# <a name="itsdpget_machineaddress-method"></a>ITSdp：： get \_ MachineAddress 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ MachineAddress** 方法會取得來源主機的電腦位址。

## <a name="syntax"></a>語法


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppMachineAddress* \[擴展\]
</dt> <dd>

包含會議主機之電腦位址之 **BSTR** 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                        |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PpMachineAddres* s 參數不是有效的指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>     |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                       |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                      |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppMachineAddress* 參數的記憶體。

*PpMachineAddress* 參數可以做為 DNS 名稱 ( "JohnSmith.workinghard.microsoft.com" ) 或 ( "10.111.222.111" ) 的 IP 位址傳回。

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

[**ITSdp：:p 的 \_ MachineAddress**](itsdp-put-machineaddress.md)
</dt> </dl>

 


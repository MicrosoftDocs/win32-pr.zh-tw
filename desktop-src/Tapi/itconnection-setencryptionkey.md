---
description: SetEncryptionKey 方法會設定解密會話所需的加密金鑰，或用來取得以外部方式取得可用金鑰之機制的指示。
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'ITConnection：： SetEncryptionKey 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36b3fc9e37338b17aa00d19213118b1243ec70d2f21d21060fdd43894121566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406128"
---
# <a name="itconnectionsetencryptionkey-method"></a>ITConnection：： SetEncryptionKey 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**SetEncryptionKey** 方法會設定解密會話所需的加密金鑰，或用來取得以外部方式取得可用金鑰之機制的指示。

## <a name="syntax"></a>語法


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pKeyType* \[在\]
</dt> <dd>

包含加密金鑰類型之 **BSTR** 的指標。

</dd> <dt>

*ppKeyData* \[在\]
</dt> <dd>

包含加密金鑰資訊之 **BSTR** 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                          | 描述                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 方法成功。<br/> |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 來配置 *pKeyType* 和 *ppKeyData* 參數的記憶體。 當不再需要變數時，應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。

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

 


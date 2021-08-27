---
description: 傳回已安裝安全通訊端層通訊協定 (SSL) 通訊協定提供者的陣列。
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: 'SslEnumProtocolProviders 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c0e20bd98f8f3e76d4185cf2a3aa52985d73f66ff1ea61ed50bf67552330290d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906680"
---
# <a name="sslenumprotocolproviders-function"></a>SslEnumProtocolProviders 函式

**SslEnumProtocolProviders** 函式會傳回已安裝 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者的陣列。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdwProviderCount* \[擴展\]
</dt> <dd>

**DWORD** 值的指標，用來接收傳回的通訊協定提供者數目。

</dd> <dt>

*ppProviderList* \[擴展\]
</dt> <dd>

接收 [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) 結構陣列的緩衝區指標。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | Description                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_錯誤的 \_ 旗標**</dt> <dt>0x80090009L</dt> </dl>         | *DwFlags* 參數不是零。<br/>                              |
| <dl> 不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt> </dl>         | 可用的記憶體不足，無法配置必要的緩衝區。<br/>     |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *PdwProviderCount* 或 *PpProviderList* 參數為 **Null**。<br/> |



 

## <a name="remarks"></a>備註

當您完成使用 [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) 結構的陣列時，請呼叫 [**SslFreeBuffer**](sslfreebuffer.md) 函數來釋放陣列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 


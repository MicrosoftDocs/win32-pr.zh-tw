---
description: 抓取安全通訊端層通訊協定 (SSL) 提供者金鑰組象的命名屬性值。
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: 'SslGetKeyProperty 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990400"
---
# <a name="sslgetkeyproperty-function"></a>SslGetKeyProperty 函式

**SslGetKeyProperty** 函式會 (SSL) 提供者金鑰組象，抓取 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly)的命名屬性值。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hKey* \[在\]
</dt> <dd>

SSL 提供者的控制碼。

</dd> <dt>

*pszProperty* \[在\]
</dt> <dd>

以 null 終止的 Unicode 字串指標，其中包含要取出的屬性名稱。 這可以是其中一個預先定義的 [**金鑰存放區屬性識別碼**](key-storage-property-identifiers.md) 或自訂屬性識別碼。

</dd> <dt>

*ppbOutput* \[擴展\]
</dt> <dd>

接收屬性值之緩衝區的指標。 函式的呼叫者必須藉由呼叫 [**SslFreeBuffer**](sslfreebuffer.md) 函式來釋放此緩衝區。

</dd> <dt>

*pcbOutput* \[擴展\]
</dt> <dd>

*PbOutput* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | Description                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | 其中一個提供的控制碼無效。<br/>    |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | 其中一個提供的參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 


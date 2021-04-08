---
description: 抓取所指定提供者屬性的值。
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: 'SslGetProviderProperty 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851551"
---
# <a name="sslgetproviderproperty-function"></a>SslGetProviderProperty 函式

**SslGetProviderProperty** 函式會捕獲指定之提供者屬性的值。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSslProvider* \[在\]
</dt> <dd>

[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 提供者的控制碼，以取得此屬性。

</dd> <dt>

*pszProperty* \[在\]
</dt> <dd>

以 null 終止的 Unicode 字串指標，其中包含要取出的屬性名稱。

</dd> <dt>

*ppbOutput* \[擴展\]
</dt> <dd>

接收屬性值的緩衝區位址。

函式的呼叫者必須藉由呼叫 [**SslFreeBuffer**](sslfreebuffer.md) 函式來釋放此緩衝區。

</dd> <dt>

*pcbOutput* \[擴展\]
</dt> <dd>

*PbOutput* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*ppEnumState* \[in、out\]
</dt> <dd>

**VOID** 指標的位址，這個位址會接收此函式後續呼叫中所使用的列舉狀態資訊。 這項資訊只對 SSL 提供者有意義，對呼叫端而言是不透明的。 SSL 提供者會使用這項資訊來判斷列舉中的下一個專案。 如果這個參數所指向的變數包含 **Null**，則會從頭開始列舉。

函式的呼叫者必須藉由呼叫 [**SslFreeBuffer**](sslfreebuffer.md) 函式來釋放此記憶體。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | Description                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt> </dl>         | 可用的記憶體不足，無法配置必要的緩衝區。<br/> |
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | *HSslProvider* 控制碼無效。<br/>                       |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | 其中一個提供的參數無效。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 


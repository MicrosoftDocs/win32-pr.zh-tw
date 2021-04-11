---
description: 開啟指定安全通訊端層通訊協定 (SSL) 通訊協定提供者的控制碼。
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: 'SslOpenProvider 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191261"
---
# <a name="sslopenprovider-function"></a>SslOpenProvider 函式

**SslOpenProvider** 函式會開啟指定 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 通訊協定提供者的控制碼。

## <a name="syntax"></a>語法


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phSslProvider* \[擴展\]
</dt> <dd>

要在其中寫入提供者控制碼的 **NCRYPT \_ >prov \_ 控制碼** 位址。

當您完成使用控制碼時，您應該呼叫 [**SslFreeObject**](sslfreeobject.md) 函式來釋放它。

</dd> <dt>

*pszProviderName* \[在\]
</dt> <dd>

Unicode 字串的指標，其中包含提供者名稱。 如果這個參數的值為 **Null**，則會傳回 **MS \_ SCHANNEL \_ 提供者** 的控制碼。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

此參數會保留供日後使用，且必須設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則會傳回零。

如果函式失敗，則會傳回非零的錯誤值。

可能的傳回碼包括（但不限於）下列各項。



| 傳回碼/值                                                                                                                                                       | Description                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> 不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt> </dl>    | 其中一個提供的控制碼無效。<br/>                      |
| <dl> 不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt> </dl> | *PhSslProvider* 或 *PpProviderList* 參數為 **Null**。<br/> |
| <dl> <dt>**狀態 \_沒有 \_ 記憶體**</dt> <dt>0xC0000017L</dt> </dl>      | 可用的記憶體不足，無法配置必要的緩衝區。<br/>  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Sslprovider。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 


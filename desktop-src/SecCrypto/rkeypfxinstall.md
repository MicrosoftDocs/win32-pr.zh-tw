---
description: 不支援 RKeyPFXInstall 函數。
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: 'RKeyPFXInstall 函式 (Rkeysvcc) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943441"
---
# <a name="rkeypfxinstall-function"></a>RKeyPFXInstall 函式

不支援 **RKeyPFXInstall** 函數。

**Windows Server 2003：****RKeyPFXInstall** 函式會在遠端電腦上安裝憑證。 請注意，此行為已隨著 Windows Server 2003 Service Pack 1 (SP1) 而變更。

## <a name="syntax"></a>語法


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hKeySvcCli* \[在\]
</dt> <dd>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)先前開啟的 [**KEYSVCC \_ 句**](keysvcc-handle.md)柄控制碼。 控制碼代表將接收憑證的遠端電腦。 此值不可以是 **Null**。

</dd> <dt>

*pPFX* \[在\]
</dt> <dd>

[**KEYSVC \_ BLOB**](keysvc-blob.md)結構的指標，代表要安裝的憑證。 BLOB 採用 [*PKCS \# 12*](../secgloss/p-gly.md) 格式。

</dd> <dt>

*pPassword* \[在\]
</dt> <dd>

[**KEYSVC \_ UNICODE \_ 字串**](keysvc-unicode-string.md)結構的指標，表示 BLOB 的密碼。 當您使用完密碼之後，請呼叫 [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) 函式來清除記憶體中的密碼。 如需保護密碼的詳細資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。

</dd> <dt>

*ulFlags* \[在\]
</dt> <dd>

指定憑證安裝選項的旗標。 這個參數可以是零或下列值的組合。



| 值                                                                                                                                                                                                                                     | 意義                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <dt>**CRYPT \_可匯出**</dt><dt></dt> </dl>              | 匯入的金鑰會標記為可匯出。<br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <dt>**CRYPT \_電腦 \_ 金鑰集**</dt><dt></dt> </dl> | 私密金鑰會儲存在遠端電腦上，而不是在目前的使用者底下。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 S \_ OK。

如果函式失敗，則傳回值為 **ULONG** ，表示錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Rkeysvcc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 

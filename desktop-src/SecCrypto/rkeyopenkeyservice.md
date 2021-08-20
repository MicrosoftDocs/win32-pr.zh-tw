---
description: 不支援 RKeyOpenKeyService 函數。
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: 'RKeyOpenKeyService 函式 (Rkeysvcc) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: bbcd0edea891ba500cbed366121d333f45e34491f1d140af8cee59f7957d98cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974826"
---
# <a name="rkeyopenkeyservice-function"></a>RKeyOpenKeyService 函式

不支援 **RKeyOpenKeyService** 函數。

**Windows Server 2003：****RKeyOpenKeyService** 函式會建立與遠端電腦的連線，並開啟金鑰服務控制碼。 然後， [**RKeyPFXInstall**](rkeypfxinstall.md) 函式可以使用金鑰服務控制碼。 請注意，這種行為隨著 Windows Server 2003 Service Pack 1 (SP1) 而有所變更。

## <a name="syntax"></a>語法


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszMachineName* \[在\]
</dt> <dd>

表示將開啟金鑰服務控制碼的電腦之以 null 結束之字串的長指標。

</dd> <dt>

擁有 *擁有者* \[在\]
</dt> <dd>

[**KEYSVC \_**](keysvc-type.md)代表索引鍵類型的類型值。 唯一支援的值為 **KeySvcMachine**。

</dd> <dt>

*pwszOwnerName* \[在\]
</dt> <dd>

保留的。 將此值設定為 **Null**。

</dd> <dt>

*pAuthentication* \[在\]
</dt> <dd>

**Void** 的指標，表示驗證設定。 此指標可以指向值為零或以下的值。



| 值                                                                                                                                                                                                                                                           | 意義                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <dt>**RKEYSVC \_\_ \_ 僅連接安全**</dt><dt></dt> </dl> | 用戶端需要相互驗證。 如果指定此值，則回復到 NTLM 將會失敗。<br/> |



 

</dd> <dt>

*保留* \[in、out\]
</dt> <dd>

保留的。 將此值設定為 **Null**。

</dd> <dt>

*phKeySvcCli* \[擴展\]
</dt> <dd>

[**KEYSVCC \_ 控制碼**](keysvcc-handle.md)的指標，該控制碼會接收開啟的金鑰服務控制碼。 當您完成使用控制碼時，請呼叫 [**RKeyCloseKeyService**](rkeyclosekeyservice.md) 函式來釋放資源。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 S \_ OK。

如果函式失敗，則傳回值為 **ULONG** ，表示錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Rkeysvcc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 





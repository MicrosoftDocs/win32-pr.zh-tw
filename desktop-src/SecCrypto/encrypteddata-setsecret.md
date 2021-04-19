---
description: 設定用來衍生加密和解密資料的密碼編譯工作階段金鑰的秘密值。
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: A. >client.setsecret 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982920"
---
# <a name="encrypteddatasetsecret-method"></a>A. >client.setsecret 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) 和 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) ，以加密和解密訊息。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**>client.setsecret** 方法會設定秘密的值，用來衍生用來加密和解密資料的密碼編譯 [*工作階段金鑰*](../secgloss/s-gly.md)。

## <a name="syntax"></a>語法


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*newVal* \[在\]
</dt> <dd>

包含用來建立會話密碼編譯金鑰之密碼的字串。

</dd> <dt>

*SecretType* \[在中，選擇性\]
</dt> <dd>

[**CAPICOM \_ 秘密 \_ 類型**](capicom-secret-type.md)列舉的值，表示用來產生工作階段金鑰的秘密種類。 預設值是 [CAPICOM \_ 秘密 \_ 密碼]。 此參數可為下列值。



| 值                                                                                                                                                                                        | 意義                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**CAPICOM \_ 秘密 \_ 密碼**</dt> </dl> | 加密金鑰是衍生自密碼。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

秘密可用來建立用於加密或解密的工作階段金鑰。 這兩個作業都必須使用相同的密碼。 如果用來加密資料的密碼遺失，則無法解密加密的資料。

如果適用于您的應用程式，請考慮使用 [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) 或 [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) ，以在使用之前和之後保護秘密。 完成時清除與秘密相關聯的記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> <dt>

[**A**](encrypteddata.md)
</dt> </dl>

 

 

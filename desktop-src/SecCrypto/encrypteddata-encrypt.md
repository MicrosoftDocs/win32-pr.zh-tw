---
description: 從秘密衍生工作階段金鑰，並使用該金鑰來加密 Content 屬性值。 它會以編碼字串的形式傳回加密的內容。
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
title: A) 加密方法 (Infocard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 04d7bf8a337c1bcfa0a024b84304fe50c035f9dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985978"
---
# <a name="encrypteddataencrypt-method"></a>A 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) 和 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) ，以加密和解密訊息。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**Encrypt** 方法會從秘密衍生工作階段金鑰，並使用該金鑰來加密 [**Content**](encrypteddata-content.md)屬性值。 它會以編碼字串的形式傳回加密的內容。

## <a name="syntax"></a>語法


```VB
EncryptedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*Edi.encodingtype* \[在中，選擇性\]
</dt> <dd>

[**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md)列舉的值，表示用來編碼加密資料的編碼類型。 預設值為 CAPICOM \_ 編碼 \_ BASE64。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                  | 意義                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ 編碼 \_ 任何**</dt> </dl>          | 只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。 如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。 在 CAPICOM 2.0 中引進。<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ 編碼 \_ BASE64**</dt> </dl> | 資料會儲存為 base64 編碼字串。<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ 編碼 \_ 二進位**</dt> </dl> | 資料會儲存為純二進位序列。<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

包含已加密之編碼資料的字串。

## <a name="remarks"></a>備註

在呼叫 **Encrypt** 方法之前，請先設定 [**Content**](encrypteddata-content.md) 屬性，然後呼叫 [**>client.setsecret**](encrypteddata-setsecret.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| 標頭<br/>                | <dl> <dt>Infocard。h</dt> </dl>  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> <dt>

[**A**](encrypteddata.md)
</dt> </dl>

 

 

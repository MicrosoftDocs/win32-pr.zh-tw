---
description: 產生工作階段金鑰，並將資料加密和信封。
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: EnvelopedData 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994040"
---
# <a name="envelopeddataencrypt-method"></a>EnvelopedData 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 [**EnvelopedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**Encrypt** 方法會產生工作階段金鑰、使用該金鑰來加密內容、使用每個收件者的公開金鑰來加密工作階段金鑰，以信封每個收件者的加密內容，然後傳回包含加密內容和加密工作階段金鑰的 [*BLOB*](../secgloss/b-gly.md)做為編碼字串。

## <a name="syntax"></a>語法


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*Edi.encodingtype* \[在中，選擇性\]
</dt> <dd>

[**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md)列舉的值，表示用來編碼封包資料的編碼類型。 預設的編碼值為 CAPICOM \_ 編碼 \_ BASE64。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                  | 意義                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ 編碼 \_ 任何**</dt> </dl>          | 只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。 如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。 在 CAPICOM 2.0 中引進。<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ 編碼 \_ BASE64**</dt> </dl> | 資料會儲存為 base64 編碼字串。<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ 編碼 \_ 二進位**</dt> </dl> | 資料會儲存為純二進位序列。<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 BLOB，其中包含編碼字串中的封包資料。

## <a name="remarks"></a>備註

傳回的 BLOB 包含加密的內容，以及每個預定收件者的加密工作階段金鑰。 這些工作階段金鑰會使用每個收件者的公開金鑰進行加密。 加密的工作階段金鑰只能使用收件者的私密金鑰進行解密。

如果收件者屬性不包含任何資訊 [**，則此**](envelopeddata-recipients.md) 方法會搜尋目前使用者的 AddressBook 憑證存放區中是否有潛在的收件者。 如果找到多個潛在的收件者，則會提示使用者從選取範圍對話方塊中選取收件者。

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

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 

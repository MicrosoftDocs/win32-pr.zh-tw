---
description: 將憑證複製到編碼的字串。
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: ICertificate2：： Export 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aee48fe3d9ba56cba90c9645a3fb9752e3367a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995050"
---
# <a name="icertificate2export-method"></a>ICertificate2：： Export 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1)。\]

**Export** 方法會將憑證複製到編碼的字串。 編碼的字串可以寫入檔案或匯入至新的 [**憑證**](certificate.md) 物件。

## <a name="syntax"></a>語法


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*Edi.encodingtype* \[在中，選擇性\]
</dt> <dd>

[**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md)列舉值，指定匯出作業的編碼類型。 預設值為 **CAPICOM \_ 編碼 \_ BASE64**。 下表顯示可能的值。



| 值                                                                                                                                                                                  | 意義                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ 編碼 \_ 任何**</dt> </dl>          | 只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。 如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。 在 CAPICOM 2.0 中引進。<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ 編碼 \_ BASE64**</dt> </dl> | 資料會儲存為 base64 編碼字串。<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ 編碼 \_ 二進位**</dt> </dl> | 資料會儲存為純二進位序列。<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

字串，其中包含以指定編碼形式匯出的憑證。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[加密物件](cryptography-objects.md)
</dt> <dt>

[**憑證**](certificate.md)
</dt> </dl>

 

 

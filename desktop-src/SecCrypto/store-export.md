---
description: 將開啟的憑證存放區的內容複寫到已編碼的字串。
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Store. Export 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9adf0f42d64e0bc7ced76441ae0fe1da2d2b6609d9d717d5e3b26f8dd07db7b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897800"
---
# <a name="storeexport-method"></a>Store. Export 方法

\[**匯出** 方法可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/previous-versions/windows/embedded/hh424027(v=msdn.10))。\]

**Export** 方法會將開啟的 [*憑證存放區*](../secgloss/c-gly.md)的內容複寫到已編碼的字串。

## <a name="syntax"></a>語法


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*SaveAs* \[在中，選擇性\]
</dt> <dd>

指定匯出作業格式之 [CAPICOM \_ 存放區的儲存 \_ \_ 為 \_ 類型](capicom-store-save-as-type.md) 列舉的值。 預設值為 [ \_ 儲存為序列化的 CAPICOM 存放區] \_ \_ \_ 。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                     | 意義                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <dt>**\_將 CAPICOM 儲存區儲存 \_ 為已 \_ \_ 序列化**</dt> </dl> | 存放區是以序列化格式儲存。<br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <dt>**\_將 CAPICOM 存放區 \_ 另存 \_ 為 \_ PKCS7**</dt> </dl>                | 存放區是以 PKCS \# 7 格式儲存。<br/>   |



 

</dd> <dt>

*Edi.encodingtype* \[在中，選擇性\]
</dt> <dd>

[CAPICOM \_ 編碼 \_ 類型](capicom-encoding-type.md)列舉的值，表示匯出之存放區的編碼類型。 預設值為 CAPICOM \_ 編碼 \_ BASE64。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                  | 意義                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ 編碼 \_ 任何**</dt> </dl>          | 只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。 如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。 在 CAPICOM 2.0 中引進。<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ 編碼 \_ BASE64**</dt> </dl> | 資料會儲存為 base64 編碼字串。<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ 編碼 \_ 二進位**</dt> </dl> | 資料會儲存為純二進位序列。<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回字串，其中包含指定編碼形式之存放區中的憑證。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**儲存**](store.md)
</dt> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 

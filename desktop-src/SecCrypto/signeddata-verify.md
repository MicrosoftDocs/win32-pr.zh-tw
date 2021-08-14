---
description: 判斷 SignedData 物件中已簽署資料的簽章是否有效。
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: SignedData Verify 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ccda81fc3640d4d09f9644bdf0d84a18a68b743397e1578a5ad434349893e893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898972"
---
# <a name="signeddataverify-method"></a>SignedData Verify 方法

\[[ **驗證** ] 方法可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**Verify** 方法會判斷 [**SignedData**](signeddata.md)物件中已簽署 [*資料的簽*](../secgloss/d-gly.md)章是否有效。 若要驗證簽章，內容的加密 [*雜湊*](../secgloss/h-gly.md) 會使用簽署者憑證的簽署者公開金鑰進行解密。 解密的雜湊會與新的資料內容雜湊進行比較。 如果雜湊相符，則簽章有效。 此外，這個方法也會建立憑證鏈，以判斷憑證的有效性，以提供用來解密雜湊的 [*公開金鑰*](../secgloss/p-gly.md) 。

## <a name="syntax"></a>語法


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*SignedMessage* \[在\]
</dt> <dd>

包含要驗證之已簽署訊息的字串。

</dd> <dt>

*bDetached* \[在中，選擇性\]
</dt> <dd>

若為 **True**，則會卸離要簽署的資料;也就是說，簽署的內容不會包含在簽署的物件中。 若要確認卸離內容上的簽章，應用程式必須有原始內容的複本。 如果已簽署訊息的收件者具有已簽署資料的原始複本，則通常會使用卸離的內容來減少在 web 上傳送的已簽署物件大小。 預設值為 **[False]** 。

</dd> <dt>

*VerifyFlag* \[在中，選擇性\]
</dt> <dd>

表示驗證原則的 [CAPICOM \_ 帶正負號 \_ 資料 \_ 驗證 \_ 旗](capicom-signed-data-verify-flag.md) 標列舉值。 預設值是 [CAPICOM \_ 驗證簽章 \_ \_ 和 \_ 憑證]。 使用此值，就會檢查憑證的有效性和簽章的有效性。 此參數可設定為驗證簽章，而非憑證。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                                             | 意義                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <dt>**\_ \_ 僅限 CAPICOM 驗證簽章 \_**</dt> </dl>                                   | 只會檢查簽章。<br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <dt>**CAPICOM \_ 驗證簽章 \_ \_ 和 \_ 憑證**</dt> </dl> | 檢查簽章和用來建立簽章之憑證的有效性。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回字串，其中包含已編碼、已簽署的資料。

如果此方法失敗，則會擲回錯誤。 **Err** 物件將包含有關錯誤的其他資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 

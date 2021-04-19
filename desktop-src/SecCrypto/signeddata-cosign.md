---
description: 在先前簽署的內容上建立數位簽章。
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: SignedData. CoSign 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ab2a24a20fd65fad9622b775bedc59cfa28301a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984860"
---
# <a name="signeddatacosign-method"></a>SignedData. CoSign 方法

\[**CoSign** 方法可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**CoSign** 方法會在先前簽署的內容上建立 [*數位簽章*](../secgloss/d-gly.md)。

## <a name="syntax"></a>語法


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*簽署者* \[在中，選擇性\]
</dt> <dd>

資料簽署者之 [**簽署者**](signer.md) 物件的參考。 **簽署者** 物件必須能夠存取用來簽署的憑證私密金鑰。 這個參數可以是 **Null**;如需詳細資訊，請參閱備註。

</dd> <dt>

*Edi.encodingtype* \[在中，選擇性\]
</dt> <dd>

[**CAPICOM \_ 編碼 \_ 類型**](capicom-encoding-type.md)列舉的值，指出簽署的資料如何進行編碼。 預設值為 CAPICOM \_ 編碼 \_ BASE64。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                  | 意義                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ 編碼 \_ 任何**</dt> </dl>          | 只有當輸入資料有未知的編碼類型時，才會使用此編碼類型。 如果這個值是用來指定輸出的編碼類型，則會 \_ 改用 CAPICOM 編碼 \_ BASE64。 在 CAPICOM 2.0 中引進。<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ 編碼 \_ BASE64**</dt> </dl> | 資料會儲存為 base64 編碼字串。<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ 編碼 \_ 二進位**</dt> </dl> | 資料會儲存為純二進位序列。<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回字串，其中包含已編碼、已簽署的資料。

如果此方法失敗，則會擲回錯誤。 **Err** 物件將包含有關錯誤的其他資訊。

## <a name="remarks"></a>備註

> [!IMPORTANT]
> 從 web 腳本呼叫這個方法時，腳本必須使用您的 [*私密金鑰*](../secgloss/p-gly.md) 來建立數位簽章。 允許不受信任的網站使用您的私密金鑰會有安全性風險。 當第一次呼叫此方法時，會詢問網站是否可以使用您的私密金鑰的對話方塊。 如果您允許腳本使用您的私密金鑰來建立數位簽章，然後選取 [不要再顯示此對話方塊]，則該網域內使用您的私密金鑰來建立數位簽章的任何腳本將不會再出現此對話方塊。 不過，嘗試使用您的私密金鑰來建立數位簽章的網域以外的腳本仍會出現此對話方塊。 如果您不允許腳本使用您的私密金鑰，然後選取 [不要再顯示此對話方塊]，則該網域內的腳本將會自動拒絕使用您私密金鑰來建立數位簽章的能力。

 

非人保證會以任何特定順序來進行。

下列結果適用于 *簽署者* 參數值：

-   如果 *簽署者* 參數不是 **Null**，這個方法會使用相關聯憑證所指向的私密金鑰來加密 cosignature。 如果憑證所指向的私密金鑰無法使用，方法將會失敗。
-   如果 *簽署者* 參數為 **Null** ，而且目前的使用者儲存區中只有一個可存取私密金鑰的憑證，則會 \_ 使用該憑證來建立 cosignature。
-   如果 *簽署者* 參數為 **Null**， [**EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) 屬性值為 true，而且目前使用者的存放區中有一個以上的憑證 \_ 具有可用的私密金鑰，則會出現一個對話方塊，讓使用者選取要使用的憑證。
-   如果 *簽署者* 參數為 **Null** ，而且 [**EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) 屬性為 false，則方法會失敗。
-   如果 *簽署者* 參數為 **Null** ，而且目前 \_ 使用者的存放區中沒有具有可用私密金鑰的憑證，則該方法會失敗。

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

 

 

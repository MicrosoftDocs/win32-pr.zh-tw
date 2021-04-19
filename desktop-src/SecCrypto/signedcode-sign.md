---
description: 建立 Authenticode 數位簽章，並簽署 SignedCode 中指定的可執行檔。
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: SignedCode. Sign 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996232"
---
# <a name="signedcodesign-method"></a>SignedCode. Sign 方法

\[**Sign** 方法可用於 [需求] 區段中指定的作業系統。 相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**Sign** 方法會建立 Authenticode 數位簽章，並簽署 [**SignedCode**](signedcode-filename.md)中指定的可執行檔。

## <a name="syntax"></a>語法


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*簽署者* \[在中，選擇性\]
</dt> <dd>

[**簽署者**](signer.md)物件，該物件可存取用來簽署程式碼的憑證私密金鑰。 預設值為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在呼叫 **Sign** 方法之前，必須在 [**FileName**](signedcode-filename.md) 屬性中指定包含程式碼的檔案。

如果可執行檔已經簽署，這個方法會覆寫現有的簽章。

下列結果適用于 *簽署者* 參數值：

-   如果 *簽署者* 參數不是 **Null**，這個方法會使用相關聯憑證所指向的私密金鑰來加密簽章。 如果憑證所指向的私密金鑰無法使用，方法將會失敗。
-   如果 *簽署者* 參數為 **Null** ，而且目前使用者的存放區中只有一個憑證可 \_ 存取具有程式碼簽署功能的私密金鑰，則會使用該憑證來建立簽章。
-   如果 *簽署者* 參數為 **Null**， [**EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) 屬性值為 true，而且目前使用者的存放區中有一個以上的憑證具有 \_ 程式碼簽署功能的可用私密金鑰，則會出現一個對話方塊，讓使用者選取所要使用的憑證。
-   如果 *簽署者* 參數為 **Null** ，而且 [**EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) 屬性為 false，則方法會失敗。
-   如果 *簽署者* 參數為 **Null** ，而且目前使用者的存放區中沒有具有 \_ 程式碼簽署功能之可用私密金鑰的憑證，則該方法會失敗。

這個方法會使用 SHA-1 雜湊演算法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

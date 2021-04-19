---
description: 確認簽署程式碼上的 Authenticode 簽章。
ms.assetid: eecd692d-6b20-4644-a3d9-fba07ee667d7
title: SignedCode Verify 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ad9ad2cdbf9c8b7970f50446bba0da7a3afdcd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994874"
---
# <a name="signedcodeverify-method"></a>SignedCode Verify 方法

\[[ **驗證** ] 方法可用於 [需求] 區段中指定的作業系統。 相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**Verify** 方法會驗證已簽署程式碼上的 Authenticode 簽章。

## <a name="syntax"></a>語法


```VB
SignedCode.Verify( _
  [ ByVal bUIAllowed ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bUIAllowed* \[在中，選擇性\]
</dt> <dd>

指定是否使用對話方塊來驗證簽章的布林值。 若為 true，則會產生對話方塊，以判斷程式碼是否受信任。 預設值為 false。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 

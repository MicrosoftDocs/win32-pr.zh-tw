---
description: 在 SignedCode 中指定的已簽署可執行檔上建立 Authenticode 時間戳記簽章。
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: SignedCode Timestamp 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987116"
---
# <a name="signedcodetimestamp-method"></a>SignedCode Timestamp 方法

\[Timestamp 方法可用於 [需求 **]** 區段中指定的作業系統。 相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**Timestamp** 方法會在 **SignedCode** 中指定的已簽署可執行檔上建立 Authenticode 時間戳記簽章。 這個時間戳記是由時間戳記授權單位所執行之已簽署可執行檔的計數器簽章。

## <a name="syntax"></a>語法


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*URL* \[在\]
</dt> <dd>

字串，包含時間戳記伺服器的 URL。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

時間戳記會藉由確認可執行檔是否在時間戳記時簽署，來擴充憑證的有效性。

在呼叫這個方法之前，必須在 **SignedCode** 中指定要加上時間戳記的已簽署可執行檔，而且必須呼叫 [**SignedCode**](signedcode-sign.md) 方法來簽署可執行檔。

如果已簽署的可執行檔已加上時間戳記，這個方法會覆寫現有的時間戳記。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 

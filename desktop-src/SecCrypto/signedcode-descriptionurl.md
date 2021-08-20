---
description: 設定或抓取已簽署的可執行檔之描述的 URL。
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: SignedCode. DescriptionURL 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2668be4a9b0d4c6d746d0849c884c9819ad0d9291049e806e73fc1cea1b49d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974205"
---
# <a name="signedcodedescriptionurl-property"></a>SignedCode. DescriptionURL 屬性

\[**DescriptionURL** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**DescriptionURL** 屬性會設定或抓取已簽署的可執行檔之描述的 URL。

## <a name="syntax"></a>Syntax


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a>屬性值

已簽署可執行檔之描述的 URL。

## <a name="remarks"></a>備註

**DescriptionURL** 是出現在 [Authenticode 驗證] 對話方塊連結中之 [**描述**](signedcode-description.md)的 URL。 如果此屬性為 **Null**，則 **描述** 不會作為連結運作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 

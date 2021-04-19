---
description: 抓取已簽署的可執行檔中的憑證集合。
ms.assetid: ecc05117-8b98-4e49-9671-71829df24597
title: SignedCode 憑證屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b24a07041dae1ea2387ced93d1d2ae541a806029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992586"
---
# <a name="signedcodecertificates-property"></a>SignedCode 憑證屬性

\[[ **憑證** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

[ **憑證** ] 屬性會在已簽署的可執行檔中，抓取憑證的集合。

## <a name="syntax"></a>Syntax


```VB
SignedCode.Certificates As Certificates
```



## <a name="property-value"></a>屬性值

[**憑證**](certificates.md)集合，其中包含已簽署可執行檔中的所有憑證。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 

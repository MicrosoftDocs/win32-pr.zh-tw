---
description: 設定或抓取已簽署之可執行檔的描述。
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: SignedCode。 Description 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6046beae61aebaf33ea5eedb6ef2ec643f2edb39dbbedc61372085be2220068b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900348"
---
# <a name="signedcodedescription-property"></a>SignedCode。 Description 屬性

\[[ **描述** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**Description** 屬性會設定或抓取已簽署之可執行檔的描述。

## <a name="syntax"></a>Syntax


```VB
SignedCode.Description As String
```



## <a name="property-value"></a>屬性值

已簽署之可執行檔的描述。

## <a name="remarks"></a>備註

描述是出現在 [Authenticode 驗證] 對話方塊中的文字。 文字應該會描述已簽署的可執行檔。 如果此屬性為 **Null**，對話方塊會顯示可執行檔的名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 

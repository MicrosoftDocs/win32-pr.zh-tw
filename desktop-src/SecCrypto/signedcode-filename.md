---
description: FileName 屬性會設定或抓取可執行檔的路徑。 這是預設屬性。
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: SignedCode FileName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e6e31e57376f987b2b5cb47e5e6bd8a0d5e85fba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995099"
---
# <a name="signedcodefilename-property"></a>SignedCode FileName 屬性

\[[ **檔案名** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用平台叫用服務 (PInvoke) 呼叫 WIN32 API [**SignerSignEx**](signersignex.md)、 [**SignerTimeStampEx**](signertimestampex.md)和 [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) 函式，以使用 Authenticode 數位簽章簽署內容。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**FileName** 屬性會設定或抓取可執行檔的路徑。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a>屬性值

可執行檔路徑。

## <a name="remarks"></a>備註

如果已修改 **FileName** 屬性的值，則會重設整個 [**SignedCode**](signedcode.md) 物件的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 

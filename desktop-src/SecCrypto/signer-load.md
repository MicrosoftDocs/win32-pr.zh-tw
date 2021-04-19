---
description: 從指定的 .pfx 檔案載入簽署憑證。
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: 簽署者. Load 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990069"
---
# <a name="signerload-method"></a>簽署者. Load 方法

\[**Load** 方法可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**CmsSigner 類別**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**Load** 方法會從指定的 .pfx 檔案載入簽署憑證。

## <a name="syntax"></a>語法


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*FileName* 
</dt> <dd>

包含簽署憑證的 .pfx 檔案名。

</dd> <dt>

*密碼* \[選\]
</dt> <dd>

字串，包含用來開啟檔案的純文字密碼。 密碼最多可使用32個 Unicode 字元，包括結束的 null 字元。 預設值為空字串 ("")。 如需保護密碼的相關資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會載入 .pfx 檔案中有相關私密金鑰的第一個憑證。

\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**簽署者**](signer.md)
</dt> </dl>

 

 

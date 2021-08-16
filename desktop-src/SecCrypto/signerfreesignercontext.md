---
description: 釋放先前呼叫 SignerSignEx 函式所配置的簽署者 \_ 內容結構。
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: SignerFreeSignerCoNtext 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8338e346db49b21f9eccfca11a7e1a1fff0c42f0a013139a097385fbbe90c76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973189"
---
# <a name="signerfreesignercontext-function"></a>SignerFreeSignerCoNtext 函式

**SignerFreeSignerCoNtext** 函式會釋放先前呼叫 [**SignerSignEx**](signersignex.md)函數所配置的 [**簽署者 \_ 內容**](signer-context.md)結構。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。

 

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSignerCoNtext* \[在\]
</dt> <dd>

要釋放之 [**簽署者 \_ 內容**](signer-context.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回 S \_ OK。

如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**簽署者 \_ 內容**](signer-context.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 

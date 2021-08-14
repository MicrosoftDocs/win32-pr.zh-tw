---
description: 抓取憑證範本的數目。
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: ISCrdEnr：： getCertTemplateCount 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cbbccf895d06106990007584e0eb1946d74b2c092a4c27c8b7a9e279b93f7e36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409668"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a>ISCrdEnr：： getCertTemplateCount 方法

**GetCertTemplateCount** 方法會抓取憑證範本的數目。

## <a name="syntax"></a>語法


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

判斷範本是否適用于使用者或電腦憑證的值。 如果此值為捨棄 \_ 註冊 \_ 使用者 \_ \_ 憑證範本 (定義為 1) 則傳回的計數將會是使用者憑證範本。 如果此值為捨棄 \_ 註冊 \_ 電腦 \_ 證書 \_ 範本 (定義為 2) 則傳回的計數將會是電腦憑證範本。

</dd> <dt>

*pdwCertTemplateCount* \[擴展\]
</dt> <dd>

傳回憑證範本數目的 **LONG** 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="c"></a>C++

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

### <a name="vb"></a>VB

代表憑證範本數目的 **Long** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 





---
description: 用來判斷憑證範本是否包含 szOID PKIX 的 \_ \_ \_ 電子郵件 \_ 保護金鑰使用方式。
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: ISCrdEnr：： getCertTemplateSMIME 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8da8c9c3202c0955a001a63e77f85858fc6237d7476c0fc5222ae8f85e94a7c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515958"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a>ISCrdEnr：： getCertTemplateSMIME 方法

**GetCertTemplateSMIME** 方法是用來判斷憑證範本是否包含 szOID PKIX 的的 \_ \_ \_ 電子郵件 \_ 保護金鑰使用方式。

如果此金鑰使用方式是憑證範本的一部分，憑證範本支援 [*安全/多用途網際網路郵件延伸*](../secgloss/s-gly.md) (S/MIME) 作業。

## <a name="syntax"></a>語法


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrCertTemplateName* \[在\]
</dt> <dd>

要查詢 S/MIME 金鑰使用方式的憑證名稱。

</dd> <dt>

*pdwCertTemplateSMIME* \[擴展\]
</dt> <dd>

**DWORD** 的指標，如果 *bstrCertTemplateName* 支援 S/MIME，則會傳回一個值。否則會傳回零。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="c"></a>C++

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

### <a name="vb"></a>VB

如果 *bstrCertTemplateName* 支援 S/MIME，則會有 **Long** 值。否則為零。

## <a name="remarks"></a>備註

SzOID \_ PKIX \_ KP \_ 電子郵件保護的常數 \_ 定義于 Wincrypt 中。

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

[**ISCrdEnr：：報名**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 

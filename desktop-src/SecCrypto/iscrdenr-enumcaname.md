---
description: 針對指定的憑證範本名稱，列舉 (Ca) 的憑證授權單位單位名稱。
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: ISCrdEnr：： enumCAName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 11742525d616aecc8d83871ae2a59025d1034513ae99d8a7253d16d9e0f64dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005216"
---
# <a name="iscrdenrenumcaname-method"></a>ISCrdEnr：： enumCAName 方法

**EnumCAName** 方法會為指定的憑證範本名稱，列舉 (ca) 的 [*憑證授權單位*](../secgloss/c-gly.md)單位名稱。

## <a name="syntax"></a>語法


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*dwIndex* \[在\]
</dt> <dd>

列舉序列的以零為基底的索引。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

值，這個值會判斷名稱是指 CA 名稱或 CA 的電腦名稱稱。 如果此值為捨棄 \_ 註冊 \_ CA \_ 電腦 \_ 名稱 (定義為 0x01) ，則名稱會參考 CA 的電腦名稱稱。 否則，名稱會參考 CA 名稱。

</dd> <dt>

*bstrCertTemplateName* \[在\]
</dt> <dd>

憑證範本的名稱。

</dd> <dt>

*pbstrCAName* \[擴展\]
</dt> <dd>

傳回 CA 名稱之字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="c"></a>C++

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

### <a name="vb"></a>VB

表示 CA 名稱的字串。

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

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 

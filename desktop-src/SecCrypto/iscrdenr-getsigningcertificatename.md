---
description: 從簽署憑證抓取主體名稱。
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: ISCrdEnr：： getSigningCertificateName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 29933856eb644e638e9e58c8da0b0e3d6234e4f0175925c8a1fb5b48b126e3ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622398"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a>ISCrdEnr：： getSigningCertificateName 方法

**GetSigningCertificateName** 方法會從簽署憑證抓取主體名稱。

這個方法也可以用來在對話方塊中顯示憑證。 這個方法會呼叫 [*CryptoAPI*](../secgloss/c-gly.md) 函數 [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)。

## <a name="syntax"></a>語法


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

值，決定憑證是否顯示在對話方塊中。 如果此值為捨棄 \_ ，則不會將 \_ 任何 \_ 顯示 \_ 憑證 (定義為 0x01) ，也不會顯示簽署憑證; 任何其他值都會導致簽署憑證顯示在 [ **憑證** ] 對話方塊中。

</dd> <dt>

*pbstrSigningCertName* \[擴展\]
</dt> <dd>

傳回簽署憑證名稱之字串的指標。 簽署憑證將用來簽署 [*憑證要求*](../secgloss/c-gly.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="c"></a>C++

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

### <a name="vb"></a>VB

字串，表示簽署憑證的名稱。 簽署憑證將用來簽署 [*憑證要求*](../secgloss/c-gly.md)。

## <a name="remarks"></a>備註

**GetSigningCertificateName** 方法會傳回您 (之憑證的主體名稱，或是在先前成功呼叫 [**ISCrdEnr：： selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)或 [**ISCrdEnr：： setSigningCertificate**](iscrdenr-setsigningcertificate.md)時選取的另一個系統管理員) 。 這個方法會呼叫 [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) 函式，根據 \_ \_ \_ \_ **CertGetNameString** 的 *dwType* 參數的 CERT name SIMPLE DISPLAY TYPE 值所述的順序，來取得主體名稱。

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

[**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 

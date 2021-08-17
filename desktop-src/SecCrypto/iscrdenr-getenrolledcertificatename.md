---
description: 抓取 ISCrdEnr：：註冊的先前成功呼叫所產生的憑證名稱。
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: ISCrdEnr：： getEnrolledCertificateName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 79158a5c10cee2f4f38163c5a657199415568b36076b9e84f2a54020d1be42a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409488"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a>ISCrdEnr：： getEnrolledCertificateName 方法

**GetEnrolledCertificateName** 方法會抓取先前成功呼叫 [**ISCrdEnr：：報名**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))所產生的憑證名稱。

這個方法也可以用來在對話方塊中顯示憑證。 這個方法會呼叫 [*CryptoAPI*](../secgloss/c-gly.md) 函數 [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)。

## <a name="syntax"></a>語法


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

值，決定憑證是否顯示在對話方塊中。 如果此值為捨棄 \_ ，則不會將 \_ 任何 \_ 顯示 \_ 憑證 (定義為 0x01) ，也不會顯示已註冊的憑證; 任何其他值都會導致註冊的憑證顯示在 **憑證** 對話方塊中。

</dd> <dt>

*pBstrCertName* \[擴展\]
</dt> <dd>

傳回已抓取憑證名稱之字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="c"></a>C++

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

### <a name="vb"></a>VB

表示已取出憑證名稱的字串。

## <a name="remarks"></a>備註

因為這個方法是在現有的憑證上操作，所以您必須先成功呼叫 [**ISCrdEnr：：報名**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) ，才能呼叫 **getEnrolledCertificateName**。

**GetEnrolledCertificateName** 方法會呼叫 [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)函式，根據 \_ \_ \_ \_ **CertGetNameString** 的 *dwType* 參數的 CERT name SIMPLE DISPLAY TYPE 值所述的順序，來取得憑證名稱。

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

 

 

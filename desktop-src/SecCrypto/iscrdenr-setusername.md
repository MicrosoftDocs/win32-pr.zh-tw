---
description: 指定要在其上註冊憑證的使用者名稱。
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: ISCrdEnr：： setUserName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: f60b69107063bc114a186338b084cfa07dd96085995f76e5cdd82b415d23c905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409168"
---
# <a name="iscrdenrsetusername-method"></a>ISCrdEnr：： setUserName 方法

**SetUserName** 方法會指定要在其上註冊憑證的使用者名稱。

## <a name="syntax"></a>語法


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

此值必須是捨棄 \_ 註冊 \_ UPN \_ 名稱 (定義為 1) 或捨棄 \_ 註冊 \_ SAM \_ 相容 \_ 名稱 (定義為 2) 。

\_ \_ \_ 如果在 *bstrUserName* 中指定的名稱是使用者的通用主體名稱（例如 ""），請將此值設定為捨棄註冊 UPN 名稱 someone@example.com 。 使用者的 UPN 名稱必須對應到現有的安全性存取管理員 (SAM) 名稱。

\_ \_ \_ \_ 如果在 *bstrUserName* 中指定的名稱是使用者的 SAM 名稱（格式為 "DOMAIN user"），請 \\ 將此值設定為捨棄註冊 SAM 相容名稱。

</dd> <dt>

*bstrUserName* \[在\]
</dt> <dd>

使用者名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="vb"></a>VB

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

## <a name="remarks"></a>備註

呼叫這個方法來指定要發出 [*智慧卡*](../secgloss/s-gly.md)的使用者名稱。 **SetUserName** 的替代方案是 [**ISCrdEnr：： selectUserName**](iscrdenr-selectusername.md)。

指定使用者名稱之後，您可以藉由呼叫 [**getUserName**](iscrdenr-getusername.md)來取出其值。

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

[**ISCrdEnr：： getUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> </dl>

 

 

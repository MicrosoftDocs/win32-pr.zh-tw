---
description: 抓取要作為憑證註冊目標之使用者的名稱。
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: ISCrdEnr：： getUserName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320379"
---
# <a name="iscrdenrgetusername-method"></a>ISCrdEnr：： getUserName 方法

**GetUserName** 方法會抓取代表憑證註冊之使用者的名稱。

在呼叫這個方法之前，您必須在 [**ISCrdEnr：： selectUserName**](iscrdenr-selectusername.md) 或 [**ISCrdEnr：： setUserName**](iscrdenr-setusername.md)的呼叫中指定使用者名稱。

## <a name="syntax"></a>語法


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

此值必須是零 (0) 、捨棄 \_ 註冊 \_ UPN \_ 名稱或捨棄 \_ 註冊 \_ SAM \_ 相容 \_ 名稱。

如果此值為捨棄 \_ 註冊 \_ UPN \_ 名稱， **getUserName** 會傳回使用者的通用主體名稱 (UPN) ，例如 " someone@example.com "。

如果這個值是捨棄 \_ 註冊 \_ SAM \_ 相容 \_ 名稱，方法會以 "DOMAIN user" 格式傳回使用者的安全性存取管理員 (SAM) 名稱 \\ 。

如果此值為零，則方法會傳回使用者的 UPN 名稱（如果有的話）。 如果使用者沒有 UPN 名稱，方法會傳回使用者的 SAM 名稱。

</dd> <dt>

*pbstrUserName* \[擴展\]
</dt> <dd>

傳回使用者名稱之字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="c"></a>C++

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

### <a name="vb"></a>VB

表示使用者名稱的字串。

## <a name="remarks"></a>備註

您可以藉由呼叫 [**ISCrdEnr：： setUserName**](iscrdenr-setusername.md)或 [**ISCrdEnr：： selectUserName**](iscrdenr-selectusername.md)，指定 [*智慧卡*](../secgloss/s-gly.md)發出的使用者名稱。 指定使用者名稱之後，您可以藉由呼叫 **getUserName** 來取出其值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 

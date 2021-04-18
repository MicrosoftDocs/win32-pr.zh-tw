---
description: 顯示選取的使用者介面，允許選取使用者名稱。
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: ISCrdEnr：： selectUserName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971549"
---
# <a name="iscrdenrselectusername-method"></a>ISCrdEnr：： selectUserName 方法

**SelectUserName** 方法會顯示 **選取的使用者** 介面，允許選取使用者名稱。

使用者名稱會套用至代表憑證註冊的使用者。

## <a name="syntax"></a>語法


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

保留供未來使用。 將此值設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="vb"></a>VB

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

## <a name="remarks"></a>備註

使用這個方法來選取使用者的名稱。 選取使用者名稱之後，您可以藉由呼叫 [**ISCrdEnr：： getUserName**](iscrdenr-getusername.md) 方法來取出其值。

使用「選取使用者」介面的另一種方式，是藉由呼叫 [**ISCrdEnr：： setUserName**](iscrdenr-setusername.md) 方法來指定使用者。

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

[**ISCrdEnr：： getUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 





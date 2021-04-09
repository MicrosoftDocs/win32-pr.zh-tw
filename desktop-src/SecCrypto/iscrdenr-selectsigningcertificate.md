---
description: 顯示 [選取憑證] 對話方塊，允許簽署憑證 (也稱為註冊代理程式憑證) 選取。
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: ISCrdEnr：： selectSigningCertificate 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852091"
---
# <a name="iscrdenrselectsigningcertificate-method"></a>ISCrdEnr：： selectSigningCertificate 方法

**SelectSigningCertificate** 方法會顯示 [**選取憑證**] 對話方塊，允許簽署憑證 (也稱為 [*註冊代理程式憑證*]) 選取。

代表使用者註冊之前，您必須先選取簽署憑證。 與此簽署憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md) 會用來簽署 PKCS \# 7 要求。 PKCS \# 7 接著會包含使用者的 pkcs \# 10 要求 (使用) 的使用者私密金鑰進行簽署。

## <a name="syntax"></a>語法


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

保留供未來使用。 將此值設定為零。

</dd> <dt>

*bstrCertTemplateName* \[在\]
</dt> <dd>

字串，表示簽署憑證的憑證範本名稱。 如果您已取得 EnrollmentAgent 憑證，您可以使用 "EnrollmentAgent" 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="vb"></a>VB

如果方法成功，則方法會傳回 **S \_ OK**。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

## <a name="remarks"></a>備註

代表使用者註冊之前，您必須先取得簽署憑證。 您可以使用 [憑證管理員] MMC 嵌入式管理單元來取得簽署憑證。 **SelectSigningCertificate** 方法不會取得簽署憑證，但會顯示先前取得之簽署憑證的對話方塊，可讓您選擇要使用哪一個憑證來簽署代表註冊的要求。

**SelectSigningCertificate** 的替代方案是 [**ISCrdEnr：： setSigningCertificate**](iscrdenr-setsigningcertificate.md)。

選取簽署憑證之後，就可以藉由呼叫 [**ISCrdEnr：： getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)來取出其名稱。

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

[**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 

---
description: 指定簽署憑證 (也稱為註冊代理程式憑證) 。
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: ISCrdEnr：： setSigningCertificate 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997262"
---
# <a name="iscrdenrsetsigningcertificate-method"></a>ISCrdEnr：： setSigningCertificate 方法

**SetSigningCertificate** 方法會指定簽署憑證 (也稱為 *註冊代理程式憑證*) 。

代表使用者註冊之前，您必須選取或設定簽署憑證。 與此簽署憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md) 會用來簽署 PKCS \# 7 要求。 PKCS \# 7 接著會包含使用者的 pkcs \# 10 要求 (使用) 的使用者私密金鑰進行簽署。

## <a name="syntax"></a>語法


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
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

簽署憑證的憑證範本名稱。 如果您已取得 EnrollmentAgent 憑證，您可以使用 "EnrollmentAgent" 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="vb"></a>VB

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

## <a name="remarks"></a>備註

代表使用者註冊之前，您必須先取得簽署憑證。 您可以使用 [憑證管理員] MMC 嵌入式管理單元來取得簽署憑證。 **SetSigningCertificate** 方法不會取得簽署憑證，但會通知先前取得要使用之簽署憑證的智慧卡註冊控制項。 **SetSigningCertificate** 方法會在呼叫端的 "My" 存放區中搜尋與 *bstrCertTemplateName* 所指定憑證範本對應的最新簽署憑證。

**SetSigningCertificate** 的替代方案是 **ISCrdEnr：： setSigningCertificate**。

設定簽署憑證之後，您可以藉由呼叫 [**ISCrdEnr：： getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)來取出其名稱。

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

 

 

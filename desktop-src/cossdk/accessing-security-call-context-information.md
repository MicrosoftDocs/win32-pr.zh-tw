---
description: 使用以角色為基礎的安全性時，安全性呼叫內容物件可以用來存取目前呼叫的安全性資訊。
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: 存取安全性呼叫內容資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190966"
---
# <a name="accessing-security-call-context-information"></a>存取安全性呼叫內容資訊

使用以角色為基礎的安全性時，安全性呼叫內容物件可以用來存取目前呼叫的安全性資訊。

下列屬性集合可從安全性呼叫內容物件取得：

-   [SecurityCallCoNtext 集合](#securitycallcontext-collection)
-   [SecurityCallers 集合](#securitycallers-collection)
-   [SecurityIdentity 集合](#securityidentity-collection)
-   [相關主題](#related-topics)

## <a name="securitycallcontext-collection"></a>SecurityCallCoNtext 集合



| 屬性                          | 描述                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| NumCallers<br/>             | 呼叫鏈中的呼叫端數目。<br/>                                                                                |
| MinAuthenticationLevel<br/> | 鏈中所有呼叫端最不安全的驗證層級。<br/>                                                          |
| 來電<br/>                | 上游呼叫端身分識別的相關資訊，以 [**SecurityCallers**](securitycallers.md) 集合的形式呈現。<br/> |
| DirectCaller<br/>           | 呼叫物件的呼叫端會直接 (，) 不會有中間的呼叫端。 <br/>                                                  |
| OriginalCaller<br/>         | 發出呼叫之物件的呼叫端。 <br/>                                                               |



 

如需有關如何使用此集合的詳細資訊，Microsoft Visual Basic 開發人員應該會看到 [**SecurityCallCoNtext**](securitycallcontext.md) 類別。 C 和 c + + 開發人員應該參考 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)。

## <a name="securitycallers-collection"></a>SecurityCallers 集合

[**SecurityCallers**](securitycallers.md)集合表示可以使用介於0和1（含）之間的索引來取出的呼叫端。 每個呼叫端都會以 [**SecurityIdentity**](securityidentity.md) 物件表示。

如需此集合的詳細資訊，Visual Basic 開發人員應該會看到 [**SecurityCallers**](securitycallers.md) 類別。 C 和 c + + 開發人員應該參考 [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)。

## <a name="securityidentity-collection"></a>SecurityIdentity 集合



| 屬性                         | 描述                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID<br/>                   | 呼叫端的安全識別碼。<br/>                                                                                                                   |
| AccountName<br/>           | 呼叫端的帳戶名稱。<br/>                                                                                                                           |
| AuthenticationService<br/> | 使用的驗證服務，例如 NTLMSSP、Kerberos 或 SSL。<br/>                                                                                       |
| AuthenticationLevel<br/>   | 使用的驗證層級，代表與物件通訊時使用的保護量。<br/>                                         |
| ImpersonationLevel<br/>    | 用戶端設定的模擬層級（如果使用了模擬）。 此層級表示用戶端提供給伺服器的授權數量。 <br/> |



 

如需此集合的詳細資訊，Visual Basic 開發人員應該會看到 [**SecurityIdentity**](securityidentity.md) 類別。 C 和 c + + 開發人員應該參考 [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檢查角色成員資格](checking-role-membership.md)
</dt> <dt>

[判斷是否已啟用 Role-Based 安全性](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> </dl>

 

 





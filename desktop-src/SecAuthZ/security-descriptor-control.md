---
description: 一組位旗標，可限定安全描述項或其元件的意義。
ms.assetid: 9a4ef57e-c374-4ef6-99dc-1a8dd250f2c2
title: 'SECURITY_DESCRIPTOR_CONTROL (Winnt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3def788407093d0a487640d1ad0e445b61fe20e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971446"
---
# <a name="security_descriptor_control"></a>安全 \_ 描述項 \_ 控制項

**安全 \_ 描述項 \_ 控制項** 資料類型是一組位旗標，可限定 [*安全描述項*](/windows/desktop/SecGloss/s-gly)或其元件的意義。 每個安全描述項都有一個可儲存 **安全 \_ 描述項 \_ 控制** 位的 **控制項** 成員。


```C++
typedef WORD SECURITY_DESCRIPTOR_CONTROL, *PSECURITY_DESCRIPTOR_CONTROL;
```



## <a name="remarks"></a>備註

若要取得安全描述項的控制位，請呼叫 [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) 函數。 若要設定安全描述項的控制位，請使用函數來修改安全描述項。 如需這些函式的清單，請參閱另請參閱一節。

應用程式可以使用 [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) 函式來設定與 ace 自動繼承相關的控制項位。

[**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol)函數所抓取的控制項值可以包含下列 **安全 \_ 描述項 \_ 控制項** 位旗標的組合。



| 值                                                     | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SE \_ DACL \_ 自動 \_ 繼承 \_ 需求<br/> 0x0100<br/> | 表示必要的 [*安全描述項*](/windows/desktop/SecGloss/s-gly) [*，其中 (DACL*](/windows/desktop/SecGloss/d-gly)) 設定為支援將可繼承的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ace) 自動傳播至現有的子物件。<br/> 對於支援自動繼承 (Acl) 的 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) ，一律會設定此位。 受保護的伺服器可以呼叫 [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) 函式來轉換安全描述項，並設定此旗標。 <br/> |
| SE \_ DACL \_ 自動 \_ 繼承<br/> 0x0400<br/>    | 指出 () DACL 的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 所設定的安全描述項，以支援將可繼承的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ace) 至現有子物件的自動傳播。<br/> 對於支援自動繼承 (Acl) 的 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) ，一律會設定此位。 受保護的伺服器可以呼叫 [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) 函式來轉換安全描述項，並設定此旗標。 <br/>                                                                                                  |
| SE \_ DACL \_ 預設<br/> 0x0008<br/>          | 表示具有預設 DACL 的安全描述項。 例如，如果建立者物件未指定 DACL，則物件會從建立者的 [*存取權杖*](/windows/desktop/SecGloss/a-gly) 接收預設的 dacl。 此旗標可能會影響系統將 DACL 視為 ACE 繼承的方式。 如果 \_ 未設定 SE DACL 出現旗標，系統會忽略此旗標 \_ 。<br/> 此旗標是用來判斷物件上的最後一個 DACL 如何進行計算，而且不會實際儲存在安全物件的安全描述項控制項中。<br/> 若要設定這個旗標，請使用 [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) 函數。<br/>                                                                                                                                                                      |
| \_有 SE DACL \_<br/> 0x0004<br/>            | 表示具有 DACL 的安全描述項。 如果未設定此旗標，或已設定此旗標，而且 DACL 為 **Null**，則安全描述項可允許所有人的完整存取權。<br/> 此旗標是用來保存呼叫端指定的安全性資訊，直到安全描述項與安全物件相關聯為止。 當安全描述項與安全物件相關聯之後， \_ \_ 會一律在安全描述項控制項中設定「SE DACL」旗標。<br/> 若要設定這個旗標，請使用 [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) 函數。<br/>                                                                                                                                                                                                                                                                                                   |
| 已 \_ 保護 SE DACL \_<br/> 0x1000<br/>          | 防止可繼承的 Ace 修改安全描述項的 DACL。 若要設定這個旗標，請使用 [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) 函數。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SE \_ 群組 \_ 預設<br/> 0x0002<br/>         | 指出安全描述項群組 (SID) 的 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) 是由預設機制提供。 資源管理員可以使用此旗標來識別安全描述項群組是由預設機制設定的物件。 若要設定這個旗標，請使用 [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup) 函數。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SE \_ 擁有者 \_ 預設<br/> 0x0001<br/>         | 指出安全描述項的擁有者 SID 是由預設機制提供。 資源管理員可以使用此旗標來識別擁有者是由預設機制設定的物件。 若要設定這個旗標，請使用 [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner) 函數。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SE \_ RM \_ 控制項 \_ 有效<br/> 0x4000<br/>       | 指出資源管理員控制項有效。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| SE \_ SACL \_ 自動 \_ 繼承 \_ 需求<br/> 0x0200<br/> | 表示必要的安全描述項，其中 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (SACL) 已設定為支援將可繼承 ace 自動傳播至現有的子物件。<br/> 系統會在執行物件及其現有子物件的自動繼承演算法時，設定此位。 若要轉換安全描述項並設定這個旗標，受保護的伺服器可以呼叫 [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) 函式。<br/>                                                                                                                                                                                                                                                                                   |
| SE \_ SACL \_ 自動 \_ 繼承<br/> 0x0800<br/>    | 表示安全描述項， [*其中 (SACL*](/windows/desktop/SecGloss/s-gly)) 設定為支援將可繼承 ace 自動傳播至現有的子物件。<br/> 系統會在執行物件及其現有子物件的自動繼承演算法時，設定此位。 若要轉換安全描述項並設定這個旗標，受保護的伺服器可以呼叫 [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) 函式。 <br/>                                                                                                                                                                                                                                                                                           |
| SE \_ SACL \_ 預設<br/> 0x0008<br/>          | 預設的機制，而不是安全描述項的原始 [*提供者*](/windows/desktop/SecGloss/p-gly) （提供 SACL）。 此旗標可能會影響對 ACE 繼承而言，系統處理 SACL 的方式。 如果 \_ 未設定 SE SACL 出現旗標，系統會忽略此旗標 \_ 。 若要設定這個旗標，請使用 [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) 函數。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_出現 SE SACL \_<br/> 0x0010<br/>            | 表示具有 SACL 的安全描述項。 若要設定這個旗標，請使用 [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) 函數。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SE \_ SACL \_ 受保護<br/> 0x2000<br/>          | 防止可繼承的 Ace 修改安全描述項的 SACL。 若要設定這個旗標，請使用 [**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) 函數。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SE \_ 自我 \_ 相關<br/> 0x8000<br/>           | 指出 [*自我相關的安全描述項*](/windows/desktop/SecGloss/s-gly)。 如果未設定此旗標，則安全描述項的格式為絕對格式。 如需詳細資訊，請參閱 [絕對和 Self-Relative 的安全描述項](absolute-and-self-relative-security-descriptors.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Winnt (包括 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[低層級存取控制](low-level-access-control.md)
</dt> <dt>

[基本存取控制結構](authorization-structures.md)
</dt> <dt>

[**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity)
</dt> <dt>

[**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol)
</dt> <dt>

[**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)
</dt> <dt>

[**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)
</dt> <dt>

[**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)
</dt> <dt>

[**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)
</dt> <dt>

[**SetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol)
</dt> <dt>

[**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)
</dt> <dt>

[**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)
</dt> <dt>

[**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)
</dt> <dt>

[**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)
</dt> </dl>

 


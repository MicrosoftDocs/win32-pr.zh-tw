---
description: 識別要設定或查詢的物件相關安全性資訊。
ms.assetid: e3e8b35d-9d18-4611-a898-72ca13e40d33
title: 'SECURITY_INFORMATION (Winnt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eda92db81cc2325dcc2eb084c06aa5ac7ca92475cca92d8221e394af9704c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907198"
---
# <a name="security_information"></a>安全性 \_ 資訊

[ **安全性 \_ 資訊** ] 資料類型會識別要設定或查詢的物件相關安全性資訊。 此安全性資訊包括：

-   物件的擁有者
-   物件的主要群組
-   物件的 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) 
-   [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) (物件的 SACL) 


```C++
typedef DWORD SECURITY_INFORMATION, *PSECURITY_INFORMATION;
```



## <a name="remarks"></a>備註

某些 **安全性 \_ 資訊** 成員僅適用于 [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) 函數。 這些成員不會在其他安全性函數（例如 [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) 或 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)）所傳回的結構中傳回。

安全性資訊的每個專案都是由位旗標所指定。 每個位旗標可以是下列其中一個值。 如需詳細資訊，請參閱 [**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask) 和 [**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask) 函數。



| 需要查詢/設定的值/許可權                                                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 屬性 \_ 安全性 \_ 資訊<br/> 需要查詢的許可權： **讀取 \_ 控制項**<br/> 需要設定的許可權： **寫入 \_ DAC**<br/>                                                                                     | 所參考之物件的資源屬性。 資源屬性會儲存在安全描述項的 SACL 中的系統 \_ 資源 \_ 屬性 \_ ACE 類型。<br/> **Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP：** 無法使用這個位旗標。<br/> <br/>                 |
| 備份 \_ 安全性 \_ 資訊<br/> 需要查詢的許可權： **讀取 \_ 控制** 和 **存取 \_ 系統 \_ 安全性**<br/> 需要設定的許可權： **寫入 \_ DAC** 和 **寫入 \_ 擁有** 者和 **存取 \_ 系統 \_ 安全性**<br/> | 安全描述項的所有部分。 這適用于需要保留整個安全描述項的備份和還原軟體。<br/> **Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP：** 無法使用這個位旗標。<br/> <br/>                                                  |
| DACL \_ 安全性 \_ 資訊<br/> 需要查詢的許可權： **讀取 \_ 控制項**<br/> 需要設定的許可權： **寫入 \_ DAC**<br/>                                                                                          | 正在參考物件的 DACL。<br/>                                                                                                                                                                                                                                                                                                                        |
| 群組 \_ 安全性 \_ 資訊<br/> 需要查詢的許可權： **讀取 \_ 控制項**<br/> 需要設定的許可權：**寫入 \_ 擁有** 者 <br/>                                                                                      | 正在參考物件的主要群組識別碼。<br/>                                                                                                                                                                                                                                                                                                    |
| 標籤 \_ 安全性 \_ 資訊<br/> 需要查詢的許可權： **讀取 \_ 控制項**<br/> 需要設定的許可權：**寫入 \_ 擁有** 者 <br/>                                                                                      | 正在參考強制完整性標籤。<br/> 強制完整性標籤是物件的 SACL 中的 ACE。<br/> **Windows Server 2003 和 Windows XP：** 無法使用這個位旗標。<br/> <br/>                                                                                                                                    |
| 擁有者 \_ 安全性 \_ 資訊<br/> 需要查詢的許可權： **讀取 \_ 控制項**<br/> 需要設定的許可權：**寫入 \_ 擁有** 者 <br/>                                                                                      | 正在參考物件的擁有者識別碼。<br/>                                                                                                                                                                                                                                                                                                            |
| 受保護的 \_ DACL \_ 安全性 \_ 資訊<br/> 需要查詢的許可權：無法使用<br/> 需要設定的許可權： **寫入 \_ DAC**<br/>                                                                                   | DACL 無法 (Ace) 繼承 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 。<br/>                                                                                                                                                                                                                   |
| 受保護的 \_ SACL \_ 安全性 \_ 資訊<br/> 需要查詢的許可權：無法使用<br/> 需要設定的許可權： **存取 \_ 系統 \_ 安全性**<br/>                                                                     | SACL 無法繼承 Ace。<br/>                                                                                                                                                                                                                                                                                                                                      |
| SACL \_ 安全性 \_ 資訊<br/> 需要查詢的許可權： **存取 \_ 系統 \_ 安全性**<br/> 需要設定的許可權： **存取 \_ 系統 \_ 安全性**<br/>                                                                 | 正在參考物件的 SACL。<br/>                                                                                                                                                                                                                                                                                                                        |
| 領域 \_ 安全性 \_ 資訊<br/> 需要查詢的許可權： **讀取 \_ 控制項**<br/> 需要設定的許可權： **存取 \_ 系統 \_ 安全性**<br/>                                                                           | 集中存取原則 (端點適用于所參考物件的) 識別碼。 每個 CAP 識別碼都會儲存在 \_ SD 的 SACL 中的系統範圍原則識別碼 \_ \_ \_ ACE 類型。<br/> **Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP：** 無法使用這個位旗標。<br/> <br/> |
| 未受保護的 \_ DACL \_ 安全性 \_ 資訊<br/> 需要查詢的許可權：無法使用<br/> 需要設定的許可權： **寫入 \_ DAC**<br/>                                                                                 | DACL 繼承自父物件的 Ace。<br/>                                                                                                                                                                                                                                                                                                                     |
| 未受保護的 \_ SACL \_ 安全性 \_ 資訊<br/> 需要查詢的許可權：無法使用<br/> 需要設定的許可權： **存取 \_ 系統 \_ 安全性**<br/>                                                                   | SACL 會從父物件繼承 Ace。<br/>                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Winnt (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[存取控制](access-control.md)
</dt> <dt>

[基本存取控制結構](authorization-structures.md)
</dt> <dt>

[**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
</dt> <dt>

[**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)
</dt> <dt>

[**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa)
</dt> <dt>

[**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity)
</dt> <dt>

[**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo)
</dt> <dt>

[**GetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity)
</dt> <dt>

[**QuerySecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-querysecurityaccessmask)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya)
</dt> <dt>

[**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)
</dt> <dt>

[**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa)
</dt> <dt>

[**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)
</dt> <dt>

[**SetSecurityAccessMask**](/windows/desktop/api/Securitybaseapi/nf-securitybaseapi-setsecurityaccessmask)
</dt> <dt>

[**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)
</dt> <dt>

[**SetUserObjectSecurity**](/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity)
</dt> <dt>

[**TreeResetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treeresetnamedsecurityinfoa)
</dt> <dt>

[**TreeSetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treesetnamedsecurityinfoa)
</dt> </dl>

 


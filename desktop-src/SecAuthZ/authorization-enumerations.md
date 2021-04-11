---
description: 搭配授權應用程式使用的列舉。
ms.assetid: e2f22838-102e-432c-9c82-06a3e0741374
title: 授權列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9363ca8039c326a81ad2e08a9136f5f65363146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193661"
---
# <a name="authorization-enumerations"></a>授權列舉

下列列舉與授權應用程式搭配使用。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                          | 描述                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**存取 \_ 模式**](/windows/win32/api/accctrl/ne-accctrl-access_mode)<br/>                                                 | 包含值，這些值會指出如何將 [**明確 \_ 存取**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) 結構中的存取權限套用至信任者。<br/>                                                                                                                                      |
| [**ACL \_ 資訊 \_ 類別**](/windows/desktop/api/Winnt/ne-winnt-acl_information_class)<br/>                            | 包含值，這些值會指定要從 [存取控制清單](/windows/desktop/SecGloss/a-gly) 指派或抓取 (ACL) 的資訊類型。<br/>                                                               |
| [**AUDIT \_ 事件 \_ 類型**](/windows/desktop/api/Winnt/ne-winnt-audit_event_type)<br/>                                      | 定義指出正在進行審核之物件類型的值。 [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)和 [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)函數會使用這些值。<br/>   |
| [**AUDIT \_ 參數 \_ 類型**](/windows/desktop/api/Adtgen/ne-adtgen-audit_param_type)<br/>                                      | 定義可用之 audit 參數的類型。<br/>                                                                                                                                                                                                                   |
| [**AUTHZ \_ 內容 \_ 資訊 \_ 類別**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class)<br/>       | 指定要從現有 AuthzClientCoNtext 中取出的資訊類型。 [**AuthzGetInformationFromCoNtext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext)函數會使用這個列舉。<br/>                                                                  |
| [**AUTHZ \_ 安全性 \_ 屬性 \_ 操作**](/windows/desktop/api/Authz/ne-authz-authz_security_attribute_operation)<br/> | 指出呼叫 [**AuthzModifySecurityAttributes**](/windows/desktop/api/Authz/nf-authz-authzmodifysecurityattributes) 函式時，要對安全性屬性進行的修改類型。<br/>                                                                                                     |
| [**AUTHZ \_ SID \_ 操作**](/windows/desktop/api/Authz/ne-authz-authz_sid_operation)<br/>                                | 指出呼叫 [**AuthzModifySids**](/windows/desktop/api/Authz/nf-authz-authzmodifysids) 函式時可進行的 SID 作業類型。<br/>                                                                                                                                                |
| [**AZ \_ 的 \_ 常數**](/windows/win32/api/azroles/ne-azroles-az_prop_constants)<br/>                                    | 定義授權管理員所使用的常數。<br/>                                                                                                                                                                                                                           |
| [**強制 \_ 等級**](/windows/desktop/api/Winnt/ne-winnt-mandatory_level)<br/>                                         | 列出可能的安全性層級。<br/>                                                                                                                                                                                                                                        |
| [**多個 \_ 信任者 \_ 操作**](/windows/desktop/api/AccCtrl/ne-accctrl-multiple_trustee_operation)<br/>                  | 包含值，指出 [**受信任**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) 結構是否為模擬信任者。<br/>                                                                                                                                                                  |
| [**進程 \_ 調用 \_ 設定**](/windows/win32/api/accctrl/ne-accctrl-prog_invoke_setting)<br/>                                | 指出用來追蹤呼叫 [**TreeSetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treesetnamedsecurityinfoa) 或 [**TreeResetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-treeresetnamedsecurityinfoa) 函式之函數的初始設定。<br/>                                       |
| [**SE \_ 物件 \_ 類型**](/windows/desktop/api/AccCtrl/ne-accctrl-se_object_type)<br/>                                          | 包含值，這些值會對應至支援安全性的 Windows 物件類型。<br/>                                                                                                                                                                                     |
| [**安全性 \_ 模擬 \_ 等級**](/windows/desktop/api/Winnt/ne-winnt-security_impersonation_level)<br/>              | 包含指定安全性模擬層級的值。 安全性模擬等級會控管伺服器進程可代表用戶端 [進程](/windows/desktop/SecGloss/p-gly)採取的程度。<br/>                                 |
| [**SI \_ 頁面 \_ 類型**](/windows/desktop/api/Aclui/ne-aclui-si_page_type)<br/>                                              | 包含值，這些值表示存取控制編輯器屬性工作表中的屬性頁類型。<br/>                                                                                                                                                                      |
| [**SID \_ 名稱 \_ 使用**](/windows/desktop/api/Winnt/ne-winnt-sid_name_use)<br/>                                              | 包含值，這些值會指定 [安全識別碼](/windows/desktop/SecGloss/s-gly) (SID) 的類型。<br/>                                                                                                                |
| [**權杖 \_ 提升許可權 \_ 類型**](/windows/desktop/api/Winnt/ne-winnt-token_elevation_type)<br/>                             | 指出 [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) 函式所查詢或由 [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) 函數所設定之 token 的提升許可權類型。<br/>                                                                          |
| [**TOKEN \_ 資訊 \_ 類別**](/windows/desktop/api/Winnt/ne-winnt-token_information_class)<br/>                        | 包含值，這些值會指定要指派給 [存取權杖](/windows/desktop/SecGloss/a-gly)或從中抓取的資訊類型。<br/>                                                                                          |
| [**TOKEN \_ 類型**](/windows/desktop/api/Winnt/ne-winnt-token_type)<br/>                                                   | 包含區分 [主要權杖](/windows/desktop/SecGloss/p-gly) 和模擬 [權杖](/windows/desktop/SecGloss/i-gly)的值。<br/>                     |
| [**信任者 \_ 表單**](/windows/desktop/api/AccCtrl/ne-accctrl-trustee_form)<br/>                                               | 值，指出 [**受信任**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a)結構之 **ptstrName** 成員所指向的資料類型。<br/>                                                                                                                                                  |
| [**信任 \_ 類型**](/windows/desktop/api/AccCtrl/ne-accctrl-trustee_type)<br/>                                               | 值，指出受 [**信任**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) 結構識別之信任者的類型。<br/>                                                                                                                                                                             |
| [**\_已知的 \_ SID \_ 類型**](/windows/desktop/api/Winnt/ne-winnt-well_known_sid_type)<br/>                               |  (Sid) 的常用 [安全識別碼](/windows/desktop/SecGloss/s-gly) 清單。 程式可以將這些值傳遞至 [**CreateWellKnownSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createwellknownsid) 函式，以從這份清單建立 SID。<br/> |



 

 


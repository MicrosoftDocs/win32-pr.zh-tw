---
description: 用來建立安全描述項，以及取得和設定安全描述項元件的函數。
ms.assetid: d07dab5a-7c06-40c4-aa59-fa0baaaa77e7
title: 建立低層級安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6462dcd7672836df5f2c1f6b368723bc3a9488eff290dc22a071ce40279def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781481"
---
# <a name="low-level-security-descriptor-creation"></a>建立低層級安全描述項

低層級存取控制提供一組功能，可用來建立 [*安全描述項*](/windows/desktop/SecGloss/s-gly) ，以及取得和設定安全描述項的元件。 初始化和設定安全描述項元件的低層級函式僅適用于絕對格式的安全描述項。 取得安全描述項元件的低層級函式可搭配 [絕對和自我相關的安全描述項](absolute-and-self-relative-security-descriptors.md)。

[**InitializeSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesecuritydescriptor)函式會初始化 [**安全 \_ 描述項**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor)緩衝區。 初始化的安全描述項是 [*絕對*](/windows/desktop/SecGloss/a-gly) 格式，而且沒有擁有者、主要群組、 [*任意存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) 或 (SACL) 的 [*系統存取控制清單*](/windows/desktop/SecGloss/s-gly) 。 您可以使用下列低層級函數來取得或設定指定安全描述項的特定元件。



| 函式                                                             | 描述                                                                                                                                                               |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSecurityDescriptorControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) | 從安全描述項取出修訂和控制資訊。                                                                                                    |
| [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)       | 從安全描述項抓取 DACL。                                                                                                                            |
| [**GetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorgroup)     | 從安全描述項中，抓取 (SID) 的主要群組 [*安全性識別*](/windows/desktop/SecGloss/s-gly) 元。 |
| [**GetSecurityDescriptorLength**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorlength)   | 傳回安全描述項的長度。                                                                                                                              |
| [**GetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)     | 從安全描述項抓取擁有者 SID。                                                                                                                       |
| [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)       | 從安全描述項捕獲 SACL。                                                                                                                            |
| [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl)       | 將 DACL 放入安全描述項中，取代任何現有的 DACL。                                                                                                    |
| [**SetSecurityDescriptorGroup**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorgroup)     | 設定安全描述項的主要群組 SID。                                                                                                                      |
| [**SetSecurityDescriptorOwner**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorowner)     | 設定安全描述項的擁有者 SID。                                                                                                                              |
| [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl)       | 將 SACL 放入安全描述項中，取代任何現有的 SACL。                                                                                                    |



 

若要檢查安全描述項的修訂層級和結構 [*完整性*](/windows/desktop/SecGloss/i-gly) ，請呼叫 [**IsValidSecurityDescriptor**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor) 函數。

 

 

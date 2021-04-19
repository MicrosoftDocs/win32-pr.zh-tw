---
description: Microsoft Windows 安全性模型可讓您控制對工作物件的存取。 如需安全性的詳細資訊，請參閱 Access-Control 模型。
ms.assetid: 8d212292-f087-41e4-884e-cec4423dac49
title: 工作物件安全性和存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f5207e459bab2ae444282355844401e0b82e9c
ms.sourcegitcommit: 18023a15a4312c653a8dcc0feef23e3413a7f5dd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/25/2021
ms.locfileid: "106981907"
---
# <a name="job-object-security-and-access-rights"></a>工作物件安全性和存取權限

Microsoft Windows 安全性模型可讓您控制對工作物件的存取。 如需安全性的詳細資訊，請參閱 [存取控制模型](../secauthz/access-control-model.md)。

當您呼叫 [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)函式時，可以指定工作物件的 [安全描述項](../secauthz/security-descriptors.md)。 如果您指定 Null，工作物件會取得預設安全描述項。 工作物件之預設安全描述項中的 Acl 來自于建立者的主要或模擬權杖。

若要取得或設定工作物件的安全描述項，請呼叫 [**GetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getnamedsecurityinfoa)、 [**SetNamedSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setnamedsecurityinfoa)、 [**GetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-getsecurityinfo)或 [**SetSecurityInfo**](/windows/win32/api/aclapi/nf-aclapi-setsecurityinfo) 函數。

工作物件的有效存取權限包括 [標準存取權限](../secauthz/standard-access-rights.md) ，以及某些特定作業的存取權限。 下表列出所有物件使用的標準存取權限。

| 值                           | 意義                                                                                                                                                                                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **刪除** (0x00010000L)         | 刪除物件的必要參數。                                                                                                                                                                                                                                                           |
| **讀取 \_控制** (0x00020000L)  | 需要讀取物件安全描述項中的資訊，而不包含 SACL 中的資訊。 若要讀取或寫入 SACL，您必須要求 **存取 \_ 系統 \_ 安全性** 存取權限。 如需詳細資訊，請參閱 [SACL 訪問](../secauthz/sacl-access-right.md)許可權。 |
| **同步處理** (0x00100000L)    | 使用同步物件的權限。 這可讓執行緒等候，直到物件處於已發出信號的狀態。                                                                                                                                                                |
| **寫入 \_DAC** (0x00040000L)     | 修改物件安全描述項中的 DACL 時需要。                                                                                                                                                                                                                   |
| **寫入 \_擁有** 者 (0x00080000L)   | 需要變更物件之安全描述項中的擁有者。                                                                                                                                                                                                                  |



 

下表列出特定作業的存取權限。



| 值                                               | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **作業 \_物件的 \_ 所有 \_ 存取** (0x1F001F)              | 結合所有有效的工作物件存取權限。                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **作業 \_物件 \_ 指派 \_ 進程** (0x0001)            | 需要呼叫 [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) 函式，才能將進程指派給工作物件。                                                                                                                                                                                                                                                                                                                                                                |
| **作業 \_物件 \_ 查詢** (0x0004)                      | 若要取得工作物件的特定資訊（例如屬性和帳戶處理資訊）， (參閱 [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) 和 [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)) 。                                                                                                                                                                                                                                                                    |
| **作業 \_ (0x0002) 的物件 \_ 集 \_ 屬性**           | 需要呼叫 [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) 函式來設定工作物件的屬性。                                                                                                                                                                                                                                                                                                                                                                |
| **作業 \_ (0x0010) 的物件 \_ 集 \_ 安全性 \_ 屬性** | 不支援此旗標。 您必須針對與工作物件相關聯的每個進程個別設定安全性限制。**Windows Server 2003 和 WINDOWS XP：** 需要使用 **JobObjectSecurityLimitInformation** 資訊類別呼叫 [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)函式，以設定與工作物件相關聯之進程的安全性限制。 Windows Vista 和 Windows Server 2008 已移除對此旗標的支援。 <br/> |
| **作業 \_物件 \_ 終止** (0x0008)                  | 需要呼叫 [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) 函式，以終止工作物件中的所有進程。                                                                                                                                                                                                                                                                                                                                                                     |



 

[**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)傳回的控制碼具有工作物件的 **\_ \_ 所有 \_ 存取** 權。 當您呼叫 [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) 函式時，系統會針對物件的安全描述項，檢查要求的存取權限。 如果工作物件是在 [嵌套的作業](nested-jobs.md)階層中，具有工作物件存取權的呼叫端會隱含地存取階層中的所有子工作。

如果您想要讀取或寫入物件的 SACL，您可以向工作物件要求 **存取 \_ 系統 \_ 安全性** 存取權。 如需詳細資訊，請參閱 (Acl) 和[SACL 訪問](../secauthz/sacl-access-right.md)許可權[的存取控制清單](../secauthz/access-control-lists.md)。

您必須針對與工作物件相關聯的每個進程個別設定安全性限制，而不是為工作物件本身設定它們。 如需詳細資訊，請參閱 [進程安全性和存取權限](process-security-and-access-rights.md)。

**Windows Server 2003 和 WINDOWS XP：** 您可以使用 [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) 函數來設定工作物件的安全性限制。 這項功能已在 Windows Vista 和 Windows Server 2008 中移除。

 

 

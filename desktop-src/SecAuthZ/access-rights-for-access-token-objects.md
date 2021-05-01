---
description: 除非應用程式有許可權，否則應用程式無法變更物件的存取控制清單。
ms.assetid: 5f710fd8-33de-47c0-a8b2-baf3008c4ed7
title: Access-Token 物件的存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469081d2caa4e5ff7c9b7c55b4c09c31cff1acac
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327193"
---
# <a name="access-rights-for-access-token-objects"></a>Access-Token 物件的存取權限

除非應用程式有許可權，否則應用程式無法變更物件的存取控制清單。 這些許可權是由物件存取權杖中的安全描述項所控制。 如需安全性的詳細資訊，請參閱 [存取控制模型](access-control-model.md)。

若要取得或設定 [*存取權杖*](/windows/desktop/SecGloss/a-gly)的 [安全描述項](security-descriptors.md)，請呼叫 [**GetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity)和 [**SetKernelObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity)函數。

當您呼叫 [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) 或 [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) 函式來取得存取權杖的控制碼時，系統會針對權杖的安全描述項中的 DACL 檢查要求的 [存取權限](access-rights-and-access-masks.md) 。

以下是存取權杖物件的有效存取權限：

-   刪除、讀取 \_ 控制、寫入 \_ DAC，以及寫入 \_ 擁有者 [標準存取權限](standard-access-rights.md)。 存取權杖不支援同步處理標準存取權。
-   取得或設定物件安全描述項中 SACL 的 [存取 \_ 系統 \_ 安全性許可權](sacl-access-right.md) 。
-   存取權杖的特定存取權限，如下表所列。

    | 值                     | 意義                                                                                                                                                                                                                                                                           |
    |---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 權杖 \_ 調整 \_ 預設值    | 變更存取權杖的預設擁有者、主要群組或 DACL 所需。                                                                                                                                                                                                  |
    | 權杖 \_ 調整 \_ 群組     | 需要調整存取權杖中群組的屬性。                                                                                                                                                                                                               |
    | 權杖 \_ 調整 \_ 許可權 | 必須啟用或停用存取權杖中的許可權。                                                                                                                                                                                                                  |
    | 權杖 \_ 調整 \_ SESSIONID  | 需要調整存取權杖的會話識別碼。 需要「SE \_ TCB \_ 名稱」許可權。                                                                                                                                                                                    |
    | 權杖 \_ 指派 \_ 主要    | 需要將 [*主要權杖*](/windows/desktop/SecGloss/p-gly) 附加至 [*進程*](/windows/desktop/SecGloss/p-gly)。 \_ \_ 若要完成這項工作，也需要 SE ASSIGNPRIMARYTOKEN 名稱許可權。 |
    | 標記 \_ 重複          | 需要複製存取權杖。                                                                                                                                                                                                                                            |
    | 權杖 \_ 執行            | 等同于標準 \_ 許可權 \_ 執行。                                                                                                                                                                                                                                                |
    | 標記 \_ 模擬        | 需要將模擬存取權杖附加至進程。                                                                                                                                                                                                                    |
    | TOKEN \_ 查詢              | 查詢存取權杖的必要參數。                                                                                                                                                                                                                                                |
    | TOKEN \_ 查詢 \_ 來源      | 查詢存取權杖的來源所需。                                                                                                                                                                                                                                  |
    | 權杖 \_ 讀取               | 結合標準 \_ 許可權 \_ 讀取和權杖 \_ 查詢。                                                                                                                                                                                                                                 |
    | 標記 \_ 寫入              | 結合標準的 \_ 許可權 \_ 寫入、權杖 \_ 調整 \_ 許可權、權杖 \_ 調整 \_ 群組和權杖 \_ 調整 \_ 預設值。                                                                                                                                                                   |
    | 權杖 \_ 所有 \_ 存取        | 結合了權杖的所有可能存取權限。                                                                                                                                                                                                                                  |

    

     

 

 

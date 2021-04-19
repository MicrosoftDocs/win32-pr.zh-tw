---
description: 列出並描述原則物件的存取類型。
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: 原則物件存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971192"
---
# <a name="policy-object-access-rights"></a>原則物件存取權限

[**原則**](policy-object.md)物件具有下列物件特定的存取類型：



| 存取類型                         | Description                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 原則 \_ 視圖 \_ 區域 \_ 資訊    | 需要此存取類型才能讀取目標系統的其他安全性原則資訊。 這包括預設配額、審核、伺服器狀態和角色資訊，以及信任資訊。 列舉受信任的網域、帳戶和 [*許可權*](/windows/desktop/SecGloss/p-gly)也需要此存取類型。 |
| 原則 \_ 取得 \_ 私用 \_ 資訊   | 需要此存取類型才能查看敏感性資訊，例如針對信任的網域關聯性所建立的帳戶名稱。                                                                                                                                                                                                                              |
| 原則 \_ 信任 \_ 管理員                | 變更帳戶網域或主域資訊需要此存取類型。                                                                                                                                                                                                                                                                             |
| 原則 \_ 設定 \_ 預設 \_ 配額 \_ 限制 | 設定套用至使用者帳戶的預設系統配額。                                                                                                                                                                                                                                                                                                   |
| 原則 \_ 建立 \_ 秘密              | 需要此存取類型才能建立新的私用資料物件。                                                                                                                                                                                                                                                                                                    |
| 原則 \_ 建立 \_ 帳戶             | 建立新的 [**帳戶**](account-object.md) 物件時需要此存取類型。                                                                                                                                                                                                                                                                               |
| 原則 \_ 集 \_ 審核 \_ 需求    | 需要此存取類型才能更新系統的審核需求。                                                                                                                                                                                                                                                                                      |
| 原則 \_ 審核 \_ 記錄 \_ 管理員           | 需要此存取類型才能變更審核記錄的特性，例如其大小上限或審核記錄的保留期限，或清除記錄檔。                                                                                                                                                                                               |
| 原則 \_ 視圖 \_ 審核 \_ 資訊    | 需要此存取類型才能查看審核記錄或審核需求資訊。                                                                                                                                                                                                                                                                                  |
| 原則 \_ 伺服器 \_ 管理員               | 需要此存取類型才能修改伺服器狀態或 (master/replica) 資訊的角色。 您也需要變更複本來源和帳戶名稱資訊。                                                                                                                                                                                           |
| 原則 \_ 查閱 \_ 名稱               | 需要有此存取類型，才能在名稱和 Sid 之間轉譯。                                                                                                                                                                                                                                                                                                    |
| 原則 \_ 建立 \_ 許可權           | 尚不支援。                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a>一般存取遮罩

[**原則**](policy-object.md)物件會從一般存取類型發佈下列對應到特定存取類型：

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a>標準存取類型

此物件不支援 (選擇性) 同步處理標準存取類型。 支援所有必要的存取類型。 此物件類型所有支援之存取類型的遮罩為：

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 

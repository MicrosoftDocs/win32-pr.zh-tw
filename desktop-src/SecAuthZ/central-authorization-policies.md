---
description: 集中授權原則 (上限) 會將特定授權規則 (CAPRs) 收集到單一原則。
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: 集中授權原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0617f6bddb606d3c3fb3e5ccb6692c79c62a60f90de591b6ec3e04988db46f63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783222"
---
# <a name="central-authorization-policies"></a>集中授權原則

集中授權原則 (上限) 會將特定授權規則 (CAPRs) 收集到單一原則。 若要允許特定授權規則 (CAPRs) 合併到組織的整體授權原則，可將 CAPRs 同時參考並套用至一組資源。 這是藉由將多個 (以) 至端點的參考收集來完成。 一旦定義上限後，資源管理員就可以將其散發給資源，以將組織授權原則套用至資源。

端點具有下列屬性：

-   CAPRs 集合–現有 CAPR 物件的參考清單
-    (Sid 的識別碼) 
-   描述
-   名稱

系統管理員啟用檔案和資料夾的存取評估期間會評估上限。 在 [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) 呼叫期間，端點檢查會以邏輯方式結合任意的 ACL 檢查;這表示，若要取得 CAP 套用之檔案的存取權，使用者必須根據 CAP (其相關聯的 CAPRs) 和檔案上的任意 ACL 來存取兩者。

範例上限：

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a>端點定義

您可以使用 ADAC (或 PowerShell) 中的新 UX，在 Active Directory 中建立和編輯端點，以允許系統管理員建立端點並指定組成端點的一組 CAPRs。

 

 

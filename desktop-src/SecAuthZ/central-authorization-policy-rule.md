---
description: " (CAPR) 的集中授權原則規則用途，是提供組織授權原則之隔離層面的全網域定義。"
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: 集中授權原則規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5638633f655794464a9d603e1bb6a0380d2224170b9afe0f6314b1f8fee945b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783202"
---
# <a name="central-authorization-policy-rule"></a>集中授權原則規則

集中授權原則規則 (CAPR) 的目的，是要提供組織授權原則的隔離層面的全網域定義。 系統管理員會定義 CAPR，以強制執行其中一個特定的授權需求。 由於 CAPR 只定義了一個特定的授權原則需求，因此可以更單純地定義和瞭解組織的所有授權原則需求是否會編譯成單一原則定義。

CAPR 具有下列屬性：

-   名稱–識別系統管理員的 CAPR。
-   描述-定義 CAPR 的用途，以及 CAPR 取用者可能需要的任何資訊。
-   適用性運算式–定義將套用原則的資源或狀況。
-   ID –用於審核 CAPR 變更的識別碼。
-   有效存取控制原則– Windows 的安全描述項，其中包含定義有效授權原則的 DACL。
-   例外狀況運算式–一或多個運算式，提供覆寫原則的方法，並根據運算式的評估來授與主體的存取權。
-   暫存原則：選擇性的 Windows 安全描述項，其中包含的 DACL 會定義建議的授權原則， (存取控制專案的清單，而這些存取控制專案) 會針對有效的原則進行測試，但不會強制執行。 如果有效原則的結果和暫存原則之間有差異，則會在 audit 事件記錄檔中記錄差異。
    -   因為暫存可能會對系統效能造成無法預期的影響，所以群組原則系統管理員必須能夠選取預備環境生效的特定電腦。 這可讓現有的原則位於 OU 中的大部分電腦上，而預備環境則是在部分的電腦上進行。
    -   P2 –特定電腦上的本機系統管理員應該能夠停用暫存，如果該機器上的預備環境造成效能降低的情況過高。
-   Backlink 至 CAP –可參考此 CAPR 之任何 Cap 的 backlinks 清單。

在存取檢查期間，會根據適用性運算式評估 CAPR 的適用性。 如果有 CAPR，則會評估它是否會為要求的使用者提供所識別資源的要求存取權。 然後，會以邏輯方式聯結「維德角評估」的結果， **並與資源** 上的 DACL 結果和任何其他適用的 CAPRs 作用。

範例 CAPRs：

``` syntax
[HBI-POLICY]
APPLIES-TO="(@resource.confidentiality == HBI"
SD ="D:(A;;FA;;;AU;(@memberOf("Smartcard Logon")))"
StagingSD = "D:(A;;FA;;;AU;(@memberOf("Smartcard Logon") AND memberOfAny(Resource.ProjectGroups)))"
description="Control access to sensitive information"
 
[RETENTION-POLICY]
Applies-To="@resource.retention == true"
SD ="D:(A;;;FA;;BA)(A;;FR;;;WD)"
description="If the document is marked for retention, then it is read-only for everyone however Local Admins have 
full control to them to put them out of retention when the time comes"
 
[TEST-FINANCE-POLICY]
Applies-To="@resource.label == 'finance'"
SD="D:(A;;FA;;;AU;(member_of(FinanceGroup))"
description="Department: Only employees of the finance department should be able to read documents labeled as finance"
```

## <a name="deny-aces-in-capes"></a>CAPEs 中的 Deny Ace

在 Windows 8 拒絕 ace 將不會在 CAPR 中受到支援。 CAPR 撰寫 UX 將不允許建立拒絕 ACE。 此外，當 LSA 從 Active Directory 抓取端點時，LSA 會驗證沒有任何 CAPRs 具有拒絕 Ace。 如果在 CAPR 中找到 deny ACE，則會將端點視為無效，而不會複製到登錄或 SRM。

> [!Note]  
> 存取檢查不會強制出現任何拒絕 Ace。 將會套用 CAPR 中的 Deny Ace。 撰寫工具預期會導致無法進行此程式。

 

## <a name="cape-definition"></a>維德角定義

CAPRs 是透過 Active Directory 管理中心 (ADAC 中提供的新 UX 所建立。 ADAC 中的 ) 會提供新的工作選項來建立 CAPR。 選取此工作時，ADAC 會提示使用者提供一個對話方塊，要求使用者輸入 CAPR 名稱和描述。 提供這些專案時，將會啟用定義任何剩餘 CAPR 元素的控制項。 針對其餘的每個 CAPR 元素，UX 會呼叫 ACL UI 以允許定義運算式和/或 Acl。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[動態存取控制 (DAC) 案例](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 

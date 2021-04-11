---
description: " (CAPR) 的集中授權原則規則用途，是提供組織授權原則之隔離層面的全網域定義。"
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: 集中授權原則規則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda6279b2bf28f80f99a0e2608b5bf209855a76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027598"
---
# <a name="central-authorization-policy-rule"></a><span data-ttu-id="9fbd1-103">集中授權原則規則</span><span class="sxs-lookup"><span data-stu-id="9fbd1-103">Central Authorization Policy Rule</span></span>

<span data-ttu-id="9fbd1-104">集中授權原則規則 (CAPR) 的目的，是要提供組織授權原則的隔離層面的全網域定義。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-104">The purpose of the Central Authorization Policy Rule (CAPR) is to provide a domain-wide definition of an isolated aspect of the organization's authorization policy.</span></span> <span data-ttu-id="9fbd1-105">系統管理員會定義 CAPR，以強制執行其中一個特定的授權需求。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-105">The administrator defines the CAPR to enforce one of the specific authorization requirements.</span></span> <span data-ttu-id="9fbd1-106">由於 CAPR 只定義了一個特定的授權原則需求，因此可以更單純地定義和瞭解組織的所有授權原則需求是否會編譯成單一原則定義。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-106">Since the CAPR defines only one specific desired requirement of the authorization policy it can be more simply defined and understood than if all the authorization policy requirements of the organization are compiled into a single policy definition.</span></span>

<span data-ttu-id="9fbd1-107">CAPR 具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="9fbd1-107">The CAPR has the following attributes:</span></span>

-   <span data-ttu-id="9fbd1-108">名稱–識別系統管理員的 CAPR。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-108">Name – identifies the CAPR to the administrators.</span></span>
-   <span data-ttu-id="9fbd1-109">描述-定義 CAPR 的用途，以及 CAPR 取用者可能需要的任何資訊。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-109">Description – defines the purpose of the CAPR and any information that may be needed by consumers of the CAPR.</span></span>
-   <span data-ttu-id="9fbd1-110">適用性運算式–定義將套用原則的資源或狀況。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-110">Applicability Expression – defines the resources or situations in which the policy will be applied.</span></span>
-   <span data-ttu-id="9fbd1-111">ID –用於審核 CAPR 變更的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-111">ID – identifier for use in auditing of changes to the CAPR.</span></span>
-   <span data-ttu-id="9fbd1-112">有效存取控制原則– Windows 安全描述項，其中包含定義有效授權原則的 DACL。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-112">Effective Access Control Policy – a Windows security descriptor containing a DACL that defines the effective authorization policy.</span></span>
-   <span data-ttu-id="9fbd1-113">例外狀況運算式–一或多個運算式，提供覆寫原則的方法，並根據運算式的評估來授與主體的存取權。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-113">Exception Expression – one or more expressions that provide a means to override the policy and grant access to a principal according to the evaluation of the expression.</span></span>
-   <span data-ttu-id="9fbd1-114">暫存原則：選用的 Windows 安全描述項，其中包含的 DACL 會定義建議的授權原則， (存取控制專案的清單，) 這些存取控制專案會針對有效的原則進行測試，但不會加以強制執行。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-114">Staging Policy – an optional Windows security descriptor containing a DACL that defines a proposed authorization policy (list of access control entries) that will be tested against the effective policy but not enforced.</span></span> <span data-ttu-id="9fbd1-115">如果有效原則的結果和暫存原則之間有差異，則會在 audit 事件記錄檔中記錄差異。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-115">If there is a difference between the results of the effective policy and the staging policy the difference will be recorded in the audit event log.</span></span>
    -   <span data-ttu-id="9fbd1-116">因為暫存可能會對系統效能造成無法預期的影響，所以群組原則系統管理員必須能夠選取預備環境生效的特定電腦。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-116">Since staging can have an unpredictable effect on system performance, a Group Policy administrator must be able to select specific machines on which staging will be in effect.</span></span> <span data-ttu-id="9fbd1-117">這可讓現有的原則位於 OU 中的大部分電腦上，而預備環境則是在部分的電腦上進行。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-117">This allows the existing policy to be in place on most machines in an OU while staging is happening on a subset of the machines.</span></span>
    -   <span data-ttu-id="9fbd1-118">P2 –特定電腦上的本機系統管理員應該能夠停用暫存，如果該機器上的預備環境造成效能降低的情況過高。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-118">P2 – A local administrator on a particular machine should be able to disable staging if staging on that machine is causing too much of a performance degradation.</span></span>
-   <span data-ttu-id="9fbd1-119">Backlink 至 CAP –可參考此 CAPR 之任何 Cap 的 backlinks 清單。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-119">Backlink to CAP – A list of backlinks to any CAPs that may be referring to this CAPR.</span></span>

<span data-ttu-id="9fbd1-120">在存取檢查期間，會根據適用性運算式評估 CAPR 的適用性。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-120">During access check, the CAPR is be evaluated for applicability based on the applicability expression.</span></span> <span data-ttu-id="9fbd1-121">如果有 CAPR，則會評估它是否會為要求的使用者提供所識別資源的要求存取權。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-121">If a CAPR is applicable, it is evaluated for whether it provides the requesting user the requested access to the identified resource.</span></span> <span data-ttu-id="9fbd1-122">然後，會以邏輯方式聯結「維德角評估」的結果， **並與資源** 上的 DACL 結果和任何其他適用的 CAPRs 作用。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-122">The results of the CAPE evaluation is then logically joined by **AND** with the results of the DACL on the resource and any other applicable CAPRs in effect on the resource.</span></span>

<span data-ttu-id="9fbd1-123">範例 CAPRs：</span><span class="sxs-lookup"><span data-stu-id="9fbd1-123">Example CAPRs:</span></span>

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

## <a name="deny-aces-in-capes"></a><span data-ttu-id="9fbd1-124">CAPEs 中的 Deny Ace</span><span class="sxs-lookup"><span data-stu-id="9fbd1-124">Deny ACEs in CAPEs</span></span>

<span data-ttu-id="9fbd1-125">在 Windows 8 拒絕 Ace 將不會在 CAPR 中受到支援。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-125">In Windows 8 deny ACEs will not be supported in a CAPR.</span></span> <span data-ttu-id="9fbd1-126">CAPR 撰寫 UX 將不允許建立拒絕 ACE。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-126">The CAPR authoring UX will not allow creation of a deny ACE.</span></span> <span data-ttu-id="9fbd1-127">此外，當 LSA 從 Active Directory 抓取端點時，LSA 會驗證沒有任何 CAPRs 具有拒絕 Ace。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-127">Additionally, when the LSA retrieves the CAP from Active Directory, LSA will verify that no CAPRs have deny ACEs.</span></span> <span data-ttu-id="9fbd1-128">如果在 CAPR 中找到 deny ACE，則會將端點視為無效，而不會複製到登錄或 SRM。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-128">If a deny ACE is found in a CAPR then the CAP will be treated as invalid and not be copied to the registry or SRM.</span></span>

> [!Note]  
> <span data-ttu-id="9fbd1-129">存取檢查不會強制出現任何拒絕 Ace。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-129">The access check will not enforce that no deny ACEs are present.</span></span> <span data-ttu-id="9fbd1-130">將會套用 CAPR 中的 Deny Ace。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-130">Deny ACEs in a CAPR will be applied.</span></span> <span data-ttu-id="9fbd1-131">撰寫工具預期會導致無法進行此程式。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-131">It is expected that authoring tools will prevent this from happening.</span></span>

 

## <a name="cape-definition"></a><span data-ttu-id="9fbd1-132">維德角定義</span><span class="sxs-lookup"><span data-stu-id="9fbd1-132">CAPE Definition</span></span>

<span data-ttu-id="9fbd1-133">CAPRs 是透過 Active Directory 管理中心 (ADAC 中提供的新 UX 所建立。 ADAC 中的 ) 會提供新的工作選項來建立 CAPR。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-133">CAPRs are created though a new UX provided in Active Directory Administrative Center (ADAC.) In ADAC a new task option is provided to create a CAPR.</span></span> <span data-ttu-id="9fbd1-134">選取此工作時，ADAC 會提示使用者提供一個對話方塊，要求使用者輸入 CAPR 名稱和描述。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-134">When this task is selected, ADAC will prompt the user with a dialog asking the user for a CAPR name and a description.</span></span> <span data-ttu-id="9fbd1-135">提供這些專案時，將會啟用定義任何剩餘 CAPR 元素的控制項。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-135">When these are provided, the controls to define any of the remaining CAPR elements become enabled.</span></span> <span data-ttu-id="9fbd1-136">針對其餘的每個 CAPR 元素，UX 會呼叫 ACL UI 以允許定義運算式和/或 Acl。</span><span class="sxs-lookup"><span data-stu-id="9fbd1-136">For each of the remaining CAPR elements, the UX will call out to the ACL-UI to allow definition of expression and/or ACLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fbd1-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="9fbd1-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fbd1-138">**AccessCheck**</span><span class="sxs-lookup"><span data-stu-id="9fbd1-138">**AccessCheck**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[<span data-ttu-id="9fbd1-139">動態存取控制 (DAC) 案例</span><span class="sxs-lookup"><span data-stu-id="9fbd1-139">Dynamic Access Control (DAC) scenario</span></span>](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 

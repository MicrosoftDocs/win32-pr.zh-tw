---
title: " (Windows 篩選平台) 的存取控制"
description: 在 Windows 篩選平台 (WFP) 中，基底篩選引擎 (BFE) 服務會根據存取權杖和安全描述項來實行標準的 Windows 存取控制模型。
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "104321371"
---
# <a name="access-control-windows-filtering-platform"></a><span data-ttu-id="f0b28-103"> (Windows 篩選平台) 的存取控制</span><span class="sxs-lookup"><span data-stu-id="f0b28-103">Access Control (Windows Filtering Platform)</span></span>

<span data-ttu-id="f0b28-104">在 Windows 篩選平台 (WFP) 中，基底篩選引擎 (BFE) 服務會根據存取權杖和安全描述項來實行標準的 [Windows 存取控制模型](/windows/desktop/SecAuthZ/access-control-model) 。</span><span class="sxs-lookup"><span data-stu-id="f0b28-104">In Windows Filtering Platform (WFP), the Base Filtering Engine (BFE) service implements the standard [Windows access control model](/windows/desktop/SecAuthZ/access-control-model) based on access tokens and security descriptors.</span></span>

## <a name="access-control-model"></a><span data-ttu-id="f0b28-105">存取控制模型</span><span class="sxs-lookup"><span data-stu-id="f0b28-105">Access Control Model</span></span>

<span data-ttu-id="f0b28-106">加入新的 WFP 物件（例如篩選和子層）時，可以指定安全描述項。</span><span class="sxs-lookup"><span data-stu-id="f0b28-106">Security descriptors can be specified when adding new WFP objects, such as filters and sub-layers.</span></span> <span data-ttu-id="f0b28-107">安全描述項是使用 WFP 管理函式 **Fwpm \* GetSecurityInfo0** 和 **Fwpm \* SetSecurityInfo0** 來管理，其中 \* *\** _ 代表 WFP 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0b28-107">Security descriptors are managed using the WFP management functions **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0**, where \**\** _ stands for the WFP object's name.</span></span> <span data-ttu-id="f0b28-108">這些函式在語義上等同于 Windows [_ *GetSecurityInfo* \*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo)和 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)函數。</span><span class="sxs-lookup"><span data-stu-id="f0b28-108">These functions are semantically identical to the Windows [_ *GetSecurityInfo*\*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

> [!Note]  
> <span data-ttu-id="f0b28-109">無法從明確交易中呼叫 **Fwpm \* SetSecurityInfo0** 函數。</span><span class="sxs-lookup"><span data-stu-id="f0b28-109">The **Fwpm\*SetSecurityInfo0** functions cannot be called from within an explicit transaction.</span></span>

 

> [!Note]  
> <span data-ttu-id="f0b28-110">如果 **Fwpm \* SetSecurityInfo0** 函式是用來管理在相同會話內建立的動態物件，則只能從動態會話內呼叫這些函數。</span><span class="sxs-lookup"><span data-stu-id="f0b28-110">The **Fwpm\*SetSecurityInfo0** functions can only be called from within a dynamic session if they are being used to manage a dynamic object created within the same session.</span></span>

 

<span data-ttu-id="f0b28-111">篩選引擎的預設安全描述項 (下圖中的根引擎物件) 如下所示。</span><span class="sxs-lookup"><span data-stu-id="f0b28-111">The default security descriptor for the filter engine (the root Engine object in the diagram below) is as follows.</span></span>

-   <span data-ttu-id="f0b28-112">將內建系統管理員群組的 **一般 \_ 所有** (GA) 存取權限授與一般。</span><span class="sxs-lookup"><span data-stu-id="f0b28-112">Grant **GENERIC\_ALL** (GA) access rights to the built-in Administrators group.</span></span>
-   <span data-ttu-id="f0b28-113">授與 **一般 \_ 讀取** (GR) **一般 \_ 寫入** (GW) **一般 \_ 執行** (GX) 網路設定運算子的存取權限。</span><span class="sxs-lookup"><span data-stu-id="f0b28-113">Grant **GENERIC\_READ** (GR) **GENERIC\_WRITE** (GW) **GENERIC\_EXECUTE** (GX) access rights to network configuration operators.</span></span>
-   <span data-ttu-id="f0b28-114">授與 **GRGWGX** 存取權給下列服務安全識別碼 (ssid) ： MpsSvc (Windows 防火牆) 、NapAgent (網路存取保護代理程式) 、PolicyAgent (IPsec 原則代理程式) 、RpcSs (遠端程序呼叫) 和 WdiServiceHost (診斷服務裝載) 。</span><span class="sxs-lookup"><span data-stu-id="f0b28-114">Grant **GRGWGX** access rights to the following service security identifiers (SSIDs): MpsSvc (Windows Firewall), NapAgent (Network Access Protection Agent), PolicyAgent (IPsec Policy Agent), RpcSs (Remote Procedure Call), and WdiServiceHost (Diagnostic Service Host).</span></span>
-   <span data-ttu-id="f0b28-115">授與 **FWPM \_ ACTRL \_ OPEN** 和 **FWPM \_ ACTRL \_ 分類** 給每個人。</span><span class="sxs-lookup"><span data-stu-id="f0b28-115">Grant **FWPM\_ACTRL\_OPEN** and **FWPM\_ACTRL\_CLASSIFY** to everyone.</span></span> <span data-ttu-id="f0b28-116"> (這些都是 WFP 特定的存取權限，如下表所述。 ) </span><span class="sxs-lookup"><span data-stu-id="f0b28-116">(These are WFP-specific access rights, described in table below.)</span></span>

<span data-ttu-id="f0b28-117">其餘預設安全描述項是透過繼承來衍生。</span><span class="sxs-lookup"><span data-stu-id="f0b28-117">The remaining default security descriptors are derived through inheritance.</span></span>

<span data-ttu-id="f0b28-118">有一些存取檢查（例如 **Fwpm \* Add0**、 **Fwpm \* CreateEnumHandle0**、 **Fwpm \* SubscribeChanges0** 函式呼叫）無法在個別物件層級進行。</span><span class="sxs-lookup"><span data-stu-id="f0b28-118">There are some access checks, such as for **Fwpm\*Add0**, **Fwpm\*CreateEnumHandle0**, **Fwpm\*SubscribeChanges0** function calls, that cannot be done at the individual object level.</span></span> <span data-ttu-id="f0b28-119">針對這些函數，每個物件類型都有容器物件。</span><span class="sxs-lookup"><span data-stu-id="f0b28-119">For these functions, there are container objects for each object type.</span></span> <span data-ttu-id="f0b28-120">針對標準物件類型 (例如，提供者、標注、篩選) 、現有的 **Fwpm \* GetSecurityInfo0** 和 **Fwpm \* SetSecurityInfo0** 函式已多載，因此 null **GUID** 參數可識別相關聯的容器。</span><span class="sxs-lookup"><span data-stu-id="f0b28-120">For the standard object types (for example, providers, callouts, filters), the existing **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0** functions are overloaded, such that a null **GUID** parameter identifies the associated container.</span></span> <span data-ttu-id="f0b28-121">針對其他物件類型 (例如，網路事件和 IPsec 安全性關聯) ，有明確的函式可用於管理容器的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="f0b28-121">For the other object types (for example, network events and IPsec security associations), there are explicit functions for managing the container's security information.</span></span>

<span data-ttu-id="f0b28-122">BFE 支援自動繼承任意的存取控制清單 (DACL) 存取控制專案 (Ace) 。</span><span class="sxs-lookup"><span data-stu-id="f0b28-122">BFE supports automatic inheritance of Discretionary Access Control List (DACL) access control entries (ACEs).</span></span> <span data-ttu-id="f0b28-123">BFE 不支援) Ace (SACL 的系統存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="f0b28-123">BFE does not support System Access Control List (SACL) ACEs.</span></span> <span data-ttu-id="f0b28-124">物件會從其容器繼承 Ace。</span><span class="sxs-lookup"><span data-stu-id="f0b28-124">Objects inherit ACEs from their container.</span></span> <span data-ttu-id="f0b28-125">容器會從篩選引擎繼承 Ace。</span><span class="sxs-lookup"><span data-stu-id="f0b28-125">Containers inherit ACEs from the filter engine.</span></span> <span data-ttu-id="f0b28-126">傳播路徑如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="f0b28-126">The propagation paths are shown in the diagram below.</span></span>

![顯示 ACE 傳播路徑的圖表，以 ' Engine ' 開頭。](images/access-control.jpg)

<span data-ttu-id="f0b28-128">針對標準物件類型，BFE 會強制執行所有的一般和標準存取權限。</span><span class="sxs-lookup"><span data-stu-id="f0b28-128">For the standard object types, BFE enforces all the generic and standard access rights.</span></span> <span data-ttu-id="f0b28-129">此外，WFP 還定義了下列特定的存取權限。</span><span class="sxs-lookup"><span data-stu-id="f0b28-129">In addition, WFP defines the following specific access rights.</span></span>



| <span data-ttu-id="f0b28-130">WFP 存取權</span><span class="sxs-lookup"><span data-stu-id="f0b28-130">WFP Access Right</span></span>                                                                                                                        | <span data-ttu-id="f0b28-131">Description</span><span class="sxs-lookup"><span data-stu-id="f0b28-131">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b28-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ 新增**</span><span class="sxs-lookup"><span data-stu-id="f0b28-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span><br/>                                       | <span data-ttu-id="f0b28-133">將物件新增至容器所需。</span><span class="sxs-lookup"><span data-stu-id="f0b28-133">Required to add an object to a container.</span></span><br/>                                                                                                                     |
| <span data-ttu-id="f0b28-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ 新增 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="f0b28-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>                       | <span data-ttu-id="f0b28-135">需要建立物件的關聯。</span><span class="sxs-lookup"><span data-stu-id="f0b28-135">Required to create an association to an object.</span></span> <span data-ttu-id="f0b28-136">例如，若要加入參考標注的篩選準則，呼叫端必須具有標注的 [新增] \_ 連結存取權。</span><span class="sxs-lookup"><span data-stu-id="f0b28-136">For example, to add a filter that references a callout, the caller must have ADD\_LINK access to the callout.</span></span><br/> |
| <span data-ttu-id="f0b28-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ 開始 \_ 閱讀 \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="f0b28-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span><br/>    | <span data-ttu-id="f0b28-138">開始明確讀取交易的必要。</span><span class="sxs-lookup"><span data-stu-id="f0b28-138">Required to begin an explicit read transaction.</span></span><br/>                                                                                                               |
| <span data-ttu-id="f0b28-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ 開始 \_ 寫入 \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="f0b28-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span><br/> | <span data-ttu-id="f0b28-140">開始明確寫入交易所需。</span><span class="sxs-lookup"><span data-stu-id="f0b28-140">Required to begin an explicit write transaction.</span></span><br/>                                                                                                              |
| <span data-ttu-id="f0b28-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ 分類**</span><span class="sxs-lookup"><span data-stu-id="f0b28-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span><br/>                        | <span data-ttu-id="f0b28-142">需要針對使用者模式層進行分類。</span><span class="sxs-lookup"><span data-stu-id="f0b28-142">Required to classify against a user-mode layer.</span></span><br/>                                                                                                               |
| <span data-ttu-id="f0b28-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="f0b28-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span><br/>                                    | <span data-ttu-id="f0b28-144">列舉容器中的物件所需。</span><span class="sxs-lookup"><span data-stu-id="f0b28-144">Required to enumerate the objects in a container.</span></span> <span data-ttu-id="f0b28-145">不過，列舉值只會傳回呼叫端具有 FWPM \_ ACTRL READ 存取權的物件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f0b28-145">However, the enumerator only returns objects to which the caller has FWPM\_ACTRL\_READ access.</span></span><br/>              |
| <span data-ttu-id="f0b28-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="f0b28-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span><br/>                                    | <span data-ttu-id="f0b28-147">開啟具有 BFE 的會話時需要此參數。</span><span class="sxs-lookup"><span data-stu-id="f0b28-147">Required to open a session with BFE.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="f0b28-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ READ**</span><span class="sxs-lookup"><span data-stu-id="f0b28-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span><br/>                                    | <span data-ttu-id="f0b28-149">讀取物件的屬性時需要。</span><span class="sxs-lookup"><span data-stu-id="f0b28-149">Required to read an object's properties.</span></span><br/>                                                                                                                      |
| <span data-ttu-id="f0b28-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ READ \_ STATS**</span><span class="sxs-lookup"><span data-stu-id="f0b28-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span><br/>                 | <span data-ttu-id="f0b28-151">讀取統計資料所需。</span><span class="sxs-lookup"><span data-stu-id="f0b28-151">Required to read statistics.</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="f0b28-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ 訂閱**</span><span class="sxs-lookup"><span data-stu-id="f0b28-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span><br/>                     | <span data-ttu-id="f0b28-153">訂閱通知所需。</span><span class="sxs-lookup"><span data-stu-id="f0b28-153">Required to subscribe for notifications.</span></span> <span data-ttu-id="f0b28-154">訂閱者只會收到 FWPM \_ ACTRL 讀取權限之物件的通知 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f0b28-154">Subscribers will only receive notifications for objects to which they have FWPM\_ACTRL\_READ access.</span></span><br/>                 |
| <span data-ttu-id="f0b28-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="f0b28-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span><br/>                                 | <span data-ttu-id="f0b28-156">設定引擎選項的必要參數。</span><span class="sxs-lookup"><span data-stu-id="f0b28-156">Required to set engine options.</span></span><br/>                                                                                                                               |



 

<span data-ttu-id="f0b28-157">BFE 會略過核心模式呼叫端的所有存取檢查。</span><span class="sxs-lookup"><span data-stu-id="f0b28-157">BFE skips all access checks for kernel-mode callers.</span></span>

<span data-ttu-id="f0b28-158">為了防止系統管理員從 BFE 鎖定自己，內建 administrators 群組的成員一律會被授與 **FWPM \_ ACTRL \_ 開啟** 給引擎物件。</span><span class="sxs-lookup"><span data-stu-id="f0b28-158">In order to prevent administrators from locking themselves out of BFE, members of the built-in administrators group are always granted **FWPM\_ACTRL\_OPEN** to the engine object.</span></span> <span data-ttu-id="f0b28-159">因此，系統管理員可以透過下列步驟重新取得存取權。</span><span class="sxs-lookup"><span data-stu-id="f0b28-159">Thus, an administrator can regain access through the following steps.</span></span>

-   <span data-ttu-id="f0b28-160">啟用 **SE \_ 取得 \_ 擁有權 \_ 名稱** 許可權。</span><span class="sxs-lookup"><span data-stu-id="f0b28-160">Enable the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="f0b28-161">呼叫 [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)。</span><span class="sxs-lookup"><span data-stu-id="f0b28-161">Call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span> <span data-ttu-id="f0b28-162">呼叫會成功，因為呼叫端是內建系統管理員的成員。</span><span class="sxs-lookup"><span data-stu-id="f0b28-162">The call succeeds because the caller is a member of Built-in Administrators.</span></span>
-   <span data-ttu-id="f0b28-163">取得引擎物件的擁有權。</span><span class="sxs-lookup"><span data-stu-id="f0b28-163">Take ownership of the engine object.</span></span> <span data-ttu-id="f0b28-164">這會成功，因為呼叫端具有 **SE \_ 取得 \_ 擁有權 \_ 名稱** 許可權。</span><span class="sxs-lookup"><span data-stu-id="f0b28-164">This succeeds because the caller has the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="f0b28-165">更新 DACL。</span><span class="sxs-lookup"><span data-stu-id="f0b28-165">Update the DACL.</span></span> <span data-ttu-id="f0b28-166">這會成功，因為擁有者一律具有 **寫入 \_ DAC** 存取權</span><span class="sxs-lookup"><span data-stu-id="f0b28-166">This succeeds because the owner always has **WRITE\_DAC** access</span></span>

<span data-ttu-id="f0b28-167">因為 BFE 支援它自己的自訂審核，所以不會產生一般物件存取權審核。</span><span class="sxs-lookup"><span data-stu-id="f0b28-167">Since BFE supports its own custom auditing, it does not generate generic object access audits.</span></span> <span data-ttu-id="f0b28-168">因此，會忽略 SACL。</span><span class="sxs-lookup"><span data-stu-id="f0b28-168">Thus, the SACL is ignored.</span></span>

## <a name="wfp-required-access-rights"></a><span data-ttu-id="f0b28-169">需要 WFP 存取權限</span><span class="sxs-lookup"><span data-stu-id="f0b28-169">WFP Required Access Rights</span></span>

<span data-ttu-id="f0b28-170">下表顯示 WFP 函數所需的存取權限，以便存取各種篩選平臺物件。</span><span class="sxs-lookup"><span data-stu-id="f0b28-170">The table below shows the access rights required by the WFP functions in order to access various filtering platform objects.</span></span> <span data-ttu-id="f0b28-171">**FwpmFilter \* *_ 函數會列為存取標準物件的範例。所有存取標準物件的其他* 函式都會遵循 _ FwpmFilter \*** 函式存取模型。</span><span class="sxs-lookup"><span data-stu-id="f0b28-171">The **FwpmFilter\**_ functions are listed as an example for accessing the standard objects. All the other functions that access standard objects follow the _\* FwpmFilter\**\* functions access model.</span></span>



<span data-ttu-id="f0b28-172">函式</span><span class="sxs-lookup"><span data-stu-id="f0b28-172">Function</span></span>

<span data-ttu-id="f0b28-173">已核取物件</span><span class="sxs-lookup"><span data-stu-id="f0b28-173">Object Checked</span></span>

<span data-ttu-id="f0b28-174">所需的存取</span><span class="sxs-lookup"><span data-stu-id="f0b28-174">Access Required</span></span>

[<span data-ttu-id="f0b28-175">**FwpmEngineOpen0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-175">**FwpmEngineOpen0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

<span data-ttu-id="f0b28-176">引擎</span><span class="sxs-lookup"><span data-stu-id="f0b28-176">Engine</span></span>

<span data-ttu-id="f0b28-177">**FWPM \_ ACTRL \_ OPEN**</span><span class="sxs-lookup"><span data-stu-id="f0b28-177">**FWPM\_ACTRL\_OPEN**</span></span>

[<span data-ttu-id="f0b28-178">**FwpmEngineGetOption0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-178">**FwpmEngineGetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

<span data-ttu-id="f0b28-179">引擎</span><span class="sxs-lookup"><span data-stu-id="f0b28-179">Engine</span></span>

<span data-ttu-id="f0b28-180">**FWPM \_ ACTRL \_ READ**</span><span class="sxs-lookup"><span data-stu-id="f0b28-180">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="f0b28-181">**FwpmEngineSetOption0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-181">**FwpmEngineSetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

<span data-ttu-id="f0b28-182">引擎</span><span class="sxs-lookup"><span data-stu-id="f0b28-182">Engine</span></span>

<span data-ttu-id="f0b28-183">**FWPM \_ ACTRL \_ 寫入**</span><span class="sxs-lookup"><span data-stu-id="f0b28-183">**FWPM\_ACTRL\_WRITE**</span></span>

[<span data-ttu-id="f0b28-184">**FwpmSessionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-184">**FwpmSessionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

<span data-ttu-id="f0b28-185">引擎</span><span class="sxs-lookup"><span data-stu-id="f0b28-185">Engine</span></span>

<span data-ttu-id="f0b28-186">**FWPM \_ ACTRL \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="f0b28-186">**FWPM\_ACTRL\_ENUM**</span></span>

[<span data-ttu-id="f0b28-187">**FwpmTransactionBegin0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-187">**FwpmTransactionBegin0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

<span data-ttu-id="f0b28-188">引擎</span><span class="sxs-lookup"><span data-stu-id="f0b28-188">Engine</span></span>

<span data-ttu-id="f0b28-189">**FWPM \_ACTRL \_ BEGIN \_ READ \_ TXN**  &  **FWPM \_ ACTRL \_ BEGIN \_ WRITE \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="f0b28-189">**FWPM\_ACTRL\_BEGIN\_READ\_TXN** & **FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>

[<span data-ttu-id="f0b28-190">**FwpmFilterAdd0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-190">**FwpmFilterAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

<span data-ttu-id="f0b28-191">容器提供者</span><span class="sxs-lookup"><span data-stu-id="f0b28-191">Container Provider</span></span><br/> <span data-ttu-id="f0b28-192">層</span><span class="sxs-lookup"><span data-stu-id="f0b28-192">Layer</span></span><br/> <span data-ttu-id="f0b28-193">Sub-Layer</span><span class="sxs-lookup"><span data-stu-id="f0b28-193">Sub-Layer</span></span><br/> <span data-ttu-id="f0b28-194">圖說文字</span><span class="sxs-lookup"><span data-stu-id="f0b28-194">Callout</span></span><br/> <span data-ttu-id="f0b28-195">提供者內容</span><span class="sxs-lookup"><span data-stu-id="f0b28-195">Provider Context</span></span><br/>

<span data-ttu-id="f0b28-196">**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ ADD \_ LINK**</span><span class="sxs-lookup"><span data-stu-id="f0b28-196">**FWPM\_ACTRL\_ADDFWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="f0b28-197">**FWPM \_ ACTRL \_ 新增 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="f0b28-197">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="f0b28-198">**FWPM \_ ACTRL \_ 新增 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="f0b28-198">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="f0b28-199">**FWPM \_ ACTRL \_ 新增 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="f0b28-199">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="f0b28-200">**FWPM \_ ACTRL \_ 新增 \_ 連結**</span><span class="sxs-lookup"><span data-stu-id="f0b28-200">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>

<span data-ttu-id="f0b28-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="f0b28-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span></span><br/>

<span data-ttu-id="f0b28-202">篩選</span><span class="sxs-lookup"><span data-stu-id="f0b28-202">Filter</span></span>

<span data-ttu-id="f0b28-203">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="f0b28-203">**DELETE**</span></span>

<span data-ttu-id="f0b28-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span><span class="sxs-lookup"><span data-stu-id="f0b28-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span></span><br/>

<span data-ttu-id="f0b28-205">篩選</span><span class="sxs-lookup"><span data-stu-id="f0b28-205">Filter</span></span>

<span data-ttu-id="f0b28-206">**FWPM \_ ACTRL \_ READ**</span><span class="sxs-lookup"><span data-stu-id="f0b28-206">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="f0b28-207">**FwpmFilterCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-207">**FwpmFilterCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

<span data-ttu-id="f0b28-208">容器篩選</span><span class="sxs-lookup"><span data-stu-id="f0b28-208">Container Filter</span></span><br/>

<span data-ttu-id="f0b28-209">**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ READ**</span><span class="sxs-lookup"><span data-stu-id="f0b28-209">**FWPM\_ACTRL\_ENUMFWPM\_ACTRL\_READ**</span></span><br/>

[<span data-ttu-id="f0b28-210">**FwpmFilterSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-210">**FwpmFilterSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

<span data-ttu-id="f0b28-211">容器</span><span class="sxs-lookup"><span data-stu-id="f0b28-211">Container</span></span>

<span data-ttu-id="f0b28-212">**FWPM \_ ACTRL \_ 訂閱**</span><span class="sxs-lookup"><span data-stu-id="f0b28-212">**FWPM\_ACTRL\_SUBSCRIBE**</span></span>

[<span data-ttu-id="f0b28-213">**FwpmFilterSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-213">**FwpmFilterSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

<span data-ttu-id="f0b28-214">容器</span><span class="sxs-lookup"><span data-stu-id="f0b28-214">Container</span></span>

<span data-ttu-id="f0b28-215">**FWPM \_ ACTRL \_ READ**</span><span class="sxs-lookup"><span data-stu-id="f0b28-215">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="f0b28-216">**IPsecGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-216">**IPsecGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

<span data-ttu-id="f0b28-217">IPsec SA 資料庫</span><span class="sxs-lookup"><span data-stu-id="f0b28-217">IPsec SA DB</span></span>

<span data-ttu-id="f0b28-218">**FWPM \_ ACTRL \_ READ \_ STATS**</span><span class="sxs-lookup"><span data-stu-id="f0b28-218">**FWPM\_ACTRL\_READ\_STATS**</span></span>

<span data-ttu-id="f0b28-219">[**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaCoNtextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span><span class="sxs-lookup"><span data-stu-id="f0b28-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span></span><br/> [<span data-ttu-id="f0b28-220">**IPsecSaCoNtextAddInbound0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-220">**IPsecSaContextAddInbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [<span data-ttu-id="f0b28-221">**IPsecSaCoNtextAddOutbound0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-221">**IPsecSaContextAddOutbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

<span data-ttu-id="f0b28-222">IPsec SA 資料庫</span><span class="sxs-lookup"><span data-stu-id="f0b28-222">IPsec SA DB</span></span>

<span data-ttu-id="f0b28-223">**FWPM \_ ACTRL \_ 新增**</span><span class="sxs-lookup"><span data-stu-id="f0b28-223">**FWPM\_ACTRL\_ADD**</span></span>

<span data-ttu-id="f0b28-224">[**IPsecSaCoNtextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaCoNtextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span><span class="sxs-lookup"><span data-stu-id="f0b28-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span></span><br/>

<span data-ttu-id="f0b28-225">IPsec SA 資料庫</span><span class="sxs-lookup"><span data-stu-id="f0b28-225">IPsec SA DB</span></span>

<span data-ttu-id="f0b28-226">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="f0b28-226">**DELETE**</span></span>

[<span data-ttu-id="f0b28-227">**IPsecSaCoNtextGetById0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-227">**IPsecSaContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

<span data-ttu-id="f0b28-228">IPsec SA 資料庫</span><span class="sxs-lookup"><span data-stu-id="f0b28-228">IPsec SA DB</span></span>

<span data-ttu-id="f0b28-229">**FWPM \_ ACTRL \_ READ**</span><span class="sxs-lookup"><span data-stu-id="f0b28-229">**FWPM\_ACTRL\_READ**</span></span>

<span data-ttu-id="f0b28-230">[**IPsecSaCoNtextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span><span class="sxs-lookup"><span data-stu-id="f0b28-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span></span><br/>

<span data-ttu-id="f0b28-231">IPsec SA 資料庫</span><span class="sxs-lookup"><span data-stu-id="f0b28-231">IPsec SA DB</span></span>

<span data-ttu-id="f0b28-232">**FWPM \_ACTRL \_ 列舉**  &  **FWPM \_ ACTRL \_ READ**</span><span class="sxs-lookup"><span data-stu-id="f0b28-232">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="f0b28-233">**IkeextGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-233">**IkeextGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

<span data-ttu-id="f0b28-234">IKE SA 資料庫</span><span class="sxs-lookup"><span data-stu-id="f0b28-234">IKE SA DB</span></span>

<span data-ttu-id="f0b28-235">**FWPM \_ ACTRL \_ READ \_ STATS**</span><span class="sxs-lookup"><span data-stu-id="f0b28-235">**FWPM\_ACTRL\_READ\_STATS**</span></span>

[<span data-ttu-id="f0b28-236">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-236">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

<span data-ttu-id="f0b28-237">IKE SA 資料庫</span><span class="sxs-lookup"><span data-stu-id="f0b28-237">IKE SA DB</span></span>

<span data-ttu-id="f0b28-238">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="f0b28-238">**DELETE**</span></span>

[<span data-ttu-id="f0b28-239">**IkeextSaGetById0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-239">**IkeextSaGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

<span data-ttu-id="f0b28-240">IKE SA 資料庫</span><span class="sxs-lookup"><span data-stu-id="f0b28-240">IKE SA DB</span></span>

<span data-ttu-id="f0b28-241">**FWPM \_ ACTRL \_ READ**</span><span class="sxs-lookup"><span data-stu-id="f0b28-241">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="f0b28-242">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-242">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

<span data-ttu-id="f0b28-243">IKE SA 資料庫</span><span class="sxs-lookup"><span data-stu-id="f0b28-243">IKE SA DB</span></span>

<span data-ttu-id="f0b28-244">**FWPM \_ACTRL \_ 列舉**  &  **FWPM \_ ACTRL \_ READ**</span><span class="sxs-lookup"><span data-stu-id="f0b28-244">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="f0b28-245">**FwpmNetEventCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="f0b28-245">**FwpmNetEventCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

<span data-ttu-id="f0b28-246">容器</span><span class="sxs-lookup"><span data-stu-id="f0b28-246">Container</span></span>

<span data-ttu-id="f0b28-247">**FWPM \_ ACTRL \_ 列舉**</span><span class="sxs-lookup"><span data-stu-id="f0b28-247">**FWPM\_ACTRL\_ENUM**</span></span>

<span data-ttu-id="f0b28-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="f0b28-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span></span><br/>

<span data-ttu-id="f0b28-249">除了個別篩選和提供者內容以外，不會有其他存取權檢查</span><span class="sxs-lookup"><span data-stu-id="f0b28-249">No additional access checks beyond those for the individual filters and provider contexts</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="f0b28-250">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0b28-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0b28-251">**標準存取權限**</span><span class="sxs-lookup"><span data-stu-id="f0b28-251">**Standard Access Rights**</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="f0b28-252">Windows 存取控制模型</span><span class="sxs-lookup"><span data-stu-id="f0b28-252">Windows access control model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[<span data-ttu-id="f0b28-253">**Windows 篩選平台存取權限識別碼**</span><span class="sxs-lookup"><span data-stu-id="f0b28-253">**Windows Filtering Platform Access Rights Identifiers**</span></span>](access-right-identifiers.md)
</dt> </dl>

 


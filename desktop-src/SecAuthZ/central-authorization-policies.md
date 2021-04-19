---
description: 集中授權原則 (上限) 會將特定授權規則 (CAPRs) 收集到單一原則。
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: 集中授權原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b890236b0dae0f8f8d51254def4e1607cc35894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973905"
---
# <a name="central-authorization-policies"></a><span data-ttu-id="d6f22-103">集中授權原則</span><span class="sxs-lookup"><span data-stu-id="d6f22-103">Central Authorization Policies</span></span>

<span data-ttu-id="d6f22-104">集中授權原則 (上限) 會將特定授權規則 (CAPRs) 收集到單一原則。</span><span class="sxs-lookup"><span data-stu-id="d6f22-104">A Central Authorization Policy (CAP) collects the specific authorization rules (CAPRs) into a single policy.</span></span> <span data-ttu-id="d6f22-105">若要允許特定授權規則 (CAPRs) 合併到組織的整體授權原則，可將 CAPRs 同時參考並套用至一組資源。</span><span class="sxs-lookup"><span data-stu-id="d6f22-105">To allow the specific authorization rules (CAPRs) to be combined into the holistic authorization policy of the organization, CAPRs can be referenced together and applied to a set of resources.</span></span> <span data-ttu-id="d6f22-106">這是藉由將多個 (以) 至端點的參考收集來完成。</span><span class="sxs-lookup"><span data-stu-id="d6f22-106">This is done by collecting multiple (by reference) into a CAP.</span></span> <span data-ttu-id="d6f22-107">一旦定義上限後，資源管理員就可以將其散發給資源，以將組織授權原則套用至資源。</span><span class="sxs-lookup"><span data-stu-id="d6f22-107">Once a CAP is defined it can be distributed consumed by resource managers to apply the organizations authorization policy to resources.</span></span>

<span data-ttu-id="d6f22-108">端點具有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="d6f22-108">A CAP has the following attributes:</span></span>

-   <span data-ttu-id="d6f22-109">CAPRs 集合–現有 CAPR 物件的參考清單</span><span class="sxs-lookup"><span data-stu-id="d6f22-109">Collection of CAPRs – a list of references to existing CAPR objects</span></span>
-   <span data-ttu-id="d6f22-110"> (Sid 的識別碼) </span><span class="sxs-lookup"><span data-stu-id="d6f22-110">An identifier (Sid)</span></span>
-   <span data-ttu-id="d6f22-111">描述</span><span class="sxs-lookup"><span data-stu-id="d6f22-111">Description</span></span>
-   <span data-ttu-id="d6f22-112">Name</span><span class="sxs-lookup"><span data-stu-id="d6f22-112">Name</span></span>

<span data-ttu-id="d6f22-113">系統管理員啟用檔案和資料夾的存取評估期間會評估上限。</span><span class="sxs-lookup"><span data-stu-id="d6f22-113">A CAP is evaluated during access evaluation for files and folders on which an administrator enables it.</span></span> <span data-ttu-id="d6f22-114">在 [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) 呼叫期間，端點檢查會以邏輯方式結合任意的 ACL 檢查;這表示，若要取得 CAP 套用之檔案的存取權，使用者必須根據 CAP (其相關聯的 CAPRs) 和檔案上的任意 ACL 來存取兩者。</span><span class="sxs-lookup"><span data-stu-id="d6f22-114">During an [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) call, the CAP check is logically combined with the discretionary ACL check; this means that in order to obtain access to a file to which the CAP applies, a user needs to have access both according to the CAP (its associated CAPRs) and the discretionary ACL on the file.</span></span>

<span data-ttu-id="d6f22-115">範例上限：</span><span class="sxs-lookup"><span data-stu-id="d6f22-115">Example CAP:</span></span>

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a><span data-ttu-id="d6f22-116">端點定義</span><span class="sxs-lookup"><span data-stu-id="d6f22-116">CAP Definition</span></span>

<span data-ttu-id="d6f22-117">您可以使用 ADAC (或 PowerShell) 中的新 UX，在 Active Directory 中建立和編輯端點，以允許系統管理員建立端點並指定組成端點的一組 CAPRs。</span><span class="sxs-lookup"><span data-stu-id="d6f22-117">A CAP is created and edited in Active Directory using a new UX in ADAC (or PowerShell) that allows the administrator to create a CAP and specify a set of CAPRs that make up the CAP.</span></span>

 

 

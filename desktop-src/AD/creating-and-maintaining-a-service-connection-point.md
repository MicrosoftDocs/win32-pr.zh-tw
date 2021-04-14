---
title: 建立和維護服務連接點
description: 使用 SCP 發佈時，請記住，它必須包含服務實例的最新資料。
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- 建立和維護服務連接點 AD
- 服務連接點 AD、建立和維護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023265"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a><span data-ttu-id="40b3f-105">建立和維護服務連接點</span><span class="sxs-lookup"><span data-stu-id="40b3f-105">Creating and Maintaining a Service Connection Point</span></span>

<span data-ttu-id="40b3f-106">使用 SCP 發佈時，請記住，它必須包含服務實例的最新資料。</span><span class="sxs-lookup"><span data-stu-id="40b3f-106">When publishing with an SCP, remember that it must contain current data about the service instance.</span></span> <span data-ttu-id="40b3f-107">否則，系結至 SCP 的用戶端會取出過期的資料。</span><span class="sxs-lookup"><span data-stu-id="40b3f-107">Otherwise, clients that bind to the SCP retrieve outdated data.</span></span> <span data-ttu-id="40b3f-108">建立 SCP 的服務安裝程式會指定 Scp 屬性的初始值。</span><span class="sxs-lookup"><span data-stu-id="40b3f-108">Your service installer, that creates an SCP, specifies the initial values for the SCPs attributes.</span></span> <span data-ttu-id="40b3f-109">然後，當服務實例啟動時，它必須找出 SCP 並更新屬性值（如有必要）。</span><span class="sxs-lookup"><span data-stu-id="40b3f-109">Then, when the service instance starts, it must locate the SCP and update the attribute values, if necessary.</span></span> <span data-ttu-id="40b3f-110">如此一來，用戶端就可以確保最新的資料。</span><span class="sxs-lookup"><span data-stu-id="40b3f-110">In this way, clients are assured the most current data.</span></span>

<span data-ttu-id="40b3f-111">建立 SCP 之後，您的服務安裝程式會執行兩個額外的步驟，讓您的服務更新 SCP：</span><span class="sxs-lookup"><span data-stu-id="40b3f-111">After creating the SCP, your service installer performs two additional steps that enable your service to update the SCP:</span></span>

-   <span data-ttu-id="40b3f-112">在 SCP 物件的安全描述項中設定 Ace，讓服務在執行時間修改 SCP 屬性。</span><span class="sxs-lookup"><span data-stu-id="40b3f-112">Set ACEs in the security descriptor of the SCP object to enable the service to modify SCP attributes at run time.</span></span> <span data-ttu-id="40b3f-113">如需詳細資訊和程式碼範例，請參閱 [啟用服務帳戶以存取 SCP 屬性](enabling-service-account-to-access-scp-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="40b3f-113">For more information and a code example, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>
-   <span data-ttu-id="40b3f-114">在服務主機電腦上的登錄中快取 SCP 的 **objectGUID** 。</span><span class="sxs-lookup"><span data-stu-id="40b3f-114">Cache the **objectGUID** of the SCP in the registry on the service host computer.</span></span> <span data-ttu-id="40b3f-115">服務會抓取快取的 GUID 以系結至 SCP，以驗證並更新其屬性。</span><span class="sxs-lookup"><span data-stu-id="40b3f-115">The service retrieves the cached GUID to bind to the SCP to verify and update its attributes.</span></span>

<span data-ttu-id="40b3f-116">服務安裝程式會快取 SCP 的 **objectGUID** ，而不是其 DN。</span><span class="sxs-lookup"><span data-stu-id="40b3f-116">The service installer caches the SCP's **objectGUID** rather than its DN.</span></span> <span data-ttu-id="40b3f-117">**ObjectGUID** 永遠不會變更，不論 SCP 是否已移動或重新命名。</span><span class="sxs-lookup"><span data-stu-id="40b3f-117">The **objectGUID** never changes, regardless of whether the SCP is moved or renamed.</span></span> <span data-ttu-id="40b3f-118">如果系統管理員移動或重新命名 SCP，則 DN 可能會變更。</span><span class="sxs-lookup"><span data-stu-id="40b3f-118">The DN can change if an administrator moves or renames the SCP.</span></span> <span data-ttu-id="40b3f-119">例如，如果您將 SCP 建立為電腦物件的子系，則如果電腦已重新命名或移至不同的網域或組織單位，SCP 的辨別名稱就會變更。</span><span class="sxs-lookup"><span data-stu-id="40b3f-119">For example, if you create an SCP as a child of a computer object, the distinguished name of the SCP changes if the computer is renamed or moved to a different domain or organizational unit.</span></span>

<span data-ttu-id="40b3f-120">當服務安裝程式建立 SCP 時，它必須讀取新建立之物件的 **objectGUID** ，並在服務主機電腦的登錄中加以快取。</span><span class="sxs-lookup"><span data-stu-id="40b3f-120">When a service installer creates an SCP, it must read the **objectGUID** of the newly created object and cache it in the registry of the service host computer.</span></span> <span data-ttu-id="40b3f-121">使用 [**IADs：： get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) 方法可取得適用于系結的字串格式的 **objectGUID** 值。</span><span class="sxs-lookup"><span data-stu-id="40b3f-121">Use the [**IADs::get\_GUID**](/windows/desktop/ADSI/iads-property-methods) method to get the **objectGUID** value in string format suitable for binding.</span></span> <span data-ttu-id="40b3f-122">將 GUID 字串快取為下列登錄機碼下的值。</span><span class="sxs-lookup"><span data-stu-id="40b3f-122">Cache the GUID string as a value under the following registry key.</span></span>

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

<span data-ttu-id="40b3f-123">其中「廠商名稱」和「產品名稱」可識別廠商和產品。</span><span class="sxs-lookup"><span data-stu-id="40b3f-123">Where "vendor name" and "product name" identify the vendor and product.</span></span>

<span data-ttu-id="40b3f-124">當服務啟動時，會從登錄抓取快取的 GUID 字串，並使用它來系結至 SCP。</span><span class="sxs-lookup"><span data-stu-id="40b3f-124">When the service starts, it retrieves the cached GUID string from the registry and uses it to bind to the SCP.</span></span> <span data-ttu-id="40b3f-125">服務會讀取重要的 SCP 屬性，並將它們與目前的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="40b3f-125">The service reads the important SCP attributes and compares them to current values.</span></span> <span data-ttu-id="40b3f-126">如果 SCP 值過期，則服務會更新這些值。</span><span class="sxs-lookup"><span data-stu-id="40b3f-126">If the SCP values are outdated, the service updates them.</span></span> <span data-ttu-id="40b3f-127">服務可能需要更新的值包括 **關鍵字**、 **serviceBindingInformation**、 **serviceDNSName** 和 **serviceDNSNameType**。</span><span class="sxs-lookup"><span data-stu-id="40b3f-127">Values that the service might require to update include **keywords**, **serviceBindingInformation**, **serviceDNSName**, and **serviceDNSNameType**.</span></span>

## <a name="examples"></a><span data-ttu-id="40b3f-128">範例</span><span class="sxs-lookup"><span data-stu-id="40b3f-128">Examples</span></span>

-   [<span data-ttu-id="40b3f-129">腳本範例</span><span class="sxs-lookup"><span data-stu-id="40b3f-129">Script samples</span></span>](script-samples-for-managing-service-connection-points.md)
-   [<span data-ttu-id="40b3f-130">C/c + +) 範例 (程式碼</span><span class="sxs-lookup"><span data-stu-id="40b3f-130">Code (C/C++) samples</span></span>](code-samples-for-managing-service-connection-points.md)

 

 
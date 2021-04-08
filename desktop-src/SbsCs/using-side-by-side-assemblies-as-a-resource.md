---
description: 使用並存元件作為資源
ms.assetid: f7963d37-93c4-49d6-af7d-fc692f632894
title: 使用並存元件作為資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b97265b48f4ce8f3c87a87ec4ca9ea2b8252819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943340"
---
# <a name="using-side-by-side-assemblies-as-a-resource"></a><span data-ttu-id="c6300-103">使用並存元件作為資源</span><span class="sxs-lookup"><span data-stu-id="c6300-103">Using Side-by-Side Assemblies as a Resource</span></span>

<span data-ttu-id="c6300-104">您可以將資訊清單新增至應用程式，做為應用程式二進位可執行檔標頭檔中的資源。</span><span class="sxs-lookup"><span data-stu-id="c6300-104">You can add a manifest to a application as a resource in the application's binary executable header file.</span></span> <span data-ttu-id="c6300-105">資訊清單 \_ 資源識別碼的值 \_ 會決定載入器如何使用資訊清單中所述的並存元件相依性。</span><span class="sxs-lookup"><span data-stu-id="c6300-105">The value of the MANIFEST\_RESOURCE\_ID determines how the side-by-side assembly dependencies described in the manifest are used by the loader.</span></span>

<span data-ttu-id="c6300-106">如果您將資訊清單 \_ 資源 \_ 識別碼設定為1，則載入器會使用資訊清單中指定的並存元件相依性作為進程的預設值。</span><span class="sxs-lookup"><span data-stu-id="c6300-106">If you set the MANIFEST\_RESOURCE\_ID to 1, the loader uses the side-by-side assembly dependencies specified in the manifest as the process default.</span></span> <span data-ttu-id="c6300-107">所有外掛程式也會使用此進程預設。</span><span class="sxs-lookup"><span data-stu-id="c6300-107">All plug-ins also use this process default.</span></span>

<span data-ttu-id="c6300-108">下表摘要說明 \_ \_ 當應用程式使用-DISOLATION \_ 感知啟用旗標進行編譯時，載入器如何針對不同的資訊清單資源識別碼值使用資訊清單 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c6300-108">The following table summarizes how the loader uses the manifest for different values of MANIFEST\_RESOURCE\_ID when the application is compiled with the -DISOLATION\_AWARE\_ENABLED flag.</span></span> <span data-ttu-id="c6300-109">請注意，值1-16 是保留供 Windows XP 使用。</span><span class="sxs-lookup"><span data-stu-id="c6300-109">Note that the values 1-16 are reserved for use by Windows XP.</span></span> <span data-ttu-id="c6300-110">如果開發人員想要使用 [啟用內容參考](activation-context-reference.md)中所描述的函式來管理啟用內容，則可使用其他值。</span><span class="sxs-lookup"><span data-stu-id="c6300-110">A developer may use other values if they wish to manage the activation contexts using the functions describe in the [Activation Context Reference](activation-context-reference.md).</span></span>



| <span data-ttu-id="c6300-111">資訊清單 \_ 資源 \_ 識別碼的值</span><span class="sxs-lookup"><span data-stu-id="c6300-111">Value of MANIFEST\_RESOURCE\_ID</span></span> | <span data-ttu-id="c6300-112">資訊清單會指定進程預設值？</span><span class="sxs-lookup"><span data-stu-id="c6300-112">Manifest specifies the Process Default?</span></span> | <span data-ttu-id="c6300-113">用於靜態匯入？</span><span class="sxs-lookup"><span data-stu-id="c6300-113">Use for Static Imports?</span></span> | <span data-ttu-id="c6300-114">針對 EXE 使用嗎？</span><span class="sxs-lookup"><span data-stu-id="c6300-114">Use for an EXE?</span></span> | <span data-ttu-id="c6300-115">針對 DLL 使用嗎？</span><span class="sxs-lookup"><span data-stu-id="c6300-115">Use for a DLL?</span></span> | <span data-ttu-id="c6300-116">如果已啟用 DISOLATION 感知功能，則會使用並存版本的元件 \_ \_ ？</span><span class="sxs-lookup"><span data-stu-id="c6300-116">Uses Side-by-Side version of assemblies if compiled with -DISOLATION\_AWARE\_ENABLED?</span></span> |
|---------------------------------|-----------------------------------------|-------------------------|-----------------|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6300-117">1</span><span class="sxs-lookup"><span data-stu-id="c6300-117">1</span></span>                               | <span data-ttu-id="c6300-118">是</span><span class="sxs-lookup"><span data-stu-id="c6300-118">Yes</span></span>                                     | <span data-ttu-id="c6300-119">是</span><span class="sxs-lookup"><span data-stu-id="c6300-119">Yes</span></span>                     | <span data-ttu-id="c6300-120">是</span><span class="sxs-lookup"><span data-stu-id="c6300-120">Yes</span></span>             | <span data-ttu-id="c6300-121">否</span><span class="sxs-lookup"><span data-stu-id="c6300-121">No</span></span>             | <span data-ttu-id="c6300-122">是</span><span class="sxs-lookup"><span data-stu-id="c6300-122">Yes</span></span>                                                                                   |
| <span data-ttu-id="c6300-123">2</span><span class="sxs-lookup"><span data-stu-id="c6300-123">2</span></span>                               | <span data-ttu-id="c6300-124">否</span><span class="sxs-lookup"><span data-stu-id="c6300-124">No</span></span>                                      | <span data-ttu-id="c6300-125">是</span><span class="sxs-lookup"><span data-stu-id="c6300-125">Yes</span></span>                     | <span data-ttu-id="c6300-126">是</span><span class="sxs-lookup"><span data-stu-id="c6300-126">Yes</span></span>             | <span data-ttu-id="c6300-127">是</span><span class="sxs-lookup"><span data-stu-id="c6300-127">Yes</span></span>            | <span data-ttu-id="c6300-128">是</span><span class="sxs-lookup"><span data-stu-id="c6300-128">Yes</span></span>                                                                                   |
| <span data-ttu-id="c6300-129">3</span><span class="sxs-lookup"><span data-stu-id="c6300-129">3</span></span>                               | <span data-ttu-id="c6300-130">否</span><span class="sxs-lookup"><span data-stu-id="c6300-130">No</span></span>                                      | <span data-ttu-id="c6300-131">否</span><span class="sxs-lookup"><span data-stu-id="c6300-131">No</span></span>                      | <span data-ttu-id="c6300-132">是</span><span class="sxs-lookup"><span data-stu-id="c6300-132">Yes</span></span>             | <span data-ttu-id="c6300-133">是</span><span class="sxs-lookup"><span data-stu-id="c6300-133">Yes</span></span>            | <span data-ttu-id="c6300-134">是</span><span class="sxs-lookup"><span data-stu-id="c6300-134">Yes</span></span>                                                                                   |



 

<span data-ttu-id="c6300-135">資訊清單 \_ 資源 \_ 識別碼1應用於不裝載外掛程式的應用程式。\_ \_ 當應用程式的所有部分都應該使用資訊清單中指定的並存元件版本時，請使用資訊清單資源識別碼1。</span><span class="sxs-lookup"><span data-stu-id="c6300-135">MANIFEST\_RESOURCE\_ID 1 should be used for applications that do not host plug-ins. Use MANIFEST\_RESOURCE\_ID 1 when all parts of the application should use the version of the side-by-side assembly specified in the manifest.</span></span> <span data-ttu-id="c6300-136">如需詳細資訊，請參閱 [在不含擴充功能的應用程式中啟用元件](enabling-an-assembly-in-an-application-without-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="c6300-136">For more information, see [Enabling an Assembly in an Application Without Extensions](enabling-an-assembly-in-an-application-without-extensions.md).</span></span>

<span data-ttu-id="c6300-137">資訊清單 \_ 資源 \_ 識別碼2應用於裝載協力廠商控制項或外掛程式的應用程式。在此情況下，資訊清單會影響靜態載入所載入的所有並存元件、DllMain 的呼叫，以及已啟用 DISOLATION 感知的呼叫重新 \_ 導向 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c6300-137">MANIFEST\_RESOURCE\_ID 2 should be used for applications that host third-party controls or plug-ins. In this case, the manifest affects all side-by-side assemblies being loaded by static loading, calls to DllMain, and calls redirected by -DISOLATION\_AWARE\_ENABLED.</span></span> <span data-ttu-id="c6300-138">如需詳細資訊，請參閱 [在裝載 DLL、副檔名或主控台的應用程式中啟用元件](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md)。</span><span class="sxs-lookup"><span data-stu-id="c6300-138">For more information, see [Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span></span>

<span data-ttu-id="c6300-139">資訊清單 \_ 資源 \_ 識別碼3應用來重新導向 \_ \_ 僅限啟用 DISOLATION 感知的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c6300-139">MANIFEST\_RESOURCE\_ID 3 should be used for redirecting calls by -DISOLATION\_AWARE\_ENABLED only.</span></span> <span data-ttu-id="c6300-140">其他方法的載入不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="c6300-140">Loading by other methods are unaffected.</span></span>

 

 




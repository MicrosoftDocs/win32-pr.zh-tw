---
title: 使用 ADSI 擴充功能的優點
description: 擴充方法的執行方式視擴充功能寫入器而定。
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27e80e6c095fcc02ca02c57b0987d1e6ed410ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020809"
---
# <a name="benefits-of-using-adsi-extensions"></a><span data-ttu-id="782ea-103">使用 ADSI 擴充功能的優點</span><span class="sxs-lookup"><span data-stu-id="782ea-103">Benefits of Using ADSI Extensions</span></span>

<span data-ttu-id="782ea-104">擴充方法的執行方式視擴充功能寫入器而定。</span><span class="sxs-lookup"><span data-stu-id="782ea-104">The way in which extension methods are implemented depends on the extension writer.</span></span> <span data-ttu-id="782ea-105">延伸模組寫入器甚至可以完整地在目錄範圍之外執行方法。</span><span class="sxs-lookup"><span data-stu-id="782ea-105">An extension writer may even implement a method completely outside the scope of the directory.</span></span> <span data-ttu-id="782ea-106">例如，備份和還原軟體的開發人員計畫擴充稱為「 **電腦**」的物件。</span><span class="sxs-lookup"><span data-stu-id="782ea-106">For example, a developer of backup and restore software plans to extend an object called **computer**.</span></span> <span data-ttu-id="782ea-107">開發人員必須建立兩個方法： **備份** 和 **還原**。</span><span class="sxs-lookup"><span data-stu-id="782ea-107">The developer must create two methods: **BackUp** and **Restore**.</span></span> <span data-ttu-id="782ea-108">這些方法會從遠端在目錄中的 **電腦** 物件所指向的實體電腦上操作。</span><span class="sxs-lookup"><span data-stu-id="782ea-108">These methods operate remotely on the physical computer that the **computer** object in the directory points to.</span></span> <span data-ttu-id="782ea-109">藉由作為擴充功能，此元件會存取 ADSI 基礎結構，而且 ADSI 用戶端會將其視為物件的整數部分。</span><span class="sxs-lookup"><span data-stu-id="782ea-109">By acting as an extension, the component accesses the ADSI infrastructure and is viewed by ADSI clients as an integral part of the object.</span></span>

<span data-ttu-id="782ea-110">下列案例描述建立 ADSI 延伸模組的情況很有利：</span><span class="sxs-lookup"><span data-stu-id="782ea-110">The following scenarios describe situations where creating an extension to ADSI would be advantageous:</span></span>

-   <span data-ttu-id="782ea-111">建立延伸模組，以將元件與目錄物件整合。</span><span class="sxs-lookup"><span data-stu-id="782ea-111">Create an extension to integrate a component with the directory object.</span></span> <span data-ttu-id="782ea-112">因為目錄中有一個 **使用者** 物件，所以 HR 開發人員可能會想要建立 ADSI 擴充功能，以在建立 **使用者** 時填入目錄中的其他資料。</span><span class="sxs-lookup"><span data-stu-id="782ea-112">Because there is a **user** object in the directory, an HR developer may wish to create an ADSI extension that populates other data in the directory when a **user** is created.</span></span>
-   <span data-ttu-id="782ea-113">如果元件需要目錄查閱，請建立延伸模組。</span><span class="sxs-lookup"><span data-stu-id="782ea-113">Create an extension if a component requires a directory lookup.</span></span> <span data-ttu-id="782ea-114">元件可能需要目錄做為查閱的起點。</span><span class="sxs-lookup"><span data-stu-id="782ea-114">A component may require a directory as a starting point for a lookup.</span></span> <span data-ttu-id="782ea-115">例如，建立新的應用程式時。</span><span class="sxs-lookup"><span data-stu-id="782ea-115">For example, when creating a new application.</span></span> <span data-ttu-id="782ea-116">應用程式物件 **ToolApp** 可以在目錄中發行。</span><span class="sxs-lookup"><span data-stu-id="782ea-116">An application object, **ToolApp**, can be published in the directory.</span></span> <span data-ttu-id="782ea-117">您的應用程式可能會支援郵件伺服器集合上的狀態通知。</span><span class="sxs-lookup"><span data-stu-id="782ea-117">Your application may support status notifications on a collection of mail servers.</span></span> <span data-ttu-id="782ea-118">您決定將此應用程式設為 ADSI 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="782ea-118">You decide to make this application an ADSI extension.</span></span>

    <span data-ttu-id="782ea-119">現在，使用者可以在目錄中搜尋 **ToolApp** 的所有實例。</span><span class="sxs-lookup"><span data-stu-id="782ea-119">Now, a user may search for all instances of **ToolApp** in the directory.</span></span> <span data-ttu-id="782ea-120">針對傳回的每個物件，使用者可能會發出對 **NotifyNow ()** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="782ea-120">For each object returned, the user may issue a call to **NotifyNow()**.</span></span> <span data-ttu-id="782ea-121">應用程式或延伸模組可以在目錄中取得更多目前的物件資料，並以非同步方式通知每部伺服器。</span><span class="sxs-lookup"><span data-stu-id="782ea-121">An application or extension can obtain more current object data in the directory and notify each server asynchronously.</span></span>

-   <span data-ttu-id="782ea-122">建立擴充功能做為命名空間與程式設計模型之間的連接點。</span><span class="sxs-lookup"><span data-stu-id="782ea-122">Create an extension as a junction between namespaces and programming models.</span></span> <span data-ttu-id="782ea-123">例如，ISV invents 了列印服務的新物件模型。</span><span class="sxs-lookup"><span data-stu-id="782ea-123">For example, an ISV invents a new object model for print services.</span></span> <span data-ttu-id="782ea-124">目錄中已定義了 **列印佇列** 物件。</span><span class="sxs-lookup"><span data-stu-id="782ea-124">The **printQueue** object is already defined in the directory.</span></span> <span data-ttu-id="782ea-125">ISV 可以建立 ADSI 擴充功能，並將它與 **列印佇列** 物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="782ea-125">The ISV can create an ADSI extension and associate it with the **printQueue** object.</span></span> <span data-ttu-id="782ea-126">ADSI 使用者可以系結至 **列印佇列** 物件，並開始使用 ISV 的物件模型。</span><span class="sxs-lookup"><span data-stu-id="782ea-126">ADSI users can bind to a **printQueue** object and start using the object model for the ISV.</span></span> <span data-ttu-id="782ea-127">從 ADSI 用戶端的觀點來看，這個連接點是透明的。</span><span class="sxs-lookup"><span data-stu-id="782ea-127">From the ADSI client perspective, this junction point is transparent.</span></span>
-   <span data-ttu-id="782ea-128">建立延伸模組以簡化工作。</span><span class="sxs-lookup"><span data-stu-id="782ea-128">Create an extension to simplify tasks.</span></span> <span data-ttu-id="782ea-129">您可以藉由搜尋和設定物件或多個物件中的多個屬性，來完成目錄中的許多工。</span><span class="sxs-lookup"><span data-stu-id="782ea-129">Many tasks in the directory can be accomplished by searching and setting multiple attributes in an object or multiple objects.</span></span> <span data-ttu-id="782ea-130">藉由建立單一函式來操作多個屬性，它可簡化應用程式和腳本寫入器的開發工作。</span><span class="sxs-lookup"><span data-stu-id="782ea-130">By creating a single function to manipulate multiple attributes, it simplifies development for application and script writers.</span></span>

<span data-ttu-id="782ea-131">針對 ADSI 用戶端，擴充功能以數種方式擴充 ADSI 程式設計環境：</span><span class="sxs-lookup"><span data-stu-id="782ea-131">For ADSI clients, extensions enrich the ADSI programming environment in several ways:</span></span>

-   <span data-ttu-id="782ea-132">建立 ADSI 用戶端的開發人員不需要學習新的程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="782ea-132">Developers creating ADSI clients do not have to learn a new programming model.</span></span> <span data-ttu-id="782ea-133">延伸模組是 ADSI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="782ea-133">The extensions are part of ADSI.</span></span> <span data-ttu-id="782ea-134">它們會使用相同的架構來搜尋、資料操作以及保護物件的安全。</span><span class="sxs-lookup"><span data-stu-id="782ea-134">They would use the same paradigm for searching, data manipulation, and securing objects.</span></span>
-   <span data-ttu-id="782ea-135">系統管理員可以使用擴充功能來管理已啟用目錄的相關應用程式。</span><span class="sxs-lookup"><span data-stu-id="782ea-135">Administrators can manage related directory-enabled applications using extensions.</span></span>
-   <span data-ttu-id="782ea-136">擴充功能取用者可以將 ADSI 物件和延伸模組視為一個整合物件來查看。</span><span class="sxs-lookup"><span data-stu-id="782ea-136">Extension consumers can view an ADSI object and extension as one integrated object.</span></span>
-   <span data-ttu-id="782ea-137">現有的元件可以與 ADSI 整合，讓擴充功能得以利用現有的投資，並在元件之間建立協力功能。</span><span class="sxs-lookup"><span data-stu-id="782ea-137">Existing components may be integrated with ADSI, which enables extensions to leverage existing investments and create synergy between components.</span></span>

<span data-ttu-id="782ea-138">ADSI 擴充功能的設計具有下列目標：</span><span class="sxs-lookup"><span data-stu-id="782ea-138">ADSI extensions were designed with the following objectives:</span></span>

-   <span data-ttu-id="782ea-139">易於實行。</span><span class="sxs-lookup"><span data-stu-id="782ea-139">Easy to implement.</span></span> <span data-ttu-id="782ea-140">使用目前現有的 Microsoft 技術、Microsoft Visual C++ 開發系統，以及 Active Template Library，您可以快速建立擴充功能。</span><span class="sxs-lookup"><span data-stu-id="782ea-140">With the current existing Microsoft technologies, Microsoft Visual C++ development system, and the Active Template Library, an extension can be created quickly.</span></span>
-   <span data-ttu-id="782ea-141">用戶端會看到一個 IDispatch。</span><span class="sxs-lookup"><span data-stu-id="782ea-141">Clients view one IDispatch.</span></span> <span data-ttu-id="782ea-142">從腳本和自動化寫入器的觀點來看，擴充方法和屬性會以透明的方式混合成一個 ADSI 物件。</span><span class="sxs-lookup"><span data-stu-id="782ea-142">From the perspective of script and Automation writers, the extension methods and properties are transparently blended into one ADSI object.</span></span>
-   <span data-ttu-id="782ea-143">獨立。</span><span class="sxs-lookup"><span data-stu-id="782ea-143">Independent.</span></span> <span data-ttu-id="782ea-144">延伸模組寫入器可以獨立擴充 ADSI，而不需要事先瞭解現有的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="782ea-144">Extension writers can independently extend ADSI without prior knowledge of existing extensions.</span></span>

<span data-ttu-id="782ea-145">請考慮此案例：公司開發人員或 ISV 需要開發備份程式。</span><span class="sxs-lookup"><span data-stu-id="782ea-145">Consider this scenario: A corporate developer or an ISV needs to develop a backup program.</span></span> <span data-ttu-id="782ea-146">此備份應用程式可讓系統管理員備份組織單位中的所有電腦。</span><span class="sxs-lookup"><span data-stu-id="782ea-146">This backup application enables an administrator to back up all computers in an organizational unit.</span></span> <span data-ttu-id="782ea-147">使用 ADSI 擴充功能時，可以使用下列腳本。</span><span class="sxs-lookup"><span data-stu-id="782ea-147">With an ADSI extension, the following script is possible.</span></span>


```VB
Dim ou
On Error Resume Next
Set ou = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
If Err.Number<>0 Then
    MsgBox("An error has occurred.")
    Err.Clear
    Set ou = Nothing
    Exit Sub
End If

ou.Filter = Array("computer")

For each comp in ou
   Debug.Print comp.Get("networkAddress")
   Debug.Print comp.LastBackUp
   comp.BackUpNow
Next
```



<span data-ttu-id="782ea-148">**LastBackUp** 是一個屬性，而 **BackUpNow** 是延伸模組寫入器所提供的方法。</span><span class="sxs-lookup"><span data-stu-id="782ea-148">**LastBackUp** is a property and **BackUpNow** is a method that the extension writer provides.</span></span> <span data-ttu-id="782ea-149">此程式碼會顯示擴充取用者和提供者的優點。</span><span class="sxs-lookup"><span data-stu-id="782ea-149">The code shows the benefits for both extension consumers and providers.</span></span> <span data-ttu-id="782ea-150">延伸模組寫入器不需要建立新的方式來篩選、搜尋及存取目錄。</span><span class="sxs-lookup"><span data-stu-id="782ea-150">The extension writer does not have to create a new way of filtering, searching, and accessing the directory.</span></span> <span data-ttu-id="782ea-151">擴充取用者不需要破解新的程式設計範例。</span><span class="sxs-lookup"><span data-stu-id="782ea-151">The extension consumer does not have to relearn a new programming paradigm.</span></span> <span data-ttu-id="782ea-152">延伸模組寫入器所提供的新方法和屬性會視為 ADSI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="782ea-152">New methods and properties that the extension writer provides are viewed as part of ADSI.</span></span>

 

 





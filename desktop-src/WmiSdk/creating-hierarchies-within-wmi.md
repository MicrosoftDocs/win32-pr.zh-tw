---
description: WMI 命名空間是一種程式設計物件，可定義一組類別和實例的範圍。 WMI 提供者類別必須定義在命名空間內。
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: 在 WMI 內建立階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192204"
---
# <a name="creating-hierarchies-within-wmi"></a><span data-ttu-id="8de19-104">在 WMI 內建立階層</span><span class="sxs-lookup"><span data-stu-id="8de19-104">Creating Hierarchies Within WMI</span></span>

<span data-ttu-id="8de19-105">[*WMI 命名空間*](gloss-n.md) 是一種程式設計物件，可定義一組類別和實例的範圍。</span><span class="sxs-lookup"><span data-stu-id="8de19-105">[*WMI namespace*](gloss-n.md) is a programming object that defines the scope for a set of classes and instances.</span></span> <span data-ttu-id="8de19-106">WMI 提供者類別必須定義在命名空間內。</span><span class="sxs-lookup"><span data-stu-id="8de19-106">WMI provider classes must be defined inside a namespace.</span></span>

<span data-ttu-id="8de19-107">命名空間會描述不同的受控環境，例如 SMS 環境。</span><span class="sxs-lookup"><span data-stu-id="8de19-107">Namespaces describe different managed environments, such as the SMS environment.</span></span> <span data-ttu-id="8de19-108">由於架構的類別和實例會定義 managed 環境的元件，因此每個新的架構都需要新的命名空間。</span><span class="sxs-lookup"><span data-stu-id="8de19-108">Because the classes and instances of a schema define the components of a managed environment, each new schema requires a new namespace.</span></span> <span data-ttu-id="8de19-109">例如，根 \\ cimv2 命名空間包含 win32 架構中定義的類別和實例，以及 win32 架構所繼承 (CIM) 類別的父系通用訊息模型。</span><span class="sxs-lookup"><span data-stu-id="8de19-109">For example, the root\\cimv2 namespace contains the classes and instances defined in the Win32 schema as well as the parent Common Information Model (CIM) classes from which the Win32 schema inherits.</span></span> <span data-ttu-id="8de19-110">CIM 類別是由分散式管理工作強制 ([DMTF](https://www.dmtf.org/home)) 所定義。</span><span class="sxs-lookup"><span data-stu-id="8de19-110">CIM classes are defined by the Distributed Management Task Force ([DMTF](https://www.dmtf.org/home)).</span></span>

> [!Note]  
> <span data-ttu-id="8de19-111">若要確保在 WMI 發生失敗並重新啟動時，受管理物件的所有 WMI 類別定義都會還原至 [*wmi 儲存*](gloss-w.md)機制，請使用 [*受控物件格式 (MOF)*](gloss-m.md)檔中的 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器指令。</span><span class="sxs-lookup"><span data-stu-id="8de19-111">To ensure that all of your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format (MOF)*](gloss-m.md) file.</span></span>

 

<span data-ttu-id="8de19-112">WMI 會將命名空間定義為 [**\_ \_ 命名**](--namespace.md)空間系統類別的實例或衍生自 **\_ \_ 命名空間** 的任何類別。</span><span class="sxs-lookup"><span data-stu-id="8de19-112">WMI defines a namespace as an instance of the [**\_\_Namespace**](--namespace.md) system class or any class that derives from **\_\_Namespace**.</span></span> <span data-ttu-id="8de19-113">**\_ \_ 命名空間** 系統類別具有名為 **Name** 的單一屬性，這個屬性在父命名空間的範圍內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8de19-113">The **\_\_Namespace** system class has a single property called **Name**, which must be unique within the scope of the parent namespace.</span></span> <span data-ttu-id="8de19-114">**Name** 屬性也必須包含以字母開頭的字串。</span><span class="sxs-lookup"><span data-stu-id="8de19-114">The **Name** property must also contain a string that begins with a letter.</span></span> <span data-ttu-id="8de19-115">字串中的所有其他字元可以是字母、數位或底線。</span><span class="sxs-lookup"><span data-stu-id="8de19-115">All other characters in the string can be letters, digits, or underscores.</span></span> <span data-ttu-id="8de19-116">所有字元都不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8de19-116">All characters are case-insensitive.</span></span>

<span data-ttu-id="8de19-117">除了決定子命名空間的唯一名稱之外，父系 WMI 命名空間也可以保護您類別的靜態實例，防止其他提供者意外修改。</span><span class="sxs-lookup"><span data-stu-id="8de19-117">In addition to determining the unique name for a child namespace, the parent WMI namespace can protect the static instances of your classes from accidental modification by other providers.</span></span> <span data-ttu-id="8de19-118">例如，您可能會發現將新的命名空間嵌入另一個提供者的現有命名空間，是很方便的。</span><span class="sxs-lookup"><span data-stu-id="8de19-118">For example, you may find it convenient to nest a new namespace under an existing namespace for another provider.</span></span> <span data-ttu-id="8de19-119">不過，原始提供者可能會嘗試更新所有類別實例，以符合新的架構。</span><span class="sxs-lookup"><span data-stu-id="8de19-119">However, the original provider may try to update all class instances to match up with a new schema.</span></span> <span data-ttu-id="8de19-120">在這麼做的情況下，原始提供者可能會刪除命名空間中的所有子系子系。</span><span class="sxs-lookup"><span data-stu-id="8de19-120">In doing so, the original provider may delete all sub-children in a namespace.</span></span> <span data-ttu-id="8de19-121">雖然這可能是目標命名空間的適當動作，但它可能會影響子命名空間中不相關的類別實例 (例如，您自己的提供者類別) 。</span><span class="sxs-lookup"><span data-stu-id="8de19-121">While this may be an appropriate action for the target namespace, it may affect unrelated class instances in a child namespace (i.e., your own provider classes).</span></span>

<span data-ttu-id="8de19-122">因此，通常建議您建立命名空間，並將其註冊為與您未直接控制的命名空間不同的命名空間。</span><span class="sxs-lookup"><span data-stu-id="8de19-122">Therefore, it is generally recommended that you create and register your namespace as separate from namespaces that you do not directly control.</span></span> <span data-ttu-id="8de19-123">如果您的類別只衍生自您公司的一般 CIM 類別或其他類別，則更是如此。</span><span class="sxs-lookup"><span data-stu-id="8de19-123">This is especially true if your classes derive only from general CIM classes or other classes from your company.</span></span> <span data-ttu-id="8de19-124">您的命名空間可以在 **根** 命名空間底下，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8de19-124">Your namespace can be under the **Root** namespace, such as the following:</span></span>

<span data-ttu-id="8de19-125">**Root/myCompany/myProduct**</span><span class="sxs-lookup"><span data-stu-id="8de19-125">**Root/myCompany/myProduct**</span></span>

<span data-ttu-id="8de19-126">相反地，如果您的新類別衍生自另一個提供者的類別，您可能需要將您的類別儲存在該提供者的子命名空間中。</span><span class="sxs-lookup"><span data-stu-id="8de19-126">In contrast, if your new class derives from the class of another provider, you may need to store your class in a sub-namespace of that provider.</span></span> <span data-ttu-id="8de19-127">請注意，這會公開原始提供者意外刪除的新類別。</span><span class="sxs-lookup"><span data-stu-id="8de19-127">Note that this exposes your new class to accidental deletion by the original provider.</span></span>

<span data-ttu-id="8de19-128">WMI 提供數種不同的方式來建立命名空間：</span><span class="sxs-lookup"><span data-stu-id="8de19-128">WMI provides several different ways to create a namespace:</span></span>

-   [<span data-ttu-id="8de19-129">使用 MOF 程式碼建立子命名空間</span><span class="sxs-lookup"><span data-stu-id="8de19-129">Creating a Child Namespace with MOF Code</span></span>](creating-a-child-namespace-with-mof-code.md)
-   [<span data-ttu-id="8de19-130">使用 MOF 程式碼建立同級命名空間</span><span class="sxs-lookup"><span data-stu-id="8de19-130">Creating a Sibling Namespace with MOF Code</span></span>](creating-a-sibling-namespace-with-mof-code.md)
-   [<span data-ttu-id="8de19-131">使用 WMI API 建立命名空間</span><span class="sxs-lookup"><span data-stu-id="8de19-131">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a><span data-ttu-id="8de19-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="8de19-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8de19-133">設計受控物件格式 (MOF) 類別</span><span class="sxs-lookup"><span data-stu-id="8de19-133">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 




---
description: WMI 提供者是由受控物件格式 (MOF) 檔案和 DLL 檔案所組成。 MOF 檔案會定義提供者執行提供資料的類別。
ms.assetid: 20ef6b88-2aaa-4e86-bc4a-bebc34069672
ms.tgt_platform: multiple
title: 設計受控物件格式 (MOF) 類別
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 201f8c45f7a247fbca5695baa6dd440fc5dc323f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193645"
---
# <a name="designing-managed-object-format-mof-classes"></a><span data-ttu-id="747af-104">設計受控物件格式 (MOF) 類別</span><span class="sxs-lookup"><span data-stu-id="747af-104">Designing Managed Object Format (MOF) Classes</span></span>

<span data-ttu-id="747af-105">[*WMI 提供者*](gloss-p.md)是由受控物件格式 (MOF) 檔案和 DLL 檔案所組成。</span><span class="sxs-lookup"><span data-stu-id="747af-105">A [*WMI provider*](gloss-p.md) consists of a Managed Object Format (MOF) file and DLL file.</span></span> <span data-ttu-id="747af-106">MOF 檔案會定義提供者執行提供資料的類別。</span><span class="sxs-lookup"><span data-stu-id="747af-106">The MOF file defines the classes for which the provider implementation supplies data.</span></span>

<span data-ttu-id="747af-107">MOF 類別定義是由 [**mofcomp.exe**](mofcomp.md) 公用程式所編譯並儲存在 [*WMI 存放庫*](gloss-w.md)中，也稱為通用訊息模型 (CIM) 存放庫。</span><span class="sxs-lookup"><span data-stu-id="747af-107">The MOF class definitions are compiled by the [**mofcomp**](mofcomp.md) utility and stored in the [*WMI repository*](gloss-w.md), also known as the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="747af-108">建立類別的較常見方式是透過 [適用于 WMI 的 COM API](com-api-for-wmi.md)方法。</span><span class="sxs-lookup"><span data-stu-id="747af-108">A less common way to create classes is through the methods of the [COM API for WMI](com-api-for-wmi.md).</span></span>

> [!Note]  
> <span data-ttu-id="747af-109">若要確保在 WMI 發生失敗並重新啟動時，managed 物件的所有 WMI 類別定義都會還原至 [*wmi 儲存*](gloss-w.md)機制，請在您的 MOF 檔案中使用 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器指令。</span><span class="sxs-lookup"><span data-stu-id="747af-109">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your MOF file.</span></span>

 

<span data-ttu-id="747af-110">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="747af-110">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="747af-111">定義要管理的物件</span><span class="sxs-lookup"><span data-stu-id="747af-111">Defining the Objects to Manage</span></span>](#defining-the-objects-to-manage)
-   [<span data-ttu-id="747af-112">定義屬性或方法</span><span class="sxs-lookup"><span data-stu-id="747af-112">Defining Properties or Methods</span></span>](#defining-properties-or-methods)
-   [<span data-ttu-id="747af-113">彼此相關的物件</span><span class="sxs-lookup"><span data-stu-id="747af-113">Relating Objects to Each Other</span></span>](#relating-objects-to-each-other)
-   [<span data-ttu-id="747af-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="747af-114">Related topics</span></span>](#related-topics)

## <a name="defining-the-objects-to-manage"></a><span data-ttu-id="747af-115">定義要管理的物件</span><span class="sxs-lookup"><span data-stu-id="747af-115">Defining the Objects to Manage</span></span>

<span data-ttu-id="747af-116">在您識別要管理的企業部分之後，請定義要管理的物件。</span><span class="sxs-lookup"><span data-stu-id="747af-116">After you identify the part of your enterprise to manage, define the objects to manage.</span></span> <span data-ttu-id="747af-117">定義必須包含所需的資料，並可讓您精確地執行相關的商務規則。</span><span class="sxs-lookup"><span data-stu-id="747af-117">The definition must include the required data, and allow you to implement the relevant business rules accurately.</span></span> <span data-ttu-id="747af-118">您可以在更細微的層級定義物件，但最好是決定定義中所包含的詳細資料層級，而且需要提供足夠的詳細資料，才能發揮效用。</span><span class="sxs-lookup"><span data-stu-id="747af-118">You can define objects at a granular level, but it is best to decide between the level of detail contained in the definition, and the need to provide enough detail to be useful.</span></span> <span data-ttu-id="747af-119">程式初期的快捷方式可以節省時間，但未來可能會導致更多工作。</span><span class="sxs-lookup"><span data-stu-id="747af-119">Shortcuts early in the process may save time, but may be cause more work in the future.</span></span>

<span data-ttu-id="747af-120">分散式管理工作強制 (DMTF) 網站的 CIM 教學課程包含設計流程的絕佳資訊。</span><span class="sxs-lookup"><span data-stu-id="747af-120">The CIM Tutorial at the Distributed Management Task Force (DMTF) website contains excellent information about the design process.</span></span> <span data-ttu-id="747af-121">如需詳細資訊，請參閱 [www.dmtf.org](https://www.dmtf.org/)。</span><span class="sxs-lookup"><span data-stu-id="747af-121">For more information, see [www.dmtf.org](https://www.dmtf.org/).</span></span>

<span data-ttu-id="747af-122">當您開發和實行架構設計時，請考慮下列因素：</span><span class="sxs-lookup"><span data-stu-id="747af-122">Consider the following factors when you develop and implement a schema design:</span></span>

-   <span data-ttu-id="747af-123">限定詞</span><span class="sxs-lookup"><span data-stu-id="747af-123">Qualifiers</span></span>

    <span data-ttu-id="747af-124">限定詞提供如何描述類別、物件、屬性、方法和參數的相關資訊;而且它們會套用至類別和屬性定義。</span><span class="sxs-lookup"><span data-stu-id="747af-124">Qualifiers provide information about how to describe classes, objects, properties, methods, and parameters; and they are applied to class and property definitions.</span></span> <span data-ttu-id="747af-125">在 MOF 程式碼中，限定詞會以括弧括住，而且可能包含 \[ 金鑰 \] 或 \[ 關聯 \] 。</span><span class="sxs-lookup"><span data-stu-id="747af-125">In MOF code, qualifiers are enclosed in brackets and may include \[key\] or \[association\].</span></span> <span data-ttu-id="747af-126">如需詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md) 和 [WMI 限定詞](wmi-qualifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="747af-126">For more information, see [Adding a Qualifier](adding-a-qualifier.md) and [WMI Qualifiers](wmi-qualifiers.md).</span></span>

-   <span data-ttu-id="747af-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="747af-127">Namespace</span></span>

    <span data-ttu-id="747af-128">命名空間是用來分組類別和物件的邏輯單元，以及控制範圍和可見度。</span><span class="sxs-lookup"><span data-stu-id="747af-128">A namespace is a logical unit to group classes and objects, and control scope and visibility.</span></span> <span data-ttu-id="747af-129">一般而言，命名空間包含一組類別和物件，代表特定環境中的 managed 物件。</span><span class="sxs-lookup"><span data-stu-id="747af-129">Typically, a namespace contains a set of classes and objects that represent managed objects in a specific environment.</span></span> <span data-ttu-id="747af-130">如需詳細資訊，請參閱 [在 WMI 中建立](creating-hierarchies-within-wmi.md)階層。</span><span class="sxs-lookup"><span data-stu-id="747af-130">For more information, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

-   <span data-ttu-id="747af-131">Object</span><span class="sxs-lookup"><span data-stu-id="747af-131">Object</span></span>

    <span data-ttu-id="747af-132">模型化物件可能是架構的實體或邏輯元素。</span><span class="sxs-lookup"><span data-stu-id="747af-132">A modeled object might be a physical or logical element of the schema.</span></span> <span data-ttu-id="747af-133">例如，您可以建立實體磁片磁碟機（例如硬碟）或邏輯磁片（可以是實體磁片上的磁碟分割）的模型。</span><span class="sxs-lookup"><span data-stu-id="747af-133">For example, you can model a physical disk drive such as a hard disk drive, or a logical disk that can be a partition on a physical disk.</span></span> <span data-ttu-id="747af-134">使用類別來建立實體磁片磁碟機模型的設計，然後擴充該類別以建立邏輯磁片的模型，會比嘗試為每一種磁片類型建立個別類別的擴充性更容易擴充。</span><span class="sxs-lookup"><span data-stu-id="747af-134">A design that uses a class to model a physical disk drive, and then extends that class to model a logical disk is more extensible than one that attempts to create a separate class for each type of disk.</span></span>

-   <span data-ttu-id="747af-135">資料</span><span class="sxs-lookup"><span data-stu-id="747af-135">Data</span></span>

    <span data-ttu-id="747af-136">資料可能是動態或靜態的。</span><span class="sxs-lookup"><span data-stu-id="747af-136">Data may be dynamic or static.</span></span> <span data-ttu-id="747af-137">如果資料是動態的，您必須為它建立類別提供者。</span><span class="sxs-lookup"><span data-stu-id="747af-137">If the data is dynamic, you must create a class provider for it.</span></span>

    <span data-ttu-id="747af-138">若要讓使用者修改資料，您必須使用使用者所呼叫的方法，判斷您是否想要讓屬性只能直接寫入或修改。</span><span class="sxs-lookup"><span data-stu-id="747af-138">To enable the user to modify data, you must determine whether or not you want a property to be directly writable or modifiable only by using a method that the user calls.</span></span>

## <a name="defining-properties-or-methods"></a><span data-ttu-id="747af-139">定義屬性或方法</span><span class="sxs-lookup"><span data-stu-id="747af-139">Defining Properties or Methods</span></span>

<span data-ttu-id="747af-140">一般而言，WMI 類別屬性類似于 c + + 類別中的屬性。</span><span class="sxs-lookup"><span data-stu-id="747af-140">Generally, a WMI class property is similar to a property in a C++ class.</span></span> <span data-ttu-id="747af-141">如果您的程式碼針對資料所實行的唯一動作是取得值或設定值，則應該將資料定義為 WMI 類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="747af-141">If the only actions your code implements for the piece of data is to get the value or set the value, then the data should be defined as a property of the WMI class.</span></span>

<span data-ttu-id="747af-142">WMI 方法通常會執行動作來變更受管理物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="747af-142">A WMI method generally performs an action that changes the state of a managed object.</span></span> <span data-ttu-id="747af-143">例如，如果動作是要啟用或停用硬體物件的操作，則最好是建立讀取/寫入屬性的方法。</span><span class="sxs-lookup"><span data-stu-id="747af-143">For example, if the action is to enable or disable the operation of a hardware object, then a method is probably preferable to creating a read/write property.</span></span> <span data-ttu-id="747af-144">您也可以決定建立顯示硬體狀態的屬性。</span><span class="sxs-lookup"><span data-stu-id="747af-144">You may decide also to create a property that displays the state of the hardware.</span></span>

<span data-ttu-id="747af-145">當您建立類別或實例時，您可以加入批註。</span><span class="sxs-lookup"><span data-stu-id="747af-145">When you create a class or an instance, you can include comments.</span></span> <span data-ttu-id="747af-146">您可以使用這項技術來記錄您的類別，或說明程式設計技巧。</span><span class="sxs-lookup"><span data-stu-id="747af-146">Use this technique to document your class or explain your programming techniques.</span></span> <span data-ttu-id="747af-147">如需詳細資訊，請參閱 [建立批註](creating-a-comment.md)。</span><span class="sxs-lookup"><span data-stu-id="747af-147">For more information, see [Creating a Comment](creating-a-comment.md).</span></span> <span data-ttu-id="747af-148">此外，您可以加入資料來限定資料物件的用途。</span><span class="sxs-lookup"><span data-stu-id="747af-148">In addition, you can add data to qualify the purpose of a data object.</span></span> <span data-ttu-id="747af-149">如需詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md)。</span><span class="sxs-lookup"><span data-stu-id="747af-149">For more information, see [Adding a Qualifier](adding-a-qualifier.md).</span></span>

## <a name="relating-objects-to-each-other"></a><span data-ttu-id="747af-150">彼此相關的物件</span><span class="sxs-lookup"><span data-stu-id="747af-150">Relating Objects to Each Other</span></span>

<span data-ttu-id="747af-151">有兩種方式可以讓物件彼此產生關聯：藉由建立個別的物件，以及關聯的關聯物件，或在另一個物件中嵌入一個物件。</span><span class="sxs-lookup"><span data-stu-id="747af-151">There are two ways to relate objects to each other: by creating separate objects and an association object that relates them, or by embedding one object in the other.</span></span> <span data-ttu-id="747af-152">CIM 不支援内嵌物件，因此若要符合 CIM 規範，您必須使用第一個方法。</span><span class="sxs-lookup"><span data-stu-id="747af-152">CIM does not support embedded objects, so to be CIM-compliant you must use the first method.</span></span> <span data-ttu-id="747af-153">不過，WMI 支援內嵌物件，因此請使用這兩種方法來表示物件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="747af-153">However, WMI supports embedded objects so use either method to represent a relationship between objects.</span></span> <span data-ttu-id="747af-154">您可以在 [Win32 類別](/windows/desktop/CIMWin32Prov/win32-provider)中找到内嵌物件的範例。</span><span class="sxs-lookup"><span data-stu-id="747af-154">You can find examples of embedded objects in the [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider).</span></span> <span data-ttu-id="747af-155">例如， [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 具有内嵌物件 [**Win32 ACE，此 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)具有另一個内嵌物件（ [**win32 \_ 信任者**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)）。</span><span class="sxs-lookup"><span data-stu-id="747af-155">For example, [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) has the embedded object [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace), which has another embedded object, [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee).</span></span>

<span data-ttu-id="747af-156">在決定如何代表物件之間的關聯性時，請考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="747af-156">Consider the following when deciding how to represent relationships between objects:</span></span>

-   <span data-ttu-id="747af-157">如果實例很有用，則關聯最適合。</span><span class="sxs-lookup"><span data-stu-id="747af-157">If an instance is useful by itself, then an association works best.</span></span> <span data-ttu-id="747af-158">例如， [**win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 和 [**win32 \_ UserAccount**](/windows/desktop/CIMWin32Prov/win32-useraccount)。</span><span class="sxs-lookup"><span data-stu-id="747af-158">For example, [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) and [**Win32\_UserAccount**](/windows/desktop/CIMWin32Prov/win32-useraccount).</span></span> <span data-ttu-id="747af-159">如需詳細資訊，請參閱宣告 [關聯類別](declaring-an-association-class.md)。</span><span class="sxs-lookup"><span data-stu-id="747af-159">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>
-   <span data-ttu-id="747af-160">如果實例不存在父物件的外部，則内嵌物件的效果最佳。</span><span class="sxs-lookup"><span data-stu-id="747af-160">If an instance does not exist outside of the parent object, an embedded object works best.</span></span> <span data-ttu-id="747af-161">例如， [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 和 [**win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)。</span><span class="sxs-lookup"><span data-stu-id="747af-161">For example, [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) and [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span></span> <span data-ttu-id="747af-162">如需詳細資訊，請參閱 [在類別中内嵌物件](embedded-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="747af-162">For more information, see [Embedding Objects in a Class](embedded-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="747af-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="747af-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="747af-164">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="747af-164">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="747af-165">將資料提供給 WMI</span><span class="sxs-lookup"><span data-stu-id="747af-165">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> <dt>

[<span data-ttu-id="747af-166">MOF 資料類型</span><span class="sxs-lookup"><span data-stu-id="747af-166">MOF Data Types</span></span>](mof-data-types.md)
</dt> </dl>

 

 

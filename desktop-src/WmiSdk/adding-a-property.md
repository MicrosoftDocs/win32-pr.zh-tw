---
description: WMI 類別中的屬性會描述受管理物件的相關資料。
ms.assetid: 4046bfc7-9528-4737-ad61-bbb8419d0b51
ms.tgt_platform: multiple
title: 新增 WMI 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bba8944da155ca250edfed0c6e9160f555ba9551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996937"
---
# <a name="adding-a-wmi-property"></a><span data-ttu-id="7fd45-103">新增 WMI 屬性</span><span class="sxs-lookup"><span data-stu-id="7fd45-103">Adding a WMI Property</span></span>

<span data-ttu-id="7fd45-104">WMI 類別中的屬性會描述受管理物件的相關資料。</span><span class="sxs-lookup"><span data-stu-id="7fd45-104">Properties in WMI classes describe data about a managed object.</span></span> <span data-ttu-id="7fd45-105">例如， **Handle**、 **ProcessId** 和 **PageFaults** 會定義為 [**Win32 \_ process**](/windows/desktop/CIMWin32Prov/win32-process) 類別的屬性，並描述作業系統進程的各個層面。</span><span class="sxs-lookup"><span data-stu-id="7fd45-105">For example, **Handle**, **ProcessId**, and **PageFaults** are defined as properties of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class and describe aspects of an operating system process.</span></span> <span data-ttu-id="7fd45-106">如需詳細資訊，請參閱 [撰寫屬性提供者](writing-a-property-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="7fd45-106">For more information, see [Writing a Property Provider](writing-a-property-provider.md).</span></span>

## <a name="defining-a-property-in-mof"></a><span data-ttu-id="7fd45-107">在 MOF 中定義屬性</span><span class="sxs-lookup"><span data-stu-id="7fd45-107">Defining a Property in MOF</span></span>

<span data-ttu-id="7fd45-108">WMI 屬性代表物件中的外觀或狀態。</span><span class="sxs-lookup"><span data-stu-id="7fd45-108">A WMI property represents an aspect or state in the object.</span></span> <span data-ttu-id="7fd45-109">您可以建立屬性，而不是建立只取得和設定值的方法。</span><span class="sxs-lookup"><span data-stu-id="7fd45-109">Rather than create methods that simply get and set a value, you can create a property.</span></span> <span data-ttu-id="7fd45-110">例如， [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)的 **NetEnabled** 屬性會顯示是否已啟用或停用介面卡的狀態。</span><span class="sxs-lookup"><span data-stu-id="7fd45-110">For example, the **NetEnabled** property of [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) displays whether the state of the adapter is enabled or disabled.</span></span> <span data-ttu-id="7fd45-111">不過， [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) 和 [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) 方法實際上會執行變更介面卡狀態的動作。</span><span class="sxs-lookup"><span data-stu-id="7fd45-111">However, the [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) and [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) methods actually perform the action of changing the adapter state.</span></span>

<span data-ttu-id="7fd45-112">屬性必須具有資料類型。</span><span class="sxs-lookup"><span data-stu-id="7fd45-112">A property must have a data type.</span></span> <span data-ttu-id="7fd45-113">[**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)屬性 **控制碼** 的資料類型為 **字串**，而 **PageFaults** 的資料類型為 **uint32**。</span><span class="sxs-lookup"><span data-stu-id="7fd45-113">The data type of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) property **Handle** is **string** and the data type of **PageFaults** is **uint32**.</span></span> <span data-ttu-id="7fd45-114">如果屬性只能有兩個狀態，屬性的資料類型通常會設定為 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="7fd45-114">If a property can have only two states, the data type of the property is normally set to **boolean**.</span></span>

<span data-ttu-id="7fd45-115">屬性也可以是陣列。</span><span class="sxs-lookup"><span data-stu-id="7fd45-115">The property may also be an array.</span></span> <span data-ttu-id="7fd45-116">例如， [**Win32 \_ 信任者**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)的安全識別碼 (**SID**) 屬性是一個位元組陣列， (包含 SID 的 **uint8**) 。</span><span class="sxs-lookup"><span data-stu-id="7fd45-116">For example, the security identifier (**SID**) property of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) is a byte array (**uint8**) that contains the SID.</span></span> <span data-ttu-id="7fd45-117">屬性可以包含内嵌物件，這些物件是對另一個 WMI 類別的一個或多個實例的參考。</span><span class="sxs-lookup"><span data-stu-id="7fd45-117">Properties can contain embedded objects which are references to one or more instances of another WMI class.</span></span> <span data-ttu-id="7fd45-118">任意存取控制清單 **(DACL)** 和系統存取控制清單 **(SACL)** [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)的屬性，例如，會描述具有存取權的群組和帳戶的 [**win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 物件陣列。</span><span class="sxs-lookup"><span data-stu-id="7fd45-118">The discretionary access control list **(DACL)** and system access control list **(SACL)** properties of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), for example, are arrays of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) objects that describe the groups and accounts that have access.</span></span> <span data-ttu-id="7fd45-119">**Win32 \_ SecurityDescriptor** 中的 **群組** 屬性包含 **win32 \_ 受信任** 的單一實例的參考。</span><span class="sxs-lookup"><span data-stu-id="7fd45-119">The **Group** property in **Win32\_SecurityDescriptor** contains a reference to a single instance of **Win32\_Trustee**.</span></span> <span data-ttu-id="7fd45-120">如需詳細資訊，請參閱 [在類別中内嵌物件](embedded-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="7fd45-120">For more information, see [Embedding Objects in a Class](embedded-objects.md).</span></span>

<span data-ttu-id="7fd45-121">屬性可能有數個 [*限定詞*](gloss-q.md)。</span><span class="sxs-lookup"><span data-stu-id="7fd45-121">A property may have several [*qualifiers*](gloss-q.md).</span></span> <span data-ttu-id="7fd45-122">這些 [限定詞](wmi-qualifiers.md) 可 [*通用訊息模型 (CIM)*](gloss-c.md) 或 WMI 辨識符號，或可能是特定類型類別的特定類別，例如 [效能計數器](qualifiers-specific-to-wmi-performance-classes.md) 類別限定詞。</span><span class="sxs-lookup"><span data-stu-id="7fd45-122">These [qualifiers](wmi-qualifiers.md) may be [*Common Information Model (CIM)*](gloss-c.md) or WMI qualifiers or may be specific to certain types of classes, for example, the [performance Counter](qualifiers-specific-to-wmi-performance-classes.md) class qualifiers.</span></span> <span data-ttu-id="7fd45-123">限定詞會指定屬性的某些層面，例如，如果它是唯讀的，或是無法在沒有特定許可權的情況下變更。</span><span class="sxs-lookup"><span data-stu-id="7fd45-123">Qualifiers specify some aspect of the property, such as if it is read-only or if it cannot be changed without a specific privilege.</span></span> <span data-ttu-id="7fd45-124">例如，嘗試寫入 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)**DACL** 屬性的應用程式需要許可權 **SeSecurityPrivilege** 和 **SeRestorePrivilege**。</span><span class="sxs-lookup"><span data-stu-id="7fd45-124">An application which attempts to write to the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)**DACL** property, for example, requires the privileges **SeSecurityPrivilege** and **SeRestorePrivilege**.</span></span> <span data-ttu-id="7fd45-125">如需詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md)。</span><span class="sxs-lookup"><span data-stu-id="7fd45-125">For more information, see [Adding a Qualifier](adding-a-qualifier.md).</span></span>

<span data-ttu-id="7fd45-126">最後，屬性必須具有名稱。</span><span class="sxs-lookup"><span data-stu-id="7fd45-126">Finally, a property must have a name.</span></span> <span data-ttu-id="7fd45-127">您可以在標準程式設計實務的範圍內，將屬性命名為任何內容。</span><span class="sxs-lookup"><span data-stu-id="7fd45-127">You may name a property anything within the bounds of standard programming practice.</span></span> <span data-ttu-id="7fd45-128">不過，有兩個主要例外狀況。</span><span class="sxs-lookup"><span data-stu-id="7fd45-128">However, there are two main exceptions.</span></span> <span data-ttu-id="7fd45-129">首先，您不能使用任何 MOF 關鍵字（例如 "class"）作為屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="7fd45-129">First, you may not use any MOF keyword, such as "class", as a property name.</span></span> <span data-ttu-id="7fd45-130">其次，您可能不會使用任何 WQL 關鍵字（例如「群組」）作為屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="7fd45-130">Second, you may not use any WQL keywords, such as "group", as a property name either.</span></span> <span data-ttu-id="7fd45-131">如需 MOF 和 WQL 關鍵字的詳細資訊，請參閱適用于 WMI 的 [Mof 資料類型](mof-data-types.md) 和 [wql (SQL) ](wql-sql-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="7fd45-131">For more information on MOF and WQL keywords, see [MOF Data Types](mof-data-types.md) and [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span>

<span data-ttu-id="7fd45-132">針對 c + + 和受控物件格式 (MOF) 程式碼，您可以在宣告類別的同時宣告類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="7fd45-132">For both C++ and Managed Object Format (MOF) code, you declare the properties of a class at the same time that you declare the class.</span></span>

<span data-ttu-id="7fd45-133">**若要定義屬性**</span><span class="sxs-lookup"><span data-stu-id="7fd45-133">**To define a property**</span></span>

-   <span data-ttu-id="7fd45-134">在類別描述的大括弧之間，包含屬性資料類型、名稱，以及選擇性的預設值和限定詞。</span><span class="sxs-lookup"><span data-stu-id="7fd45-134">Include the property data type, name, and an optional default value and qualifier between the curly braces of the class description.</span></span>

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32         dwProp1 = 21;
        uint32         dwProp2;
    };
    ```

    <span data-ttu-id="7fd45-135">上述範例中的 MyClass 類別有三個屬性：字元字串、32位帶正負號的整數，以及32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="7fd45-135">The MyClass class in the preceding example has three properties: a character string, a 32-bit signed integer, and a 32-bit unsigned integer.</span></span> <span data-ttu-id="7fd45-136">每個屬性都會被指派不區分大小寫的名稱和 MOF 資料類型。</span><span class="sxs-lookup"><span data-stu-id="7fd45-136">Each property is assigned a case-insensitive name and a MOF data type.</span></span>

    <span data-ttu-id="7fd45-137">[**金鑰**](key-qualifier.md)辨識符號會將字串屬性定義為可唯一識別類別實例的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="7fd45-137">The [**Key**](key-qualifier.md) qualifier defines the string property as the key property that uniquely identifies an instance of the class.</span></span> <span data-ttu-id="7fd45-138">如需限定詞的詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md)。</span><span class="sxs-lookup"><span data-stu-id="7fd45-138">For more information about qualifiers, see [Adding a Qualifier](adding-a-qualifier.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fd45-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="7fd45-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fd45-140">建立類別</span><span class="sxs-lookup"><span data-stu-id="7fd45-140">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 

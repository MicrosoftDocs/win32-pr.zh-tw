---
description: Windows Management Instrumentation (WMI) 會定義一組與類別的所有類別和實例相關聯的系統屬性。
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: WMI 系統屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ee541d9de0d37c9aa1eae4ded07d3cb70ff1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192185"
---
# <a name="wmi-system-properties"></a><span data-ttu-id="84996-103">WMI 系統屬性</span><span class="sxs-lookup"><span data-stu-id="84996-103">WMI System Properties</span></span>

<span data-ttu-id="84996-104">Windows Management Instrumentation (WMI) 會定義一組與類別的所有類別和實例相關聯的系統屬性。</span><span class="sxs-lookup"><span data-stu-id="84996-104">Windows Management Instrumentation (WMI) defines a set of system properties that are associated with all classes and instances of classes.</span></span> <span data-ttu-id="84996-105">和系統類別一樣，系統屬性名稱會以雙底線開頭，與應用程式或提供者所建立的屬性區別，其不能以單一或雙底線開頭。</span><span class="sxs-lookup"><span data-stu-id="84996-105">As with system classes, system property names begin with a double underscore, distinguishing them from properties created by applications or providers that must not start with a single or double underscore.</span></span> <span data-ttu-id="84996-106">識別系統屬性的另一種方式是使用 [**IWbemClassObject：： Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) 方法。</span><span class="sxs-lookup"><span data-stu-id="84996-106">Another way to identify a system property is to use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="84996-107">系統屬性可以隨時使用，但值可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="84996-107">System properties are available at any time, but values might be **NULL**.</span></span> <span data-ttu-id="84996-108">**Null** 表示屬性不會套用至特定物件。</span><span class="sxs-lookup"><span data-stu-id="84996-108">**NULL** indicates a property does not apply to a specific object.</span></span> <span data-ttu-id="84996-109">不過，所有類別或實例的所有時間都可能無法使用系統屬性。</span><span class="sxs-lookup"><span data-stu-id="84996-109">However, system properties might not be available all the time for all classes or instances.</span></span>

## <a name="system-properties"></a><span data-ttu-id="84996-110">系統屬性</span><span class="sxs-lookup"><span data-stu-id="84996-110">System Properties</span></span>

<span data-ttu-id="84996-111">下列清單說明 WMI 系統屬性。</span><span class="sxs-lookup"><span data-stu-id="84996-111">The following list describes the WMI system properties.</span></span> <span data-ttu-id="84996-112">提供的範例取自 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) 類別的系統屬性，其描述于本主題的底部。</span><span class="sxs-lookup"><span data-stu-id="84996-112">The examples given are taken from the system properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which is described at the bottom of this topic.</span></span>

<dl> <dt>

<span data-ttu-id="84996-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_類**</span><span class="sxs-lookup"><span data-stu-id="84996-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Class**</span></span>
</dt> <dd>

<span data-ttu-id="84996-114">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="84996-114">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84996-115">存取類型：實例的唯讀;類別的讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84996-115">Access type: Read-only for instances; read/write for classes</span></span>

<span data-ttu-id="84996-116">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="84996-116">The name of the class.</span></span>

<span data-ttu-id="84996-117">範例： Win32 \_ OptionalFeature</span><span class="sxs-lookup"><span data-stu-id="84996-117">Example: Win32\_OptionalFeature</span></span>

</dd> <dt>

<span data-ttu-id="84996-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_推導**</span><span class="sxs-lookup"><span data-stu-id="84996-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivation**</span></span>
</dt> <dd>

<span data-ttu-id="84996-119">資料類型： **CIM \_ 字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="84996-119">Data type: **CIM\_STRING** array</span></span>

<span data-ttu-id="84996-120">存取類型：實例和類別的唯讀</span><span class="sxs-lookup"><span data-stu-id="84996-120">Access type: Read-only for both instances and classes</span></span>

<span data-ttu-id="84996-121">目前類別或實例的類別階層。</span><span class="sxs-lookup"><span data-stu-id="84996-121">Class hierarchy of the current class or instance.</span></span> <span data-ttu-id="84996-122">第一個元素是直屬父類別，下一個是其父系，依此類推。最後一個元素是基類。</span><span class="sxs-lookup"><span data-stu-id="84996-122">The first element is the immediate parent class, the next is its parent, and so on; the last element is the base class.</span></span>

<span data-ttu-id="84996-123">範例： {CIM \_ LogicalElement，cim \_ ManagedSystemElement}</span><span class="sxs-lookup"><span data-stu-id="84996-123">Example: {CIM\_LogicalElement, CIM\_ManagedSystemElement}</span></span>

</dd> <dt>

<span data-ttu-id="84996-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_代**</span><span class="sxs-lookup"><span data-stu-id="84996-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynasty**</span></span>
</dt> <dd>

<span data-ttu-id="84996-125">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="84996-125">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84996-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84996-126">Access type: Read-only</span></span>

<span data-ttu-id="84996-127">衍生類別或實例的最上層類別名稱。</span><span class="sxs-lookup"><span data-stu-id="84996-127">Name of the top-level class from which the class or instance is derived.</span></span> <span data-ttu-id="84996-128">當此類別或實例為最上層類別時， **\_ \_ 時代** 和 **\_ \_ 類別** 的值相同。</span><span class="sxs-lookup"><span data-stu-id="84996-128">When this class or instance is the top-level class, the values of **\_\_Dynasty** and **\_\_Class** are the same.</span></span>

<span data-ttu-id="84996-129">範例： CIM \_ ManagedSystemElement</span><span class="sxs-lookup"><span data-stu-id="84996-129">Example: CIM\_ManagedSystemElement</span></span>

</dd> <dt>

<span data-ttu-id="84996-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_屬**</span><span class="sxs-lookup"><span data-stu-id="84996-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genus**</span></span>
</dt> <dd>

<span data-ttu-id="84996-131">資料類型： **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="84996-131">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="84996-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84996-132">Access type: Read-only</span></span>

<span data-ttu-id="84996-133">用來區別類別和實例的值。</span><span class="sxs-lookup"><span data-stu-id="84996-133">Value that is used to distinguish between classes and instances.</span></span> <span data-ttu-id="84996-134">此值為類別 (1) 的 **wbem \_ 拼出動植物 \_ 類別** ，以及適用于實例和事件的 **wbem \_ 拼出動植物 \_ 實例** (2) 。</span><span class="sxs-lookup"><span data-stu-id="84996-134">This value is **WBEM\_GENUS\_CLASS** (1) for classes, and **WBEM\_GENUS\_INSTANCE** (2) for instances and events.</span></span>

<span data-ttu-id="84996-135">範例：2</span><span class="sxs-lookup"><span data-stu-id="84996-135">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="84996-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_命名 空間**](--namespace.md)</span><span class="sxs-lookup"><span data-stu-id="84996-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="84996-137">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="84996-137">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84996-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84996-138">Access type: Read-only</span></span>

<span data-ttu-id="84996-139">類別或實例的 [*命名空間*](gloss-n.md) 名稱。</span><span class="sxs-lookup"><span data-stu-id="84996-139">Name of the [*namespace*](gloss-n.md) of the class or instance.</span></span>

<span data-ttu-id="84996-140">範例：根 \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="84996-140">Example: root\\cimv2</span></span>

</dd> <dt>

<span data-ttu-id="84996-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_路徑**</span><span class="sxs-lookup"><span data-stu-id="84996-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Path**</span></span>
</dt> <dd>

<span data-ttu-id="84996-142">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="84996-142">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84996-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84996-143">Access type: Read-only</span></span>

<span data-ttu-id="84996-144">類別或實例的完整路徑，包括伺服器和命名空間。</span><span class="sxs-lookup"><span data-stu-id="84996-144">Full path to the class or instance—including server and namespace.</span></span>

<span data-ttu-id="84996-145">範例： \\ \\ MyServer \\ 根 \\ cimv2： Win32 \_ OptionalFeature。 Name = "TelnetClient"</span><span class="sxs-lookup"><span data-stu-id="84996-145">Example: \\\\MyServer\\root\\cimv2:Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="84996-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_屬性 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="84996-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Property\_Count**</span></span>
</dt> <dd>

<span data-ttu-id="84996-147">資料類型： **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="84996-147">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="84996-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84996-148">Access type: Read-only</span></span>

<span data-ttu-id="84996-149">為類別或實例定義的非系統屬性數目。</span><span class="sxs-lookup"><span data-stu-id="84996-149">Number of nonsystem properties defined for the class or instance.</span></span>

<span data-ttu-id="84996-150">範例: 6</span><span class="sxs-lookup"><span data-stu-id="84996-150">Example: 6</span></span>

</dd> <dt>

<span data-ttu-id="84996-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**</span><span class="sxs-lookup"><span data-stu-id="84996-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**</span></span>
</dt> <dd>

<span data-ttu-id="84996-152">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="84996-152">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84996-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84996-153">Access type: Read-only</span></span>

<span data-ttu-id="84996-154">類別或實例的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="84996-154">Relative path to the class or instance.</span></span>

<span data-ttu-id="84996-155">範例： Win32 \_ OptionalFeature. Name = "TelnetClient"</span><span class="sxs-lookup"><span data-stu-id="84996-155">Example: Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="84996-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_伺服器**</span><span class="sxs-lookup"><span data-stu-id="84996-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Server**</span></span>
</dt> <dd>

<span data-ttu-id="84996-157">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="84996-157">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84996-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84996-158">Access type: Read-only</span></span>

<span data-ttu-id="84996-159">提供類別或實例的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="84996-159">Name of the server supplying the class or instance.</span></span>

<span data-ttu-id="84996-160">範例： MyServer</span><span class="sxs-lookup"><span data-stu-id="84996-160">Example: MyServer</span></span>

</dd> <dt>

<span data-ttu-id="84996-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_超級**</span><span class="sxs-lookup"><span data-stu-id="84996-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclass**</span></span>
</dt> <dd>

<span data-ttu-id="84996-162">資料類型： **CIM \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="84996-162">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="84996-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84996-163">Access type: Read-only</span></span>

<span data-ttu-id="84996-164">類別或實例的直屬父類別名稱。</span><span class="sxs-lookup"><span data-stu-id="84996-164">Name of the immediate parent class of the class or instance.</span></span>

<span data-ttu-id="84996-165">範例： CIM \_ LogicalElement</span><span class="sxs-lookup"><span data-stu-id="84996-165">Example: CIM\_LogicalElement</span></span>

</dd> </dl>

<span data-ttu-id="84996-166">下列 PowerShell 程式碼會抓取 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) 類別的屬性，其中包括系統屬性。</span><span class="sxs-lookup"><span data-stu-id="84996-166">The following PowerShell code retrieves the properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which includes the system properties.</span></span>


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



<span data-ttu-id="84996-167">上述程式碼範例會傳回下列內容：</span><span class="sxs-lookup"><span data-stu-id="84996-167">The previous code sample returns the following:</span></span>


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 

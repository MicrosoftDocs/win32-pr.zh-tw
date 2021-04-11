---
description: 若要建立 WMI 方法，請定義方法的輸入和輸出參數。
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: 建立 WMI 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2489a5dd4e97ed6c8d26eeb292c45fa66901cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194709"
---
# <a name="creating-a-wmi-method"></a><span data-ttu-id="dafbb-103">建立 WMI 方法</span><span class="sxs-lookup"><span data-stu-id="dafbb-103">Creating a WMI Method</span></span>

<span data-ttu-id="dafbb-104">若要建立 WMI 方法，請定義方法的輸入和輸出參數。</span><span class="sxs-lookup"><span data-stu-id="dafbb-104">To create a WMI method, define the input and output parameters for the method.</span></span> <span data-ttu-id="dafbb-105">輸入和輸出參數是由特殊的 WMI 系統類別 [**\_ \_ 參數**](--parameters.md)表示。</span><span class="sxs-lookup"><span data-stu-id="dafbb-105">The input and output parameters are represented by a special WMI system class [**\_\_PARAMETERS**](--parameters.md).</span></span> <span data-ttu-id="dafbb-106">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md) 和 [撰寫方法提供者](writing-a-method-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="dafbb-106">For more information, see [Calling a Method](calling-a-method.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="dafbb-107">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="dafbb-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="dafbb-108">在 MOF 中建立 WMI 類別方法</span><span class="sxs-lookup"><span data-stu-id="dafbb-108">Creating a WMI Class Method in MOF</span></span>](#creating-a-wmi-class-method-in-mof)
-   [<span data-ttu-id="dafbb-109">在 c + + 中建立 WMI 類別方法</span><span class="sxs-lookup"><span data-stu-id="dafbb-109">Creating a WMI Class Method in C++</span></span>](#creating-a-wmi-class-method-in-c)
-   [<span data-ttu-id="dafbb-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="dafbb-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a><span data-ttu-id="dafbb-111">在 MOF 中建立 WMI 類別方法</span><span class="sxs-lookup"><span data-stu-id="dafbb-111">Creating a WMI Class Method in MOF</span></span>

<span data-ttu-id="dafbb-112">在 WMI 中，提供者方法通常是與類別所表示之物件相關的不同動作。</span><span class="sxs-lookup"><span data-stu-id="dafbb-112">In WMI, provider methods are generally distinct actions related to the object that the class represents.</span></span> <span data-ttu-id="dafbb-113">應該建立方法，而不是變更屬性的值來執行動作。</span><span class="sxs-lookup"><span data-stu-id="dafbb-113">Rather than change the value of a property to execute an action, a method should be created.</span></span> <span data-ttu-id="dafbb-114">例如，您可以使用 [**enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter)和 [**disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter)方法，啟用或停用 [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)所代表的網路資訊中心 (NIC) 。</span><span class="sxs-lookup"><span data-stu-id="dafbb-114">For example, you can enable or disable a network information center (NIC) that is represented by [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) by using the [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) and [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) methods.</span></span> <span data-ttu-id="dafbb-115">雖然這些動作可以表示為讀取/寫入屬性，但建議的設計是建立方法。</span><span class="sxs-lookup"><span data-stu-id="dafbb-115">While these actions can be represented as a read/write property, the recommended design is to create a method.</span></span> <span data-ttu-id="dafbb-116">或者，如果您想要讓類別能看到狀態或值，則建議的方法是建立讀取/寫入屬性，而不是方法。</span><span class="sxs-lookup"><span data-stu-id="dafbb-116">Alternatively, if you want to make a state or value visible for the class, then the recommended approach is to create a read/write property rather than a method.</span></span> <span data-ttu-id="dafbb-117">在 **Win32 \_ NetworkAdapter** 中， **NetEnabled** 屬性會讓介面卡的狀態成為可見的，但狀態之間的變更會由 **Enable** 或 **Disable** 方法執行。</span><span class="sxs-lookup"><span data-stu-id="dafbb-117">In **Win32\_NetworkAdapter**, the **NetEnabled** property makes the state of the adapter visible but changes between states are executed by the **Enable** or **Disable** methods.</span></span>

<span data-ttu-id="dafbb-118">類別宣告可以包含一或多個方法的宣告。</span><span class="sxs-lookup"><span data-stu-id="dafbb-118">Class declarations can include the declaration of one or more methods.</span></span> <span data-ttu-id="dafbb-119">您可以選擇繼承父類別的方法，或執行您自己的方法。</span><span class="sxs-lookup"><span data-stu-id="dafbb-119">You can either choose to inherit the methods of a parent class, or implement your own.</span></span> <span data-ttu-id="dafbb-120">如果您選擇執行自己的方法，您必須宣告方法，並使用特定的辨識符號標記來標記方法。</span><span class="sxs-lookup"><span data-stu-id="dafbb-120">If you choose to implement your own methods, you must declare the method and mark the method with specific qualifier tags.</span></span>

<span data-ttu-id="dafbb-121">下列程式描述如何在不繼承自基類的類別中宣告方法。</span><span class="sxs-lookup"><span data-stu-id="dafbb-121">The following procedure describes how to declare a method in a class that does not inherit from a base class.</span></span>

<span data-ttu-id="dafbb-122">**宣告方法**</span><span class="sxs-lookup"><span data-stu-id="dafbb-122">**To declare a method**</span></span>

1.  <span data-ttu-id="dafbb-123">在類別宣告的大括弧之間定義方法的名稱，後面加上任何限定詞。</span><span class="sxs-lookup"><span data-stu-id="dafbb-123">Define the name of your method between the curly braces of a class declaration, followed by any qualifiers.</span></span>

    <span data-ttu-id="dafbb-124">下列程式碼範例描述方法的語法。</span><span class="sxs-lookup"><span data-stu-id="dafbb-124">The following code example describes the syntax for a method.</span></span>

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  <span data-ttu-id="dafbb-125">完成之後，請呼叫 MOF 編譯器，將受控物件格式 (MOF) 程式碼插入 WMI 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="dafbb-125">When finished, insert your Managed Object Format (MOF) code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="dafbb-126">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="dafbb-126">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="dafbb-127">下列清單會定義方法宣告的元素。</span><span class="sxs-lookup"><span data-stu-id="dafbb-127">The following list defines the elements of the method declaration.</span></span>

<dl> <dt>

<span data-ttu-id="dafbb-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**供應商**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="dafbb-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dafbb-129">將特定提供者連結至您的類別描述。</span><span class="sxs-lookup"><span data-stu-id="dafbb-129">Links a specific provider to your class description.</span></span> <span data-ttu-id="dafbb-130">[**提供**](/windows/desktop/api/Provider/nl-provider-provider)者辨識符號的值是提供者的名稱，它會告知 WMI 支援您方法的程式碼所在位置。</span><span class="sxs-lookup"><span data-stu-id="dafbb-130">The value of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is the name of the provider, which tells WMI where the code that supports your method resides.</span></span> <span data-ttu-id="dafbb-131">提供者也應使用 **動態** 辨識符號來標記具有動態實例的任何類別。</span><span class="sxs-lookup"><span data-stu-id="dafbb-131">A provider should also mark with the **Dynamic** qualifier any class that has dynamic instances.</span></span> <span data-ttu-id="dafbb-132">相反地，請勿使用 **動態** 辨識符號來標記包含具有已 **執行** 方法之靜態實例的類別。</span><span class="sxs-lookup"><span data-stu-id="dafbb-132">In contrast, do not use the **Dynamic** qualifier to mark a class that contains a static instance with **Implemented** methods.</span></span>

</dd> <dt>

<span data-ttu-id="dafbb-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**實現**</span><span class="sxs-lookup"><span data-stu-id="dafbb-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="dafbb-134">宣告您將會執行方法，而不是從父類別繼承方法執行。</span><span class="sxs-lookup"><span data-stu-id="dafbb-134">Declares that you will implement a method, rather than inherit the method implementation from the parent class.</span></span> <span data-ttu-id="dafbb-135">根據預設，WMI 會將父類別的執行傳播至衍生類別，除非衍生的類別提供實值。</span><span class="sxs-lookup"><span data-stu-id="dafbb-135">By default, WMI propagates the implementation of the parent class to a derived class unless the derived class provides an implementation.</span></span> <span data-ttu-id="dafbb-136">省略實 **辨識符號表示** 方法在該類別中沒有任何實作為。</span><span class="sxs-lookup"><span data-stu-id="dafbb-136">Omitting the **Implemented** qualifier indicates that the method has no implementation in that class.</span></span> <span data-ttu-id="dafbb-137">如果您在沒有已實辨識 **符號的** 情況下重新宣告方法，WMI 仍會假設您不會執行該方法，並在呼叫時叫用父類別方法執行。</span><span class="sxs-lookup"><span data-stu-id="dafbb-137">If you redeclare a method without the **Implemented** qualifier, WMI still assumes that you are not going to implement that method, and invokes the parent class method implementation when called.</span></span> <span data-ttu-id="dafbb-138">因此，在衍生類別中重新宣告方法，但不附加已 **實限定詞，** 則只有在您于方法中加入或移除辨識符號時才有用。</span><span class="sxs-lookup"><span data-stu-id="dafbb-138">As such, redeclaring a method in a derived class without attaching the **Implemented** qualifier is useful only when you add or remove a qualifier to or from the method.</span></span>

</dd> <dt>

<span data-ttu-id="dafbb-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span><span class="sxs-lookup"><span data-stu-id="dafbb-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span></span>
</dt> <dd>

<span data-ttu-id="dafbb-140">說明方法傳回的值。</span><span class="sxs-lookup"><span data-stu-id="dafbb-140">Describes what value the method returns.</span></span> <span data-ttu-id="dafbb-141">方法的傳回值必須是布林值、數值、 **CHAR**、 **字串**、 [日期時間](datetime.md)或架構物件。</span><span class="sxs-lookup"><span data-stu-id="dafbb-141">The return value for a method must be a Boolean, numeric, **CHAR**, **STRING**, [DATETIME](datetime.md), or schema object.</span></span> <span data-ttu-id="dafbb-142">您也可以將傳回類型宣告為 [VOID](void.md)，表示該方法不會傳回任何內容。</span><span class="sxs-lookup"><span data-stu-id="dafbb-142">You can also declare the return type as [VOID](void.md), indicating that the method returns nothing.</span></span> <span data-ttu-id="dafbb-143">不過，您不能將陣列宣告為傳回值型別。</span><span class="sxs-lookup"><span data-stu-id="dafbb-143">However, you cannot declare an array as a return value type.</span></span>

</dd> <dt>

<span data-ttu-id="dafbb-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span><span class="sxs-lookup"><span data-stu-id="dafbb-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span></span>
</dt> <dd>

<span data-ttu-id="dafbb-145">定義方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="dafbb-145">Defines the name of the method.</span></span> <span data-ttu-id="dafbb-146">每個方法都必須有唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="dafbb-146">Every method must have a unique name.</span></span> <span data-ttu-id="dafbb-147">WMI 不允許在一個類別或類別階層中，有兩個相同名稱和不同簽章的方法存在。</span><span class="sxs-lookup"><span data-stu-id="dafbb-147">WMI does not allow two methods with the same name and different signatures to exist in one class or within a class hierarchy.</span></span> <span data-ttu-id="dafbb-148">因此，您也不能多載方法。</span><span class="sxs-lookup"><span data-stu-id="dafbb-148">As such, you also cannot overload a method.</span></span>

</dd> <dt>

<span data-ttu-id="dafbb-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span><span class="sxs-lookup"><span data-stu-id="dafbb-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span></span>
</dt> <dd>

<span data-ttu-id="dafbb-150">包含描述參數為輸入參數、輸出參數或兩者的限定詞。</span><span class="sxs-lookup"><span data-stu-id="dafbb-150">Contains qualifiers that describe if a parameter is an input parameter, output parameter, or both.</span></span> <span data-ttu-id="dafbb-151">請勿使用相同的參數名稱做為輸入參數，或使用一次以上作為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="dafbb-151">Do not use the same parameter name more than one time as an input parameter or more than one time as an output parameter.</span></span> <span data-ttu-id="dafbb-152">如果相同的參數名稱同時出現 [**在 in**](standard-qualifiers.md) 和 **out** 限定詞中，則此功能在概念上與在單一參數上使用 **in**、 **Out** 限定詞相同。</span><span class="sxs-lookup"><span data-stu-id="dafbb-152">If the same parameter name appears with both the [**In**](standard-qualifiers.md) and an **Out** qualifiers, the functionality is conceptually the same as using the **In**, **Out** qualifiers on a single parameter.</span></span> <span data-ttu-id="dafbb-153">不過，當使用不同的宣告時，輸入和輸出參數在其他所有方面都必須完全相同，包括 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號的數目和類型，而且限定詞必須相同且明確地針對兩者宣告。</span><span class="sxs-lookup"><span data-stu-id="dafbb-153">However, when using separate declarations, the input and output parameters must be exactly the same in all other respects, including the number and type of [**ID**](standard-wmi-qualifiers.md) qualifiers, and the qualifier must be the same and explicitly declared for both.</span></span> <span data-ttu-id="dafbb-154">強烈建議您在單一參數宣告中使用 **In**、 **Out** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="dafbb-154">It is strongly recommended to use the **In**, **Out** qualifiers within a single parameter declaration.</span></span>

</dd> <dt>

<span data-ttu-id="dafbb-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span><span class="sxs-lookup"><span data-stu-id="dafbb-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="dafbb-156">包含 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號，可唯一識別方法中參數序列內每個參數的位置。</span><span class="sxs-lookup"><span data-stu-id="dafbb-156">Contains the [**ID**](standard-wmi-qualifiers.md) qualifier that uniquely identifies the position of each parameter within the sequence of parameters in the method.</span></span> <span data-ttu-id="dafbb-157">根據預設，MOF 編譯器會自動以 **識別碼** 限定詞標記參數。</span><span class="sxs-lookup"><span data-stu-id="dafbb-157">By default, the MOF compiler automatically marks parameters with an **ID** qualifier.</span></span> <span data-ttu-id="dafbb-158">編譯器會標示值為 0 (零) 的第一個參數，第二個參數的值為 1 (一個) 等等。</span><span class="sxs-lookup"><span data-stu-id="dafbb-158">The compiler marks the first parameter with a value of 0 (zero), the second parameter a value of 1 (one), and so on.</span></span> <span data-ttu-id="dafbb-159">如有必要，您可以在 MOF 程式碼中明確陳述識別碼序列。</span><span class="sxs-lookup"><span data-stu-id="dafbb-159">If necessary, you can explicitly state the ID sequence in your MOF code.</span></span>

</dd> <dt>

<span data-ttu-id="dafbb-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span><span class="sxs-lookup"><span data-stu-id="dafbb-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span></span>
</dt> <dd>

<span data-ttu-id="dafbb-161">描述方法可接受的資料類型。</span><span class="sxs-lookup"><span data-stu-id="dafbb-161">Describes what data type the method can accept.</span></span> <span data-ttu-id="dafbb-162">您可以將參數類型定義為任何 MOF 資料值，包括陣列、架構物件或參考。</span><span class="sxs-lookup"><span data-stu-id="dafbb-162">You can define a parameter type as any MOF data value, including an array, schema object, or reference.</span></span> <span data-ttu-id="dafbb-163">使用陣列做為參數時，請使用陣列做為未系結或明確的大小。</span><span class="sxs-lookup"><span data-stu-id="dafbb-163">When using an array as a parameter, use the array as unbound or with an explicit size.</span></span>

</dd> <dt>

<span data-ttu-id="dafbb-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span><span class="sxs-lookup"><span data-stu-id="dafbb-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span></span>
</dt> <dd>

<span data-ttu-id="dafbb-165">包含參數的名稱。</span><span class="sxs-lookup"><span data-stu-id="dafbb-165">Contains the name of the parameter.</span></span> <span data-ttu-id="dafbb-166">您也可以選擇在此時定義參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="dafbb-166">You can also choose to define the default value of the parameter at this point.</span></span> <span data-ttu-id="dafbb-167">缺少初始值的參數會維持未指派狀態。</span><span class="sxs-lookup"><span data-stu-id="dafbb-167">Parameters lacking initial values remain unassigned.</span></span>

</dd> </dl>

<span data-ttu-id="dafbb-168">下列程式碼範例描述參數清單和限定詞。</span><span class="sxs-lookup"><span data-stu-id="dafbb-168">The following code example describes parameter listing and qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] sint32 InParam);
    [Implemented] 
    void MyMethod2 ([in, id(0)] sint32 InParam, 
       [out, id(1)] sint32 OutParam);
    [Implemented] 
    sint32 MyMethod3 ([in, out, id(0)] sint32 InOutParam);
};
```

<span data-ttu-id="dafbb-169">下列程式碼範例說明如何使用 MOF 參數中的陣列。</span><span class="sxs-lookup"><span data-stu-id="dafbb-169">The following code example describes how to use an array in a MOF parameter.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskParam[]);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskParam[32]);
};
```

<span data-ttu-id="dafbb-170">下列程式碼範例說明如何使用架構物件做為參數和傳回值。</span><span class="sxs-lookup"><span data-stu-id="dafbb-170">The following code example describes using a schema object as both a parameter and return value.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk 
        DiskParam);
    [Implemented] 
    Win32_LogicalDisk MyMethod2 ([in, id(0)] string DiskVolLabel);
};
```

<span data-ttu-id="dafbb-171">下列程式碼範例描述如何包含兩個參考：一個用於 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的實例，另一個則是未知物件類型的實例。</span><span class="sxs-lookup"><span data-stu-id="dafbb-171">The following code example describes how to include two references: one to an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and the other to an instance of an unknown object type.</span></span>

``` syntax
[Dynamic, Provider("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk ref DiskRef);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] object ref AnyObject);
};
```

## <a name="creating-a-wmi-class-method-in-c"></a><span data-ttu-id="dafbb-172">在 c + + 中建立 WMI 類別方法</span><span class="sxs-lookup"><span data-stu-id="dafbb-172">Creating a WMI Class Method in C++</span></span>

<span data-ttu-id="dafbb-173">下列程式描述如何以程式設計方式建立 WMI 類別方法。</span><span class="sxs-lookup"><span data-stu-id="dafbb-173">The following procedure describes how to create a WMI class method programmatically.</span></span>

<span data-ttu-id="dafbb-174">**以程式設計方式建立 WMI 類別方法**</span><span class="sxs-lookup"><span data-stu-id="dafbb-174">**To create a WMI class method programmatically**</span></span>

1.  <span data-ttu-id="dafbb-175">建立方法將所屬的類別。</span><span class="sxs-lookup"><span data-stu-id="dafbb-175">Create the class to which the method will belong.</span></span>

    <span data-ttu-id="dafbb-176">在建立方法之前，您必須先有一個可將方法放在其中的類別。</span><span class="sxs-lookup"><span data-stu-id="dafbb-176">You must first have a class to place the method in before you create the method.</span></span>

2.  <span data-ttu-id="dafbb-177">使用 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)或 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)，取出 [**\_ \_ PARAMETERS**](--parameters.md)系統類別的兩個子類別。</span><span class="sxs-lookup"><span data-stu-id="dafbb-177">Retrieve two child classes of the [**\_\_PARAMETERS**](--parameters.md) system class using either [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="dafbb-178">您可以使用第一個子類別來描述 in 參數，並使用第二個子類別來描述 out 參數。</span><span class="sxs-lookup"><span data-stu-id="dafbb-178">Use the first child class to describe the in-parameters, and the second to describe the out-parameters.</span></span> <span data-ttu-id="dafbb-179">如有必要，您可以執行單一抓取，然後呼叫 [**IWbemClassObject：： Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) 方法。</span><span class="sxs-lookup"><span data-stu-id="dafbb-179">If necessary, you can perform a single retrieval followed by a call to the [**IWbemClassObject::Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

3.  <span data-ttu-id="dafbb-180">使用一或多個 IWbemClassObject 呼叫，將 in 參數寫入第一個類別，並將 out 參數寫入至第二個類別 [**：:P 的內容**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)。</span><span class="sxs-lookup"><span data-stu-id="dafbb-180">Write the in-parameters to the first class, and the out-parameters to the second class, using one or more calls to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="dafbb-181">描述方法的參數時，請遵守下列規則和限制：</span><span class="sxs-lookup"><span data-stu-id="dafbb-181">When describing parameters to a method, observe the following rules and restrictions:</span></span>

    -   <span data-ttu-id="dafbb-182">將 \[ in、out \] 參數視為個別的專案，其中一個在包含 in 參數的物件中，另一個在包含 out 參數的物件中。</span><span class="sxs-lookup"><span data-stu-id="dafbb-182">Treat the \[in, out\] parameters as separate entries, one in the object that contains the in-parameters and one in the object that contains the out-parameters.</span></span>
    -   <span data-ttu-id="dafbb-183">除了 \[ in、out 限定詞之外 \] ，其餘的限定詞必須完全相同。</span><span class="sxs-lookup"><span data-stu-id="dafbb-183">Other than the \[in, out\] qualifiers, the remaining qualifiers must be exactly the same.</span></span>
    -   <span data-ttu-id="dafbb-184">指定 [**識別碼**](standard-wmi-qualifiers.md) 限定詞，從 0 (零) 開始，每個參數一個。</span><span class="sxs-lookup"><span data-stu-id="dafbb-184">Specify the [**ID**](standard-wmi-qualifiers.md) qualifiers, starting at 0 (zero), one for each parameter.</span></span>

        <span data-ttu-id="dafbb-185">輸入或輸出參數的順序，是由每個參數上的 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號值所建立。</span><span class="sxs-lookup"><span data-stu-id="dafbb-185">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="dafbb-186">所有輸入引數都必須在任何輸出引數之前。</span><span class="sxs-lookup"><span data-stu-id="dafbb-186">All input arguments must precede any output arguments.</span></span> <span data-ttu-id="dafbb-187">在更新現有的方法提供者時，變更方法輸入和輸出參數的順序，可能會導致呼叫方法的應用程式失敗。</span><span class="sxs-lookup"><span data-stu-id="dafbb-187">Changing the order of method input and output parameters when updating an existing method provider can cause applications that call the method to fail.</span></span> <span data-ttu-id="dafbb-188">在現有參數的結尾加入新的輸入參數，而不是以已經建立的順序來插入。</span><span class="sxs-lookup"><span data-stu-id="dafbb-188">Add new input parameters at the end of the existing parameters rather than inserting them in the sequence that is already established.</span></span>

        <span data-ttu-id="dafbb-189">請務必不要在 [**識別碼**](standard-wmi-qualifiers.md) 辨識符號序列中保留任何間距。</span><span class="sxs-lookup"><span data-stu-id="dafbb-189">Make sure to leave no gaps in the [**ID**](standard-wmi-qualifiers.md) qualifier sequence.</span></span>

    -   <span data-ttu-id="dafbb-190">將傳回值放在 out 參數類別中，作為名為 **ReturnValue** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="dafbb-190">Place the return value in the out-parameters class as a property named **ReturnValue**.</span></span>

        <span data-ttu-id="dafbb-191">這會將屬性識別為方法的傳回值。</span><span class="sxs-lookup"><span data-stu-id="dafbb-191">This identifies the property as the return value of the method.</span></span> <span data-ttu-id="dafbb-192">這個屬性的 CIM 型別是方法的傳回型別。</span><span class="sxs-lookup"><span data-stu-id="dafbb-192">The CIM type of this property is the return type of the method.</span></span> <span data-ttu-id="dafbb-193">如果方法的傳回型別為 void，則完全沒有 **ReturnValue** 屬性。</span><span class="sxs-lookup"><span data-stu-id="dafbb-193">If the method has a return type of void, then do not have a **ReturnValue** property at all.</span></span> <span data-ttu-id="dafbb-194">此外， **ReturnValue** 屬性不能有與方法的引數類似的 [**識別碼**](standard-wmi-qualifiers.md) 限定詞。</span><span class="sxs-lookup"><span data-stu-id="dafbb-194">Also, the **ReturnValue** property cannot have an [**ID**](standard-wmi-qualifiers.md) qualifier like the arguments of the method.</span></span> <span data-ttu-id="dafbb-195">將 **識別碼** 辨識符號指派給 **ReturnValue** 屬性會產生 WMI 錯誤。</span><span class="sxs-lookup"><span data-stu-id="dafbb-195">Assigning an **ID** qualifier to the **ReturnValue** property produces a WMI error.</span></span>

    -   <span data-ttu-id="dafbb-196">表示類別中屬性的任何預設參數值。</span><span class="sxs-lookup"><span data-stu-id="dafbb-196">Express any default parameter values for the property in the class.</span></span>

4.  <span data-ttu-id="dafbb-197">呼叫 [**IWbemClassObject：:P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)，將這兩個 [**\_ \_ 參數**](--parameters.md)物件放在父類別中。</span><span class="sxs-lookup"><span data-stu-id="dafbb-197">Place both [**\_\_PARAMETERS**](--parameters.md) objects into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

    <span data-ttu-id="dafbb-198">對 [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)的單一呼叫可以將這兩個 [**\_ \_ 參數**](--parameters.md)物件放入類別中。</span><span class="sxs-lookup"><span data-stu-id="dafbb-198">A single call to [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) can place both [**\_\_PARAMETERS**](--parameters.md) objects into the class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dafbb-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="dafbb-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dafbb-200">建立類別</span><span class="sxs-lookup"><span data-stu-id="dafbb-200">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 

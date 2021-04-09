---
description: 針對 WMI 提供者建立新 WMI 基類的建議方式，是在受控物件格式 (MOF) 檔中。
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: 建立 WMI 基類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdcbe6995a7782d854a4d0950db841f23a30b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945113"
---
# <a name="creating-a-wmi-base-class"></a><span data-ttu-id="9b4b8-103">建立 WMI 基類</span><span class="sxs-lookup"><span data-stu-id="9b4b8-103">Creating a WMI Base Class</span></span>

<span data-ttu-id="9b4b8-104">針對 WMI 提供者建立新 WMI 基類的建議方式，是在受控物件格式 (MOF) 檔中。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-104">The recommended way to create a new WMI base class for a WMI provider is in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="9b4b8-105">您也可以使用 [適用于 WMI 的 COM API 來](com-api-for-wmi.md)建立基類。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-105">You can also create a base class using the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="9b4b8-106">雖然您可以在腳本中建立基底或衍生類別，但沒有提供資料給類別及其子類別的提供者，但類別並不實用。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-106">While you can create a base or derived class in script, without a provider supplying data to the class and its subclasses, the class is not useful.</span></span>

<span data-ttu-id="9b4b8-107">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="9b4b8-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="9b4b8-108">使用 MOF 建立基類</span><span class="sxs-lookup"><span data-stu-id="9b4b8-108">Creating a Base Class Using MOF</span></span>](#creating-a-base-class-using-mof)
-   [<span data-ttu-id="9b4b8-109">使用 c + + 建立基類</span><span class="sxs-lookup"><span data-stu-id="9b4b8-109">Creating a Base Class with C++</span></span>](#creating-a-base-class-with-c)
-   [<span data-ttu-id="9b4b8-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b4b8-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-base-class-using-mof"></a><span data-ttu-id="9b4b8-111">使用 MOF 建立基類</span><span class="sxs-lookup"><span data-stu-id="9b4b8-111">Creating a Base Class Using MOF</span></span>

<span data-ttu-id="9b4b8-112">WMI 類別通常依賴繼承。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-112">WMI classes usually rely on inheritance.</span></span> <span data-ttu-id="9b4b8-113">在建立基類之前，請先檢查通用訊息模型 (可從分散式管理工作強制執行的 CIM) 類別 ([ [DMTF](https://www.dmtf.org/) ]) 。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-113">Before creating a base class, check the Common Information Model (CIM) classes available from the Distributed Management Task Force ([DMTF](https://www.dmtf.org/)).</span></span>

<span data-ttu-id="9b4b8-114">如果有許多衍生類別會使用相同的屬性，請將這些屬性和方法放在基類中。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-114">If many derived classes will use the same properties, put these properties and methods in your base class.</span></span> <span data-ttu-id="9b4b8-115">您可以在 WMI 類別中定義的最大屬性數目是1024。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-115">The maximum number of properties you can define in a WMI class is 1024.</span></span>

<span data-ttu-id="9b4b8-116">建立基類時，請觀察下列類別名稱的方針清單：</span><span class="sxs-lookup"><span data-stu-id="9b4b8-116">When creating a base class, observe the following list of guidelines for class names:</span></span>

-   <span data-ttu-id="9b4b8-117">使用大寫和小寫字母。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-117">Use both uppercase and lowercase letters.</span></span>
-   <span data-ttu-id="9b4b8-118">以字母開頭的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-118">Begin a class name with a letter.</span></span>
-   <span data-ttu-id="9b4b8-119">請勿使用開頭或尾端的底線。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-119">Do not use either a leading or trailing underscore.</span></span>
-   <span data-ttu-id="9b4b8-120">將所有剩餘的字元定義為字母、數位或底線。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-120">Define all remaining characters as letters, digits, or underscores.</span></span>
-   <span data-ttu-id="9b4b8-121">使用一致的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-121">Use a consistent naming convention.</span></span>

    <span data-ttu-id="9b4b8-122">雖然並非必要，但類別的良好命名慣例是以底線聯結的兩個元件。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-122">While not necessary, a good naming convention for a class is two components joined by an underscore.</span></span> <span data-ttu-id="9b4b8-123">有可能的話，廠商名稱應該構成名稱的前半部分，而描述性的類別名稱應該是第二個部分。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-123">When possible, a vendor name should make up the first half of the name, and a descriptive class name should be the second part.</span></span>

> [!Note]  
> <span data-ttu-id="9b4b8-124">在執行提供者期間，無法變更類別。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-124">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="9b4b8-125">您必須停止活動、變更類別，然後重新開機 Windows 管理服務。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-125">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="9b4b8-126">目前無法偵測類別變更。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-126">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="9b4b8-127">在 MOF 中，藉由使用 **class** 關鍵字命名來建立基類，但不表示父類別。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-127">In MOF, create a base class by naming it with the **class** keyword, but not indicating a parent class.</span></span>

<span data-ttu-id="9b4b8-128">**使用 MOF 程式碼建立基類**</span><span class="sxs-lookup"><span data-stu-id="9b4b8-128">**To create a base class using MOF code**</span></span>

1.  <span data-ttu-id="9b4b8-129">使用 **類別** 關鍵字搭配新類別的名稱，後面加上一對大括弧和分號。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-129">Use the **class** keyword with the name of the new class, followed by a pair of curly braces and a semicolon.</span></span> <span data-ttu-id="9b4b8-130">在大括弧之間加入類別的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-130">Add properties and methods for the class between the curly braces.</span></span> <span data-ttu-id="9b4b8-131">提供的程式碼範例如下。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-131">The following code example is provided.</span></span>

    <span data-ttu-id="9b4b8-132">下列程式碼範例顯示如何定義基類。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-132">The following code example shows how a base class should be defined.</span></span>

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    <span data-ttu-id="9b4b8-133">下列程式碼範例顯示基類的定義不正確。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-133">The following code example shows an incorrect definition of a base class.</span></span>

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  <span data-ttu-id="9b4b8-134">在 class 關鍵字之前加入任何類別 [*限定詞*](gloss-q.md) ，以修改類別的使用方式。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-134">Add any class [*qualifiers*](gloss-q.md) before the class keyword to modify the way the class is used.</span></span> <span data-ttu-id="9b4b8-135">在方括弧之間放置限定詞。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-135">Place the qualifiers between square brackets.</span></span> <span data-ttu-id="9b4b8-136">如需修改類別之限定詞的詳細資訊，請參閱 [WMI 限定詞](wmi-qualifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-136">For more information about qualifiers for modifying classes, see [WMI Qualifiers](wmi-qualifiers.md).</span></span> <span data-ttu-id="9b4b8-137">使用 **抽象** 限定詞表示您無法直接建立此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-137">Use the **Abstract** qualifier to indicate that you cannot create an instance of this class directly.</span></span> <span data-ttu-id="9b4b8-138">抽象類別通常用來定義數個衍生類別將使用的屬性或方法。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-138">Abstract classes are often used to define properties or methods that will be used by several derived classes.</span></span> <span data-ttu-id="9b4b8-139">如需詳細資訊，請參閱 [建立衍生類別](creating-a-derived-class.md)。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-139">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

    <span data-ttu-id="9b4b8-140">下列程式碼範例會將類別定義為抽象，並定義將提供資料的提供者。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-140">The following code example defines the class as abstract and defines the provider that will supply the data.</span></span> <span data-ttu-id="9b4b8-141">**ToSubClass** 限定詞類別表示 **提供者**[*辨識符號中*](gloss-f.md)的資訊是由衍生類別繼承。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-141">The **ToSubClass** qualifier [*flavor*](gloss-f.md) indicates that the information in the **Provider** qualifier is inherited by derived classes.</span></span>

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  <span data-ttu-id="9b4b8-142">將類別的屬性和方法加入至屬性或方法名稱之前的方括弧內。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-142">Add the properties and methods for the class inside square brackets before the property or method name.</span></span> <span data-ttu-id="9b4b8-143">如需詳細資訊，請參閱 [新增屬性](adding-a-property.md) 和 [建立方法](creating-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-143">For more information, see [Adding a Property](adding-a-property.md) and [Creating a Method](creating-a-method.md).</span></span> <span data-ttu-id="9b4b8-144">您可以使用 MOF 限定詞來修改這些屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-144">You can modify these properties and methods using MOF qualifiers.</span></span> <span data-ttu-id="9b4b8-145">如需詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md)。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-145">For more information, see [Adding a Qualifier](adding-a-qualifier.md).</span></span>

    <span data-ttu-id="9b4b8-146">下列程式碼範例示範如何使用 MOF 限定詞來修改屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-146">The following code example shows how to modify properties and methods with MOF qualifiers.</span></span>

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  <span data-ttu-id="9b4b8-147">以 mof 副檔名儲存 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-147">Save the MOF file with an extension of .mof.</span></span>
5.  <span data-ttu-id="9b4b8-148">藉由在檔案上執行 [**Mofcomp.exe**](mofcomp.md) ，向 WMI 註冊類別。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-148">Register the class with WMI by running [**Mofcomp.exe**](mofcomp.md) on the file.</span></span>

    <span data-ttu-id="9b4b8-149">**mofcomp.exe** *newmof mof*</span><span class="sxs-lookup"><span data-stu-id="9b4b8-149">**mofcomp.exe** *newmof.mof*</span></span>

    <span data-ttu-id="9b4b8-150">如果您未使用 **-N** 參數或預處理器命令 \# [**pragma 命名**](pragma-namespace.md)空間來指定命名空間，則編譯的 MOF 類別將會儲存在存放庫的根 \\ 預設命名空間中。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-150">If you do not use the **-N** switch or the preprocessor command \#[**pragma namespace**](pragma-namespace.md) to specify a namespace, the compiled MOF classes will be stored in the root\\default namespace in the repository.</span></span> <span data-ttu-id="9b4b8-151">如需詳細資訊，請參閱 [**mofcomp.exe**](mofcomp.md)。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-151">For more information, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="9b4b8-152">下列程式碼範例結合了先前程式中討論的 MOF 程式碼範例，並說明如何 \\ 使用 MOF 在根 cimv2 命名空間中建立基類。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-152">The following code example combines the MOF code examples discussed in the previous procedure and shows how to create a base class in the root\\cimv2 namespace using MOF.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

<span data-ttu-id="9b4b8-153">如需詳細資訊，請參閱 [建立衍生類別](creating-a-derived-class.md) 以取得衍生自這個基類的動態類別範例。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-153">For more information, see [Creating a Derived Class](creating-a-derived-class.md) for an example of a dynamic class derived from this base class.</span></span>

## <a name="creating-a-base-class-with-c"></a><span data-ttu-id="9b4b8-154">使用 c + + 建立基類</span><span class="sxs-lookup"><span data-stu-id="9b4b8-154">Creating a Base Class with C++</span></span>

<span data-ttu-id="9b4b8-155">使用 WMI API 建立基類主要是一系列的 Put 命令，其定義類別並向 WMI 註冊類別。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-155">Creating a base class using the WMI API is mainly a series of Put commands that define the class and register the class with WMI.</span></span> <span data-ttu-id="9b4b8-156">此 API 的主要目的是要讓用戶端應用程式建立基類。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-156">The main purpose of this API is to enable client applications to create base classes.</span></span> <span data-ttu-id="9b4b8-157">不過，您也可以讓提供者使用此 API 來建立基類。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-157">However, you can also have a provider use this API to create a base class.</span></span> <span data-ttu-id="9b4b8-158">例如，如果您認為提供者的 MOF 程式碼將無法正確安裝，您可以指示您的提供者在 WMI 儲存機制中自動建立正確的類別。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-158">For example, if you believe that the MOF code for your provider will not be installed properly, you can instruct your provider to automatically create the correct classes in the WMI repository.</span></span> <span data-ttu-id="9b4b8-159">如需提供者的詳細資訊，請參閱 [撰寫類別提供者](writing-a-class-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-159">For more information about providers, see [Writing a Class Provider](writing-a-class-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="9b4b8-160">在執行提供者期間，無法變更類別。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-160">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="9b4b8-161">您必須停止活動、變更類別，然後重新開機 Windows 管理服務。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-161">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="9b4b8-162">目前無法偵測類別變更。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-162">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="9b4b8-163">程式碼需要下列參考才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-163">The code requires the following reference to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="9b4b8-164">您可以使用 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立新的基類。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-164">You can create a new base class programmatically using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="9b4b8-165">**使用 WMI API 建立新的基類**</span><span class="sxs-lookup"><span data-stu-id="9b4b8-165">**To create a new base class with the WMI API**</span></span>

1.  <span data-ttu-id="9b4b8-166">藉由呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 方法，並將 *strObjectPath* 參數設定為 **null** 值，以抓取新類別的定義。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-166">Retrieve a definition for the new class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method with the *strObjectPath* parameter set to a **null** value.</span></span>

    <span data-ttu-id="9b4b8-167">下列程式碼範例示範如何取出新類別的定義。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-167">The following code example shows how to retrieve a definition for a new class.</span></span>

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  <span data-ttu-id="9b4b8-168">藉由設定 **\_ \_ 類別** 系統屬性並呼叫 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)的 ui 方法，來建立類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-168">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="9b4b8-169">下列程式碼範例顯示如何藉由設定 **\_ \_ 類別** 系統屬性來命名類別。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-169">The following code example shows how to name the class by setting the **\_\_CLASS** system property.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  <span data-ttu-id="9b4b8-170">藉由呼叫 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)]，以建立索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-170">Create the key property or properties by calling [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="9b4b8-171">下列程式碼範例說明如何建立索引屬性，該屬性在步驟4中標示為 [**索引**](swbemrefreshableitem-index.md) 鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-171">The following code example describes how to create the [**Index**](swbemrefreshableitem-index.md) property, which is labeled as a key property in Step 4.</span></span>

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  <span data-ttu-id="9b4b8-172">先呼叫 [**IWbemClassObject：： GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset)方法，然後呼叫 [**IWbemQualifierSet：:P**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put)的 ui 方法，以將 [**金鑰**](standard-qualifiers.md)標準限定詞附加至索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-172">Attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property by first calling the [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) method and then the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="9b4b8-173">下列程式碼範例示範如何將 [**金鑰**](standard-qualifiers.md) 標準限定詞附加至索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-173">The following code example shows how to attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property.</span></span>

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  <span data-ttu-id="9b4b8-174">使用 [**IWbemClassObject：:P 的內容**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)，建立類別的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-174">Create other properties of the class with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="9b4b8-175">下列程式碼範例說明如何建立其他屬性。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-175">The following code example describes how to create additional properties.</span></span>

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  <span data-ttu-id="9b4b8-176">藉由呼叫 [**IWbemServices：:P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)來註冊新的類別。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-176">Register the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="9b4b8-177">因為您無法在註冊新類別之後定義索引鍵和索引，所以在呼叫 [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)之前，請確定您已定義所有屬性。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-177">Because you cannot define keys and indices after you register a new class, ensure that you have defined all of your properties before calling [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="9b4b8-178">下列程式碼範例說明如何註冊新的類別。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-178">The following code example describes how to register a new class.</span></span>

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

<span data-ttu-id="9b4b8-179">下列程式碼範例結合了先前程式中所討論的程式碼範例，並說明如何使用 WMI API 建立基類。</span><span class="sxs-lookup"><span data-stu-id="9b4b8-179">The following code example combines the code examples discussed in the previous procedure and shows how to create a base class using the WMI API.</span></span>


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="9b4b8-180">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b4b8-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b4b8-181">建立類別</span><span class="sxs-lookup"><span data-stu-id="9b4b8-181">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 




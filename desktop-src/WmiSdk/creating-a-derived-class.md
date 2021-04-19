---
description: 在 WMI 中建立衍生類別非常類似于建立基類。 如同基類，您必須先定義衍生類別，然後向 WMI 註冊衍生類別。
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: 建立 WMI 衍生類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b65079d206cb7a0a490622018f6d2e2df98867d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977848"
---
# <a name="creating-a-wmi-derived-class"></a><span data-ttu-id="72474-104">建立 WMI 衍生類別</span><span class="sxs-lookup"><span data-stu-id="72474-104">Creating a WMI Derived Class</span></span>

<span data-ttu-id="72474-105">在 WMI 中建立衍生類別非常類似于建立基類。</span><span class="sxs-lookup"><span data-stu-id="72474-105">Creating a derived class in WMI is very similar to creating a base class.</span></span> <span data-ttu-id="72474-106">如同基類，您必須先定義衍生類別，然後向 WMI 註冊衍生類別。</span><span class="sxs-lookup"><span data-stu-id="72474-106">As with a base class, you must first define the derived class and then register the derived class with WMI.</span></span> <span data-ttu-id="72474-107">主要的差異在於，您必須先找出您想要從中衍生的父類別。</span><span class="sxs-lookup"><span data-stu-id="72474-107">The main difference is that you must first locate the parent class from which you wish to derive.</span></span> <span data-ttu-id="72474-108">如需詳細資訊，請參閱 [撰寫類別提供者](writing-a-class-provider.md) 和 [撰寫執行個體提供者](writing-an-instance-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="72474-108">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>

<span data-ttu-id="72474-109">為提供者建立類別的建議方式是在受控物件格式 (MOF) 檔案中。</span><span class="sxs-lookup"><span data-stu-id="72474-109">The recommended way to create classes for a provider is in Managed Object Format (MOF) files.</span></span> <span data-ttu-id="72474-110">數個彼此相關的衍生類別應群組為 MOF 檔案，以及它們從中衍生屬性或方法的任何基類。</span><span class="sxs-lookup"><span data-stu-id="72474-110">Several derived classes that are related to each other should be grouped into a MOF file, along with any base classes from which they derive properties or methods.</span></span> <span data-ttu-id="72474-111">如果您將每個類別放在個別的 MOF 檔案中，則必須先編譯每個檔案，提供者才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="72474-111">If you place each class in a separate MOF file then each file must be compiled before the provider can work properly.</span></span>

<span data-ttu-id="72474-112">建立類別之後，您必須先刪除類別的所有實例，才能在您的衍生類別上執行下列任何一個活動：</span><span class="sxs-lookup"><span data-stu-id="72474-112">After you create your class, you must delete all instances of your class before you can perform any of the following activities on your derived class:</span></span>

-   <span data-ttu-id="72474-113">變更衍生類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="72474-113">Change the parent class of your derived class.</span></span>
-   <span data-ttu-id="72474-114">新增或移除屬性。</span><span class="sxs-lookup"><span data-stu-id="72474-114">Add or remove properties.</span></span>
-   <span data-ttu-id="72474-115">變更屬性類型。</span><span class="sxs-lookup"><span data-stu-id="72474-115">Change property types.</span></span>
-   <span data-ttu-id="72474-116">新增或移除索引 [**鍵**](key-qualifier.md) 或 **索引** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="72474-116">Add or remove [**Key**](key-qualifier.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="72474-117">新增或移除 [**單一**](standard-wmi-qualifiers.md)、 **動態** 或 [**抽象**](standard-qualifiers.md) 的限定詞。</span><span class="sxs-lookup"><span data-stu-id="72474-117">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

> [!Note]  
> <span data-ttu-id="72474-118">若要加入、移除或修改屬性或辨識符號，請呼叫 [**IWbemServices：:P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)或 [**SWbemObject \_**](swbemobject-put-.md) ，並將旗標參數設定為「強制模式」。</span><span class="sxs-lookup"><span data-stu-id="72474-118">To add, remove, or modify a property or qualifier, call [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) or [**SWbemObject.Put\_**](swbemobject-put-.md) and set the flag parameter to "force mode".</span></span> <span data-ttu-id="72474-119">只有在父類別為抽象時，才能使用 [**抽象**](standard-qualifiers.md) 限定詞。</span><span class="sxs-lookup"><span data-stu-id="72474-119">The [**Abstract**](standard-qualifiers.md) qualifier can be used only if the parent class is abstract.</span></span>

 

<span data-ttu-id="72474-120">當您宣告衍生類別時，請遵守下列規則和限制：</span><span class="sxs-lookup"><span data-stu-id="72474-120">When you declare your derived class, observe the following rules and restrictions:</span></span>

-   <span data-ttu-id="72474-121">衍生類別的父類別必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="72474-121">The parent class of the derived class must already exist.</span></span>

    <span data-ttu-id="72474-122">父類別的宣告可以與衍生類別出現在相同的 MOF 檔案中，也可以出現在不同的檔案中。</span><span class="sxs-lookup"><span data-stu-id="72474-122">The declaration of the parent class can appear in the same MOF file as the derived class or in a different file.</span></span> <span data-ttu-id="72474-123">如果父類別是未知的，則編譯器會產生執行階段錯誤。</span><span class="sxs-lookup"><span data-stu-id="72474-123">If the parent class is unknown, the compiler generates a run-time error.</span></span>

-   <span data-ttu-id="72474-124">衍生類別只能有一個父類別。</span><span class="sxs-lookup"><span data-stu-id="72474-124">A derived class can have only a single parent class.</span></span>

    <span data-ttu-id="72474-125">WMI 不支援多重繼承。</span><span class="sxs-lookup"><span data-stu-id="72474-125">WMI does not support multiple inheritance.</span></span> <span data-ttu-id="72474-126">不過，父類別可以有許多衍生類別。</span><span class="sxs-lookup"><span data-stu-id="72474-126">However, a parent class can have many derived classes.</span></span>

-   <span data-ttu-id="72474-127">您可以定義衍生類別的索引，但 WMI 不會使用這些索引。</span><span class="sxs-lookup"><span data-stu-id="72474-127">You can define indices for derived classes, but WMI does not use these indices.</span></span>

    <span data-ttu-id="72474-128">因此，在衍生類別上指定索引不會改善衍生類別實例的查詢效能。</span><span class="sxs-lookup"><span data-stu-id="72474-128">Therefore, specifying an index on a derived class does not improve the performance of queries for instances of the derived class.</span></span> <span data-ttu-id="72474-129">您可以針對衍生類別的父類別指定索引屬性，以改善衍生類別的查詢效能。</span><span class="sxs-lookup"><span data-stu-id="72474-129">You can improve the performance of a query on a derived class by specifying indexed properties for the parent class of the derived class.</span></span>

-   <span data-ttu-id="72474-130">衍生的類別定義可能更複雜，而且可以包含別名、限定詞和辨識符號等功能。</span><span class="sxs-lookup"><span data-stu-id="72474-130">Derived class definitions can be more complex, and can include such features as aliases, qualifiers, and qualifier flavors.</span></span>

    <span data-ttu-id="72474-131">如需詳細資訊，請參閱 [建立別名](creating-an-alias.md) 和 [新增限定詞](adding-a-qualifier.md)。</span><span class="sxs-lookup"><span data-stu-id="72474-131">For more information, see [Creating an Alias](creating-an-alias.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

-   <span data-ttu-id="72474-132">如果您想要變更限定詞、變更基類屬性的預設值，或使用更強型別來變更基類的參考或内嵌物件屬性，您必須再次宣告整個基類。</span><span class="sxs-lookup"><span data-stu-id="72474-132">If you wish to change a qualifier, change the default value of a base class property, or more strongly type a reference or embedded object property of a base class, you must declare the entire base class again.</span></span>
-   <span data-ttu-id="72474-133">您可以在 WMI 類別中定義的最大屬性數目是1024。</span><span class="sxs-lookup"><span data-stu-id="72474-133">The maximum number of properties you can define in a WMI class is 1024.</span></span>

> [!Note]  
> <span data-ttu-id="72474-134">在執行提供者期間，無法變更類別。</span><span class="sxs-lookup"><span data-stu-id="72474-134">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="72474-135">您必須停止活動、變更類別，然後重新開機 Windows 管理服務。</span><span class="sxs-lookup"><span data-stu-id="72474-135">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="72474-136">目前無法偵測類別變更。</span><span class="sxs-lookup"><span data-stu-id="72474-136">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="72474-137">就像基類一樣，這項技術最常見的用法是用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="72474-137">As with the base class, the most common use of this technique will be by client applications.</span></span> <span data-ttu-id="72474-138">但是，提供者也可以建立衍生類別。</span><span class="sxs-lookup"><span data-stu-id="72474-138">However, a provider can also create a derived class.</span></span> <span data-ttu-id="72474-139">如需詳細資訊，請參閱 [建立基類](creating-a-base-class.md) 和 [撰寫類別提供者](writing-a-class-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="72474-139">For more information, see [Creating a Base Class](creating-a-base-class.md) and [Writing a Class Provider](writing-a-class-provider.md).</span></span>

<span data-ttu-id="72474-140">本主題中的程式碼範例需要下列 \# include 語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="72474-140">The code example in this topic requires the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="72474-141">下列程式說明如何使用 c + + 建立衍生類別。</span><span class="sxs-lookup"><span data-stu-id="72474-141">The following procedure describes how to create a derived class using C++.</span></span>

<span data-ttu-id="72474-142">**使用 c + + 建立衍生類別**</span><span class="sxs-lookup"><span data-stu-id="72474-142">**To create a derived class using C++**</span></span>

1.  <span data-ttu-id="72474-143">找出呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)的基類。</span><span class="sxs-lookup"><span data-stu-id="72474-143">Locate the base class with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

    <span data-ttu-id="72474-144">下列程式碼範例顯示如何找出範例基類。</span><span class="sxs-lookup"><span data-stu-id="72474-144">The following code example shows how to locate the Example base class.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="72474-145">呼叫 [**IWbemClassObject：： SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)，從基類建立衍生物件。</span><span class="sxs-lookup"><span data-stu-id="72474-145">Create a derived object from the base class with a call to [**IWbemClassObject::SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span></span>

    <span data-ttu-id="72474-146">下列程式碼範例顯示如何建立衍生類別物件。</span><span class="sxs-lookup"><span data-stu-id="72474-146">The following code example shows how to create a derived class object.</span></span>

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  <span data-ttu-id="72474-147">藉由設定 **\_ \_ 類別** 系統屬性並呼叫 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)的 ui 方法，來建立類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="72474-147">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="72474-148">下列程式碼範例顯示如何將名稱指派給衍生類別。</span><span class="sxs-lookup"><span data-stu-id="72474-148">The following code example shows how to assign a name to the derived class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="72474-149">使用 IWbemClassObject 來建立其他屬性 [**：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)]。</span><span class="sxs-lookup"><span data-stu-id="72474-149">Create additional properties with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="72474-150">下列程式碼範例顯示如何建立其他屬性。</span><span class="sxs-lookup"><span data-stu-id="72474-150">The following code example shows how to create additional properties.</span></span>

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  <span data-ttu-id="72474-151">藉由呼叫 [**IWbemServices：:P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)來儲存新的類別。</span><span class="sxs-lookup"><span data-stu-id="72474-151">Save the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="72474-152">下列程式碼範例顯示如何儲存新的衍生類別。</span><span class="sxs-lookup"><span data-stu-id="72474-152">The following code example shows how to save the new derived class.</span></span>

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

<span data-ttu-id="72474-153">下列程式碼範例結合了先前程式中所討論的程式碼範例，說明如何使用 WMI API 建立衍生類別。</span><span class="sxs-lookup"><span data-stu-id="72474-153">The following code example combines the code examples discussed in the previous procedure to describe how to create a derived class using the WMI API.</span></span>


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



<span data-ttu-id="72474-154">下列程式描述如何使用 MOF 程式碼定義衍生類別。</span><span class="sxs-lookup"><span data-stu-id="72474-154">The following procedure describes how to define a derived class using MOF code.</span></span>

<span data-ttu-id="72474-155">**使用 MOF 程式碼定義衍生類別**</span><span class="sxs-lookup"><span data-stu-id="72474-155">**To define a derived class using MOF code**</span></span>

1.  <span data-ttu-id="72474-156">使用 **class** 關鍵字定義您的衍生類別，後面接著衍生類別的名稱，並以冒號分隔父類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="72474-156">Define your derived class with the **Class** keyword, followed by the name of your derived class, and the name of the parent class separated by a colon.</span></span>

    <span data-ttu-id="72474-157">下列程式碼範例說明衍生類別的實作為。</span><span class="sxs-lookup"><span data-stu-id="72474-157">The following code example describes an implementation of a derived class.</span></span>

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  <span data-ttu-id="72474-158">完成時，使用 MOF 編譯器編譯您的 MOF 程式碼。</span><span class="sxs-lookup"><span data-stu-id="72474-158">When complete, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="72474-159">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="72474-159">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="72474-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="72474-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72474-161">建立類別</span><span class="sxs-lookup"><span data-stu-id="72474-161">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 




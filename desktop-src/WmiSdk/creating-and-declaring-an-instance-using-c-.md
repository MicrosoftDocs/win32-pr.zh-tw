---
description: 您可以透過 IWbemServices 介面，在 c + + 中建立實例。
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: 使用 c + + 建立和宣告實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997889"
---
# <a name="creating-and-declaring-an-instance-using-c"></a><span data-ttu-id="acc55-103">使用 c + + 建立和宣告實例</span><span class="sxs-lookup"><span data-stu-id="acc55-103">Creating and Declaring an Instance Using C++</span></span>

<span data-ttu-id="acc55-104">您可以透過 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 介面，在 c + + 中建立實例。</span><span class="sxs-lookup"><span data-stu-id="acc55-104">You can create an instance in C++ through the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="acc55-105">本主題中的程式碼範例需要下列 \# include 語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="acc55-105">The code examples in this topic require the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="acc55-106">下列程式描述如何建立現有類別的實例。</span><span class="sxs-lookup"><span data-stu-id="acc55-106">The following procedure describes how to create an instance of an existing class.</span></span>

<span data-ttu-id="acc55-107">**若要建立現有類別的實例**</span><span class="sxs-lookup"><span data-stu-id="acc55-107">**To create an instance of an existing class**</span></span>

1.  <span data-ttu-id="acc55-108">藉由呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 方法，來取出現有類別的定義。</span><span class="sxs-lookup"><span data-stu-id="acc55-108">Retrieve the definition of the existing class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span>

    <span data-ttu-id="acc55-109">下列程式碼範例會示範如何使用 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 和 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 方法，取得可存取類別定義的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="acc55-109">The following code example shows how to use the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to get a pointer to the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface that provides access to the class definition.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                  &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="acc55-110">藉由呼叫 [**IWbemClassObject：： SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) 方法來建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="acc55-110">Create the new instance by calling the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

    <span data-ttu-id="acc55-111">下列程式碼範例示範如何建立新的實例，然後釋放類別。</span><span class="sxs-lookup"><span data-stu-id="acc55-111">The following code example shows how to create a new instance and then release the class.</span></span>

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  <span data-ttu-id="acc55-112">藉由呼叫 [**IWbemClassObject：:P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) 的 ui 方法，設定任何未繼承類別定義之值的屬性值。</span><span class="sxs-lookup"><span data-stu-id="acc55-112">Set values for any properties that do not inherit the values defined for the class by calling the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="acc55-113">類別的每個實例都會繼承針對該類別定義的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="acc55-113">Each instance of a class inherits all of the properties that are defined for the class.</span></span> <span data-ttu-id="acc55-114">但是，如果您選擇，可以指定不同的屬性值。</span><span class="sxs-lookup"><span data-stu-id="acc55-114">However, you can specify different property values if you choose.</span></span>

    <span data-ttu-id="acc55-115">如果現有的類別有索引鍵屬性，您應該將屬性設定為 **Null** 或保證的唯一值。</span><span class="sxs-lookup"><span data-stu-id="acc55-115">If the existing class has a key property, you should set the property either to **NULL** or a guaranteed unique value.</span></span> <span data-ttu-id="acc55-116">如果您將索引鍵設定為 **Null** ，而且索引鍵是字串，則 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) 或 [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) 會在內部產生並指派 GUID 給金鑰。</span><span class="sxs-lookup"><span data-stu-id="acc55-116">If you set the key to **NULL** and the key is a string, then [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) or [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) internally generates and assigns a GUID to the key.</span></span> <span data-ttu-id="acc55-117">如此一來，為索引鍵屬性指定 **Null** ，可讓您建立不會覆寫任何先前實例的唯一實例。</span><span class="sxs-lookup"><span data-stu-id="acc55-117">This way, specifying **NULL** for a key property lets you create a unique instance that will not overwrite any previous instance.</span></span>

    <span data-ttu-id="acc55-118">下列程式碼範例顯示如何設定範例實例類別的 [**Index**](swbemrefreshableitem-index.md) 屬性值。</span><span class="sxs-lookup"><span data-stu-id="acc55-118">The following code example shows how to set the [**Index**](swbemrefreshableitem-index.md) property value of the example instance class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="acc55-119">透過呼叫 [**IWbemClassObject：： GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)，設定任何相關限定詞的值。</span><span class="sxs-lookup"><span data-stu-id="acc55-119">Set the values for any relevant qualifiers through a call to [**IWbemClassObject::GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span></span>

    <span data-ttu-id="acc55-120">[**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)方法會傳回 [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset)介面的指標，該介面會用來存取類別或實例的限定詞。</span><span class="sxs-lookup"><span data-stu-id="acc55-120">The [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) method returns a pointer to an [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface, which use to access the qualifiers for a class or instance.</span></span> <span data-ttu-id="acc55-121">如果類別限定詞的類別為 **EnableOverride**，您可以為類別定義的辨識符號指定不同的值。</span><span class="sxs-lookup"><span data-stu-id="acc55-121">You can specify different values for a qualifier defined for the class if the class qualifier flavor is **EnableOverride**.</span></span> <span data-ttu-id="acc55-122">您無法修改或刪除具有設定為 **DisableOverride** 之類別的類別限定詞。</span><span class="sxs-lookup"><span data-stu-id="acc55-122">You cannot modify or delete a class qualifier with the flavor set to **DisableOverride**.</span></span> <span data-ttu-id="acc55-123">如需詳細資訊，請參閱 [限定詞](qualifier-flavors.md)類別。</span><span class="sxs-lookup"><span data-stu-id="acc55-123">For more information, see [Qualifier Flavors](qualifier-flavors.md).</span></span>

    <span data-ttu-id="acc55-124">您也可以選擇為實例類別定義其他限定詞。</span><span class="sxs-lookup"><span data-stu-id="acc55-124">As an option, you can also define additional qualifiers for your instance class.</span></span> <span data-ttu-id="acc55-125">您可以針對不需要出現在類別宣告中的實例或實例屬性，定義其他限定詞。</span><span class="sxs-lookup"><span data-stu-id="acc55-125">You can define additional qualifiers for the instance or instance property which do not need to appear in the class declaration.</span></span>

5.  <span data-ttu-id="acc55-126">藉由呼叫 [**iwbemservices：:P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) 或 [**Iwbemservices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) 方法來儲存實例。</span><span class="sxs-lookup"><span data-stu-id="acc55-126">Save the instance by calling the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method.</span></span>

    <span data-ttu-id="acc55-127">WMI 會將實例儲存在目前的 WMI 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="acc55-127">WMI saves the instance in the current WMI namespace.</span></span> <span data-ttu-id="acc55-128">因此，實例的完整路徑會相依于命名空間，這通常是根 \\ 預設值。</span><span class="sxs-lookup"><span data-stu-id="acc55-128">As such, the full path of the instance is dependent on the namespace, which is typically root\\default.</span></span> <span data-ttu-id="acc55-129">在此程式碼範例中，完整路徑名稱會是 \\ \\ 。 \\根 \\ 預設值：範例. Index = "IX100"。</span><span class="sxs-lookup"><span data-stu-id="acc55-129">For this code example, the full path name would be \\\\.\\root\\default:Example.Index="IX100".</span></span>

    <span data-ttu-id="acc55-130">下列程式碼範例顯示如何儲存實例。</span><span class="sxs-lookup"><span data-stu-id="acc55-130">The following code example shows how to save an instance.</span></span>

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

<span data-ttu-id="acc55-131">將實例儲存至 WMI 會鎖定實例的數個屬性。</span><span class="sxs-lookup"><span data-stu-id="acc55-131">Saving the instance to WMI locks down several of the properties of the instance.</span></span>

<span data-ttu-id="acc55-132">具體而言，您無法在 WMI 基礎結構內的實例存在之後，透過 WMI API 執行下列任何作業：</span><span class="sxs-lookup"><span data-stu-id="acc55-132">Specifically, you cannot perform any of the following operations through the WMI API after an instance exists within the WMI infrastructure:</span></span>

-   <span data-ttu-id="acc55-133">變更實例所屬類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="acc55-133">Change the parent class of the class to which the instance belongs.</span></span>
-   <span data-ttu-id="acc55-134">新增或移除屬性。</span><span class="sxs-lookup"><span data-stu-id="acc55-134">Add or remove properties.</span></span>
-   <span data-ttu-id="acc55-135">變更屬性類型。</span><span class="sxs-lookup"><span data-stu-id="acc55-135">Change property types.</span></span>
-   <span data-ttu-id="acc55-136">新增或移除索引 [**鍵**](standard-qualifiers.md) 或 **索引** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="acc55-136">Add or remove [**Key**](standard-qualifiers.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="acc55-137">新增或移除 [**單一**](standard-wmi-qualifiers.md)、 **動態** 或 [**抽象**](standard-qualifiers.md) 的限定詞。</span><span class="sxs-lookup"><span data-stu-id="acc55-137">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

<span data-ttu-id="acc55-138">下列程式碼範例結合了先前程式中所討論的程式碼範例，示範如何使用 WMI API 建立實例。</span><span class="sxs-lookup"><span data-stu-id="acc55-138">The following code example combines the code examples discussed in the previous procedure to show how to create an instance using the WMI API.</span></span>


```C++
void CreateInstance (IWbemServices *pSvc)
{
    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    // Get the class definition.
    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                 &pExampleClass, &pResult);
    SysFreeString(PathToClass);

    if (hRes != 0)
       return;

    // Create a new instance.
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more

    VARIANT v;
    VariantInit(&v);

    // Set the Index property (the key).
    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);

    // Set the IntVal property.
    V_VT(&v) = VT_I4;
    V_I4(&v) = 1001;  
    
    BSTR Prop = SysAllocString(L"IntVal");
    pNewInstance->Put(Prop, 0, &v, 0);
    SysFreeString(Prop);
    VariantClear(&v);    
    
    // Other properties acquire the 'default' value specified
    // in the class definition unless otherwise modified here.

    // Write the instance to WMI. 
    hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
    pNewInstance->Release();
}
```



 

 




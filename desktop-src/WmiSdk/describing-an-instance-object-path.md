---
description: 實例物件路徑描述特定命名空間內指定類別之實例的位置。
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: 描述實例物件路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319795"
---
# <a name="describing-an-instance-object-path"></a><span data-ttu-id="e58dd-103">描述實例物件路徑</span><span class="sxs-lookup"><span data-stu-id="e58dd-103">Describing an Instance Object Path</span></span>

<span data-ttu-id="e58dd-104">實例物件路徑描述特定命名空間內指定類別之實例的位置。</span><span class="sxs-lookup"><span data-stu-id="e58dd-104">An instance object path describes the location of an instance of a given class within a specific namespace.</span></span>

<span data-ttu-id="e58dd-105">您可以有數種不同類型的實例物件路徑：</span><span class="sxs-lookup"><span data-stu-id="e58dd-105">You can have several different kinds of instance object paths:</span></span>

-   <span data-ttu-id="e58dd-106">完整</span><span class="sxs-lookup"><span data-stu-id="e58dd-106">Full</span></span>

    <span data-ttu-id="e58dd-107">完整的實例物件路徑會將類別的索引鍵屬性名稱和值附加至完整類別物件路徑。</span><span class="sxs-lookup"><span data-stu-id="e58dd-107">A full instance object path appends the name and value of the key property for the class to a full class object path.</span></span>

    <span data-ttu-id="e58dd-108">下列範例會顯示完整實例物件路徑的定義。</span><span class="sxs-lookup"><span data-stu-id="e58dd-108">The following example shows the definition of the full instance object path.</span></span>

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   <span data-ttu-id="e58dd-109">相對</span><span class="sxs-lookup"><span data-stu-id="e58dd-109">Relative</span></span>

    <span data-ttu-id="e58dd-110">相對物件路徑會參考位於目前伺服器上目前命名空間的實例。</span><span class="sxs-lookup"><span data-stu-id="e58dd-110">A relative object path refers to an instance located in the current namespace on the current server.</span></span> <span data-ttu-id="e58dd-111">相對路徑包含類別名稱，後面接著此實例之索引鍵屬性的名稱和值。</span><span class="sxs-lookup"><span data-stu-id="e58dd-111">The relative path consists of the class name followed by the names and values of the key properties of this instance.</span></span>

    <span data-ttu-id="e58dd-112">下列範例會顯示相對實例物件路徑的定義。</span><span class="sxs-lookup"><span data-stu-id="e58dd-112">The following example shows the definition of the relative instance object path.</span></span>

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   <span data-ttu-id="e58dd-113">相對於單一金鑰</span><span class="sxs-lookup"><span data-stu-id="e58dd-113">Relative with a single key</span></span>

    <span data-ttu-id="e58dd-114">對於僅有一個屬性指定為索引鍵的類別，您可以省略索引鍵屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="e58dd-114">For classes with only one property designated as the key, you can omit the name of the key property.</span></span>

    <span data-ttu-id="e58dd-115">下列範例顯示具有單一索引鍵之相對實例物件路徑的定義。</span><span class="sxs-lookup"><span data-stu-id="e58dd-115">The following example shows the definition of the relative instance object path with a single key.</span></span>

    ``` syntax
    MyClass="e:"
    ```

-   <span data-ttu-id="e58dd-116">相對於多個索引鍵</span><span class="sxs-lookup"><span data-stu-id="e58dd-116">Relative with multiple keys</span></span>

    <span data-ttu-id="e58dd-117">使用逗號來區別具有多個索引鍵的實例索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e58dd-117">Use a comma to distinguish between the keys of an instance with multiple keys.</span></span>

    <span data-ttu-id="e58dd-118">下列範例會顯示具有多個索引鍵之相對實例物件路徑的定義。</span><span class="sxs-lookup"><span data-stu-id="e58dd-118">The following example shows the definitions of the relative instance object path with multiple keys.</span></span>

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   <span data-ttu-id="e58dd-119">相對於單一類別</span><span class="sxs-lookup"><span data-stu-id="e58dd-119">Relative for a singleton class</span></span>

    <span data-ttu-id="e58dd-120">單一類別的相對物件路徑包含類別名稱，後面接著 "= @" 標記法。</span><span class="sxs-lookup"><span data-stu-id="e58dd-120">The relative object path for a singleton class consists of the class name followed by the "=@" notation.</span></span>

    <span data-ttu-id="e58dd-121">下列範例會顯示單一類別之相對實例物件路徑的定義。</span><span class="sxs-lookup"><span data-stu-id="e58dd-121">The following example shows the definition of the relative instance object path for a singleton class.</span></span>

    ``` syntax
    MySingletonClass=@
    ```

<span data-ttu-id="e58dd-122">下列程式描述如何取出類別實例。</span><span class="sxs-lookup"><span data-stu-id="e58dd-122">The following procedure describes how to retrieve a class instance.</span></span>

<span data-ttu-id="e58dd-123">**若要取出類別實例**</span><span class="sxs-lookup"><span data-stu-id="e58dd-123">**To retrieve a class instance**</span></span>

1.  <span data-ttu-id="e58dd-124">使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 函式的呼叫，初始化包含物件路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="e58dd-124">Initialize a string that contains the object path with a call to the [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) function.</span></span>
2.  <span data-ttu-id="e58dd-125">初始化將接收實例的物件。</span><span class="sxs-lookup"><span data-stu-id="e58dd-125">Initialize an object that will receive the instance.</span></span>
3.  <span data-ttu-id="e58dd-126">透過呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)來取出物件。</span><span class="sxs-lookup"><span data-stu-id="e58dd-126">Retrieve the object with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="e58dd-127">若要使用 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)，您必須執行 [**IWbemSink**](swbemsink.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="e58dd-127">To use [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), you must implement the [**IWbemSink**](swbemsink.md) interface.</span></span>

<span data-ttu-id="e58dd-128">\#本主題稍後所列的程式碼需要下列 include 語句，才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="e58dd-128">The following \#include statement is required for the code that is listed later in this topic to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="e58dd-129">下列程式碼範例說明如何使用物件路徑來取出類別實例。</span><span class="sxs-lookup"><span data-stu-id="e58dd-129">The following code example describes how to retrieve a class instance using an object path.</span></span>


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



<span data-ttu-id="e58dd-130">針對指定多個屬性做為索引鍵之類別的實例，WMI 不需要在物件路徑中有特定的索引鍵屬性順序。</span><span class="sxs-lookup"><span data-stu-id="e58dd-130">For instances of classes that specify multiple properties as the key, WMI requires no specific ordering of key properties in object paths.</span></span> <span data-ttu-id="e58dd-131">您只需要指定物件路徑中每個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e58dd-131">You need only specify the value of each of the properties in the object path.</span></span>

<span data-ttu-id="e58dd-132">下列程式碼範例描述兩個對等的索引鍵描述。</span><span class="sxs-lookup"><span data-stu-id="e58dd-132">The following code example describes two equivalent key descriptions.</span></span>

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 

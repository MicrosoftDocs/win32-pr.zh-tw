---
description: 您可以使用受控物件格式 (MOF) ，在 Windows 管理服務中宣告類別的基本實例。 您也可以覆寫實例的預設值。 如需詳細資訊，請參閱設定實例屬性值。
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: 使用 MOF 建立實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5078c5fcddaab4e8437a33e8cb3210d515360fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975032"
---
# <a name="creating-an-instance-using-mof"></a><span data-ttu-id="f0293-105">使用 MOF 建立實例</span><span class="sxs-lookup"><span data-stu-id="f0293-105">Creating an Instance Using MOF</span></span>

<span data-ttu-id="f0293-106">您可以使用受控物件格式 (MOF) ，在 Windows 管理服務中宣告類別的基本實例。</span><span class="sxs-lookup"><span data-stu-id="f0293-106">You can declare a basic instance of a class in the Windows Management service using Managed Object Format (MOF).</span></span> <span data-ttu-id="f0293-107">您也可以覆寫實例的預設值。</span><span class="sxs-lookup"><span data-stu-id="f0293-107">You can also override the default values for an instance.</span></span> <span data-ttu-id="f0293-108">如需詳細資訊，請參閱 [設定實例屬性值](#setting-an-instance-property-value)。</span><span class="sxs-lookup"><span data-stu-id="f0293-108">For more information, see [Setting an Instance Property Value](#setting-an-instance-property-value).</span></span>

<span data-ttu-id="f0293-109">下列程式描述如何使用 MOF 程式碼宣告類別的基本實例。</span><span class="sxs-lookup"><span data-stu-id="f0293-109">The following procedure describes how to declare a basic instance of a class using MOF code.</span></span>

<span data-ttu-id="f0293-110">**使用 MOF 程式碼宣告類別的基本實例**</span><span class="sxs-lookup"><span data-stu-id="f0293-110">**To declare a basic instance of a class using MOF code**</span></span>

1.  <span data-ttu-id="f0293-111">使用關鍵字的 **實例** ，後面接著類別名稱、大括弧和分號。</span><span class="sxs-lookup"><span data-stu-id="f0293-111">Use the **Instance of** keywords followed by the class name, curly braces, and a semicolon.</span></span>

    <span data-ttu-id="f0293-112">下列程式碼範例顯示如何宣告類別的實例。</span><span class="sxs-lookup"><span data-stu-id="f0293-112">The following code example shows how to declare an instance of a class.</span></span>

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  <span data-ttu-id="f0293-113">完成之後，請使用 MOF 編譯器將您的 MOF 程式碼插入 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="f0293-113">When finished, insert your MOF code into the WMI repository using the MOF compiler.</span></span>

    <span data-ttu-id="f0293-114">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="f0293-114">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="f0293-115">類別的實例包含類別的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="f0293-115">An instance of a class includes all of the properties of the class.</span></span> <span data-ttu-id="f0293-116">如果類別是衍生類別，則實例會包含屬於階層中所有較高類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="f0293-116">If the class is a derived class, instances include the properties belonging to all of the classes higher in the hierarchy.</span></span> <span data-ttu-id="f0293-117">建立實例的每個類別都有一或多個索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="f0293-117">Each class that an instance is created from has one or more key properties.</span></span> <span data-ttu-id="f0293-118">您無法使用超過256的索引鍵來建立實例。</span><span class="sxs-lookup"><span data-stu-id="f0293-118">You cannot create an instance with more than 256 keys.</span></span>

## <a name="setting-an-instance-property-value"></a><span data-ttu-id="f0293-119">設定實例屬性值</span><span class="sxs-lookup"><span data-stu-id="f0293-119">Setting an Instance Property Value</span></span>

<span data-ttu-id="f0293-120">因為 WMI 強型別屬性，所以您無法修改屬性類型。</span><span class="sxs-lookup"><span data-stu-id="f0293-120">Because WMI strongly types properties, you cannot modify property types.</span></span> <span data-ttu-id="f0293-121">不過，您可以在實例中設定屬性值。</span><span class="sxs-lookup"><span data-stu-id="f0293-121">You can, however, set property values in instances.</span></span> <span data-ttu-id="f0293-122">當類別將預設值指派給屬性時，WMI 會將預設值指派給每個實例。</span><span class="sxs-lookup"><span data-stu-id="f0293-122">When a class assigns a default value to a property, WMI assigns the default value to each instance.</span></span> <span data-ttu-id="f0293-123">您可以在實例宣告中覆寫這個值。</span><span class="sxs-lookup"><span data-stu-id="f0293-123">You can override this value in your instance declaration.</span></span>

<span data-ttu-id="f0293-124">下列程式描述如何使用 MOF 程式碼設定屬性值或覆寫預設值。</span><span class="sxs-lookup"><span data-stu-id="f0293-124">The following procedure describes how to set a property value or overwrite a default value using MOF code.</span></span>

<span data-ttu-id="f0293-125">**使用 MOF 程式碼設定屬性值或覆寫預設值**</span><span class="sxs-lookup"><span data-stu-id="f0293-125">**To set a property value or overwrite a default value using MOF code**</span></span>

1.  <span data-ttu-id="f0293-126">在實例宣告的大括弧之間放置指派語句。</span><span class="sxs-lookup"><span data-stu-id="f0293-126">Place an assignment statement between the curly braces of the instance declaration.</span></span>

    <span data-ttu-id="f0293-127">下列程式碼範例顯示如何設定屬性值。</span><span class="sxs-lookup"><span data-stu-id="f0293-127">The following code example shows how to set a property value.</span></span>

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    <span data-ttu-id="f0293-128">WMI 不需要您在建立實例時設定任何屬性。</span><span class="sxs-lookup"><span data-stu-id="f0293-128">WMI does not require that you set any property during instance creation.</span></span> <span data-ttu-id="f0293-129">例外狀況是以 [**金鑰**](key-qualifier.md) 辨識符號標記的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="f0293-129">The exception is any property marked with the [**Key**](key-qualifier.md) qualifier.</span></span> <span data-ttu-id="f0293-130">因為 WMI 會使用索引鍵屬性來唯一識別實例，所以您必須在遇到時設定所有索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="f0293-130">Because WMI uses key properties to uniquely identify instances, you must set all key properties as you encounter them.</span></span> <span data-ttu-id="f0293-131">相反地，您不能在實例宣告中設定系統屬性。</span><span class="sxs-lookup"><span data-stu-id="f0293-131">In contrast, you must not set a system property in an instance declaration.</span></span> <span data-ttu-id="f0293-132">相反地，WMI 會在必要時將適當的值指派給系統屬性。</span><span class="sxs-lookup"><span data-stu-id="f0293-132">Instead, WMI assigns the appropriate values to a system property when necessary.</span></span>

2.  <span data-ttu-id="f0293-133">完成之後，請呼叫 MOF 編譯器以將您的 MOF 程式碼插入 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="f0293-133">When finished, insert your MOF code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="f0293-134">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="f0293-134">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="f0293-135">下列程式碼範例顯示實例如何指定類別所定義之屬性的資料。</span><span class="sxs-lookup"><span data-stu-id="f0293-135">The following code examples show how an instance specifies data for properties defined by a class.</span></span>

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

<span data-ttu-id="f0293-136">在上述範例中，類別會定義三個屬性：字元字串、32位帶正負號的整數，以及32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="f0293-136">In the preceding example, the class defines three properties: a character string, a 32-bit signed integer, and a 32-bit unsigned integer.</span></span> <span data-ttu-id="f0293-137">實例會提供每個屬性的資料值。</span><span class="sxs-lookup"><span data-stu-id="f0293-137">The instance provides data values for each of these properties.</span></span>

 

 




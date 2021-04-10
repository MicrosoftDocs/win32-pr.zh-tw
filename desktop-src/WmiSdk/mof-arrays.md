---
description: 陣列是具有相同資料類型之資料值的索引清單，您可以參考這些資料值。 除了字串和數值陣列，MOF 還支援内嵌物件和參考的陣列。
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: MOF 陣列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0443f2ef3b3fe8fca398e281de71b0927a4f06f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191726"
---
# <a name="mof-arrays"></a><span data-ttu-id="e6440-104">MOF 陣列</span><span class="sxs-lookup"><span data-stu-id="e6440-104">MOF Arrays</span></span>

<span data-ttu-id="e6440-105">陣列是具有相同資料類型之資料值的索引清單，您可以參考這些資料值。</span><span class="sxs-lookup"><span data-stu-id="e6440-105">An array is an indexed list of data values that are of the same data type, which you can reference.</span></span> <span data-ttu-id="e6440-106">除了字串和數值陣列，MOF 還支援内嵌物件和參考的陣列。</span><span class="sxs-lookup"><span data-stu-id="e6440-106">In addition to string and numeric arrays, MOF supports arrays of embedded objects and references.</span></span>

<span data-ttu-id="e6440-107">下列規則會定義 MOF 陣列：</span><span class="sxs-lookup"><span data-stu-id="e6440-107">The following rules define a MOF array:</span></span>

-   <span data-ttu-id="e6440-108">屬性識別碼之後所用的括弧會指定類別定義中的陣列。</span><span class="sxs-lookup"><span data-stu-id="e6440-108">Brackets used after the property identifier specify an array in a class definition.</span></span>

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   <span data-ttu-id="e6440-109">所有陣列都必須是一維的。</span><span class="sxs-lookup"><span data-stu-id="e6440-109">All arrays must be one-dimensional.</span></span>
-   <span data-ttu-id="e6440-110">陣列可無限制或具有明確的大小。</span><span class="sxs-lookup"><span data-stu-id="e6440-110">Arrays can be unbounded or have an explicit size.</span></span>

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    <span data-ttu-id="e6440-111">WMI 會將系結和無限制的陣列實作為 **SAFEARRAY** 結構，讓 WMI 在執行時間改變數組維度。</span><span class="sxs-lookup"><span data-stu-id="e6440-111">WMI implements bounded and unbounded arrays as **SAFEARRAY** structures, which allows WMI to vary array dimensions at run time.</span></span> <span data-ttu-id="e6440-112">當您宣告明確大小的陣列時，WMI 會將大小儲存為辨識符號，並將大小視為建議的最大大小。</span><span class="sxs-lookup"><span data-stu-id="e6440-112">When you declare an array with an explicit size, WMI stores the size as a qualifier, and treats the size as the suggested maximum size.</span></span> <span data-ttu-id="e6440-113">不過，WMI 可以視需要擴充大小。</span><span class="sxs-lookup"><span data-stu-id="e6440-113">However, WMI can expand the size if necessary.</span></span> <span data-ttu-id="e6440-114">變更明確的大小不會影響實際的資料。</span><span class="sxs-lookup"><span data-stu-id="e6440-114">Changing the explicit size has no effect on the actual data.</span></span>

-   <span data-ttu-id="e6440-115">陣列的初始化方式是在逗號分隔清單中指定適當類型的值。</span><span class="sxs-lookup"><span data-stu-id="e6440-115">Arrays are initialized by specifying values of the appropriate type in a comma-separated list.</span></span>

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   <span data-ttu-id="e6440-116">參考的陣列會宣告為物件路徑字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="e6440-116">An array of references is declared as an array of object path strings.</span></span>

    <span data-ttu-id="e6440-117">宣告物件路徑字串時，請勿在物件路徑的元素之間放置空白字元。</span><span class="sxs-lookup"><span data-stu-id="e6440-117">When declaring an object path string, do not place white space between the elements of the object path.</span></span> <span data-ttu-id="e6440-118">下列範例說明如何宣告物件路徑參考。</span><span class="sxs-lookup"><span data-stu-id="e6440-118">The following example describes how to declare an object path reference.</span></span>

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   <span data-ttu-id="e6440-119">您可以使用陣列做為方法的參數，但不能做為輸入或輸入輸出參數的傳回值。</span><span class="sxs-lookup"><span data-stu-id="e6440-119">You can use an array as a parameter for a method, but not as a return value for an input or input-output parameter.</span></span>
-   <span data-ttu-id="e6440-120">陣列中的所有元素都會建立為相同類型的值。</span><span class="sxs-lookup"><span data-stu-id="e6440-120">All elements in an array are created as values of the same type.</span></span>

    <span data-ttu-id="e6440-121">如果陣列的元素屬於 **物件** 類型，則您可以將任何類型的物件放在陣列中。</span><span class="sxs-lookup"><span data-stu-id="e6440-121">If the elements of an array are of the **object** type, then you can place any kind of object in the array.</span></span> <span data-ttu-id="e6440-122">另一方面，如果您宣告特定類型的物件，則 WMI 只允許該類別的物件或陣列中的子類別。</span><span class="sxs-lookup"><span data-stu-id="e6440-122">On the other hand, if you declare a specific type of object, then WMI allows only objects of that class or subclass in the array.</span></span> <span data-ttu-id="e6440-123">下列範例顯示包含使用 **物件** 類型的陣列宣告。</span><span class="sxs-lookup"><span data-stu-id="e6440-123">The following examples show array declarations that includes using the **object** type.</span></span>

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 




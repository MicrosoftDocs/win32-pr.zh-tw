---
description: 抓取與特定來源實例相關聯的所有實例。
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: 語句 ASSOCIATORS OF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec595584efb5c32342e5bbdaa8bae309b21b29d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320031"
---
# <a name="associators-of-statement"></a><span data-ttu-id="e2053-103">語句 ASSOCIATORS OF</span><span class="sxs-lookup"><span data-stu-id="e2053-103">ASSOCIATORS OF Statement</span></span>

<span data-ttu-id="e2053-104">語句的 ASSOCIATORS OF 會抓取與特定來源實例相關聯的所有實例。</span><span class="sxs-lookup"><span data-stu-id="e2053-104">The ASSOCIATORS OF statement retrieves all instances that are associated with a particular source instance.</span></span> <span data-ttu-id="e2053-105">取出的實例稱為端點。</span><span class="sxs-lookup"><span data-stu-id="e2053-105">The instances that are retrieved are referred to as the endpoints.</span></span> <span data-ttu-id="e2053-106">每個端點會以其與來源物件之間的關聯，多次傳回。</span><span class="sxs-lookup"><span data-stu-id="e2053-106">Each endpoint is returned as many times as there are associations between it and the source object.</span></span> <span data-ttu-id="e2053-107">例如，假設有實例 A、B、X 和 Y。有兩個關聯實例存在，一個連結 A 和 X，另一個連結 B 和 Y。下列查詢會傳回單一端點 X：</span><span class="sxs-lookup"><span data-stu-id="e2053-107">For example, assume there are instances A, B, X, and Y. Two association instances exist, one that links A and X and another that links B and Y. The following query returns the single endpoint X:</span></span>


```sql
ASSOCIATORS OF {A}
```



<span data-ttu-id="e2053-108">但是，如果有另一個關聯連結 A 和 X，則上述查詢會傳回兩個 X 端點。</span><span class="sxs-lookup"><span data-stu-id="e2053-108">However, if there is another association linking A and X, the above query returns two X endpoints.</span></span>

<span data-ttu-id="e2053-109">ASSOCIATORS OF 語句的基本語法為：</span><span class="sxs-lookup"><span data-stu-id="e2053-109">The basic syntax for the ASSOCIATORS OF statement is:</span></span>

``` syntax
ASSOCIATORS OF {ObjectPath}
```

<span data-ttu-id="e2053-110">請注意，大括弧是語法的一部分。</span><span class="sxs-lookup"><span data-stu-id="e2053-110">Note that the braces are part of the syntax.</span></span> <span data-ttu-id="e2053-111">任何有效的物件路徑都可以用於 ObjectPath。</span><span class="sxs-lookup"><span data-stu-id="e2053-111">Any valid object path can be used for ObjectPath.</span></span> <span data-ttu-id="e2053-112">物件路徑內的標記不可包含任何空白字元。</span><span class="sxs-lookup"><span data-stu-id="e2053-112">The tokens within the object path cannot contain any white space.</span></span> <span data-ttu-id="e2053-113">例如，下列清單中的查詢會傳回與指定的邏輯磁片相關聯的實例：</span><span class="sxs-lookup"><span data-stu-id="e2053-113">For example, the query in the following list returns instances that are associated with the specified logical disk:</span></span>

<dl> <dt>

<span data-ttu-id="e2053-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：</span><span class="sxs-lookup"><span data-stu-id="e2053-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span data-ttu-id="e2053-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：</span><span class="sxs-lookup"><span data-stu-id="e2053-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="e2053-116">如同 [select 語句](select-statement-for-data-queries.md)，語句的 associators of 可以包含 [WHERE 子句](where-clause.md)，但語句 associators of 的 WHERE 子句與 SELECT statementWHERE 子句非常不同。</span><span class="sxs-lookup"><span data-stu-id="e2053-116">As with the [SELECT statement](select-statement-for-data-queries.md), an ASSOCIATORS OF statement can include a [WHERE clause](where-clause.md), but the WHERE clause for an ASSOCIATORS OF statement is very different from the SELECT statementWHERE clause.</span></span>

<span data-ttu-id="e2053-117">語句 ASSOCIATORS OF 的 [WHERE 子句](where-clause.md) 可以包含下列一或多個預先定義的關鍵字和其值：</span><span class="sxs-lookup"><span data-stu-id="e2053-117">The [WHERE clause](where-clause.md) of the ASSOCIATORS OF statement can include one or more of the following predefined keywords and their values:</span></span>


```sql
ASSOCIATORS OF {ObjectPath} WHERE
    AssocClass = AssocClassName
    ClassDefsOnly
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
```



<span data-ttu-id="e2053-118">請注意，選擇性的子條款不會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="e2053-118">Note that the optional subclauses are not separated by commas.</span></span>

<span data-ttu-id="e2053-119">**AssocClass** 關鍵字指出傳回的端點必須透過指定的類別或其衍生類別的其中一個來與來源產生關聯。</span><span class="sxs-lookup"><span data-stu-id="e2053-119">The **AssocClass** keyword indicates that the returned endpoints must be associated with the source through the specified class or one of its derived classes.</span></span> <span data-ttu-id="e2053-120">例如，下列清單中的查詢只會傳回透過 [**Win32 \_ SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) association 類別或其任何衍生類別與來源相關聯的端點：</span><span class="sxs-lookup"><span data-stu-id="e2053-120">For example, the query in the following list returns only endpoints that are associated with the source through the [**Win32\_SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) association class or any of its derived classes:</span></span>

<dl> <dt>

<span data-ttu-id="e2053-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：</span><span class="sxs-lookup"><span data-stu-id="e2053-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span data-ttu-id="e2053-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：</span><span class="sxs-lookup"><span data-stu-id="e2053-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="e2053-123">**ClassDefsOnly** 關鍵字指出子句會傳回類別定義物件的結果集，而不是類別的實際實例。</span><span class="sxs-lookup"><span data-stu-id="e2053-123">The **ClassDefsOnly** keyword indicates that the clause returns a result set of class definition objects rather than actual instances of the classes.</span></span> <span data-ttu-id="e2053-124">這些物件是端點實例所屬類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e2053-124">These objects are the definitions of classes to which the endpoint instances belong.</span></span> <span data-ttu-id="e2053-125">例如，下列清單中的查詢會傳回 [**win32 \_ 目錄**](/windows/desktop/CIMWin32Prov/win32-directory) 和 win32 執行程式類別 [**\_**](/windows/desktop/CIMWin32Prov/win32-computersystem) 的定義：</span><span class="sxs-lookup"><span data-stu-id="e2053-125">For example, the query in the following list returns definitions for the [**Win32\_Directory**](/windows/desktop/CIMWin32Prov/win32-directory) and [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) classes:</span></span>

<dl> <dt>

<span data-ttu-id="e2053-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：</span><span class="sxs-lookup"><span data-stu-id="e2053-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span data-ttu-id="e2053-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：</span><span class="sxs-lookup"><span data-stu-id="e2053-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

<span data-ttu-id="e2053-128">**ClassDefsOnly** 和 **ResultClass** 關鍵字是互斥的。</span><span class="sxs-lookup"><span data-stu-id="e2053-128">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="e2053-129">一起使用它們會導致不正確查詢錯誤。</span><span class="sxs-lookup"><span data-stu-id="e2053-129">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="e2053-130">**RequiredAssocQualifier** 關鍵字指出傳回的端點必須透過包含指定限定詞的關聯類別，與來源物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="e2053-130">The **RequiredAssocQualifier** keyword indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span> <span data-ttu-id="e2053-131">這種類型的篩選可用來消除範圍廣泛的端點，除非端點透過一組特定的標記關聯類別與目標相關聯。</span><span class="sxs-lookup"><span data-stu-id="e2053-131">This type of filtering is used to eliminate broad ranges of endpoints unless the endpoints are associated with the target through a particular set of tagged association classes.</span></span> <span data-ttu-id="e2053-132">例如，如果 association 類別包含稱為 **association** 的辨識符號，則下列清單中的查詢會傳回端點實例。</span><span class="sxs-lookup"><span data-stu-id="e2053-132">For example, the query in the following list returns endpoint instances if the association class includes a qualifier called **Association**.</span></span>

<dl> <dt>

<span data-ttu-id="e2053-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：</span><span class="sxs-lookup"><span data-stu-id="e2053-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span data-ttu-id="e2053-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：</span><span class="sxs-lookup"><span data-stu-id="e2053-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="e2053-135">**RequiredQualifier** 關鍵字表示與來源物件相關聯的傳回端點必須包含指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="e2053-135">The **RequiredQualifier** keyword indicates that the returned endpoints associated with the source object must include the specified qualifier.</span></span> <span data-ttu-id="e2053-136">**RequiredQualifier** 關鍵字可以用來在結果集中包含特定類型的實例。</span><span class="sxs-lookup"><span data-stu-id="e2053-136">The **RequiredQualifier** keyword can be used to include particular types of instances in the result set.</span></span> <span data-ttu-id="e2053-137">例如，下列清單中的查詢會傳回包含稱為 [**Locale**](swbemobjectpath-locale.md)的辨識符號的端點實例。</span><span class="sxs-lookup"><span data-stu-id="e2053-137">For example, the query in the following list returns endpoint instances that include a qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span>

<dl> <dt>

<span data-ttu-id="e2053-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：</span><span class="sxs-lookup"><span data-stu-id="e2053-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span data-ttu-id="e2053-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：</span><span class="sxs-lookup"><span data-stu-id="e2053-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="e2053-140">**ResultClass** 關鍵字表示與來源物件相關聯的傳回端點必須屬於或衍生自指定的類別。</span><span class="sxs-lookup"><span data-stu-id="e2053-140">The **ResultClass** keyword indicates that the returned endpoints associated with the source object must belong to or be derived from the specified class.</span></span> <span data-ttu-id="e2053-141">例如，下列清單中的查詢會傳回衍生自 [**CIM \_ 目錄**](/windows/desktop/CIMWin32Prov/cim-directory) 類別的端點實例：</span><span class="sxs-lookup"><span data-stu-id="e2053-141">For example, the query in the following list returns endpoint instances that are derived from the [**CIM\_Directory**](/windows/desktop/CIMWin32Prov/cim-directory) class:</span></span>

<dl> <dt>

<span data-ttu-id="e2053-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：</span><span class="sxs-lookup"><span data-stu-id="e2053-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span data-ttu-id="e2053-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：</span><span class="sxs-lookup"><span data-stu-id="e2053-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

<span data-ttu-id="e2053-144">**ClassDefsOnly** 和 **ResultClass** 關鍵字是互斥的。</span><span class="sxs-lookup"><span data-stu-id="e2053-144">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="e2053-145">一起使用它們會導致不正確查詢錯誤。</span><span class="sxs-lookup"><span data-stu-id="e2053-145">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="e2053-146">**ResultRole** 關鍵字指出傳回的端點必須在其與來源物件的關聯中扮演特定的角色。</span><span class="sxs-lookup"><span data-stu-id="e2053-146">The **ResultRole** keyword indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="e2053-147">角色是由指定的屬性所定義，即 [ref](references.md)類型的參考屬性。例如，您可以使用 **ResultRole** 關鍵字，在其與來源物件的關聯中取得具有 **GroupComponent** 屬性的所有端點，如下列查詢所示。</span><span class="sxs-lookup"><span data-stu-id="e2053-147">The role is defined by the specified property, a reference property of type [ref](references.md). For example, the **ResultRole** keyword can be used to retrieve all endpoints that have the **GroupComponent** property in their association with a source object, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="e2053-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：</span><span class="sxs-lookup"><span data-stu-id="e2053-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span data-ttu-id="e2053-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：</span><span class="sxs-lookup"><span data-stu-id="e2053-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="e2053-150">**Role** 關鍵字表示傳回的端點會參與與來源物件（其來源物件扮演特定角色）的關聯。</span><span class="sxs-lookup"><span data-stu-id="e2053-150">The **Role** keyword indicates that the returned endpoints participate in an association with the source object where the source object plays a particular role.</span></span> <span data-ttu-id="e2053-151">角色是由指定的屬性所定義，即 **ref** 類型的參考屬性。例如， **Role** 關鍵字可用來取得與具有 **GroupComponent** 屬性之來源物件相關聯的所有端點，如下列查詢所示。</span><span class="sxs-lookup"><span data-stu-id="e2053-151">The role is defined by the specified property, a reference property of type **ref**. For example, the **Role** keyword can be used to retrieve all endpoints associated with a source object that have the **GroupComponent** property, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="e2053-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>查詢：</span><span class="sxs-lookup"><span data-stu-id="e2053-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span data-ttu-id="e2053-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>結果：</span><span class="sxs-lookup"><span data-stu-id="e2053-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> <span data-ttu-id="e2053-154">複雜的查詢不能使用 "And" 或 "Or" 來分隔 ASSOCIATORS OF 和語句 [參考的](references-of-statement.md) 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="e2053-154">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and [REFERENCES OF](references-of-statement.md) statements.</span></span> <span data-ttu-id="e2053-155">此外，等號是唯一可用於這類查詢的有效運算子。</span><span class="sxs-lookup"><span data-stu-id="e2053-155">Furthermore, the equal sign is the only valid operator that can be used in such queries.</span></span> <span data-ttu-id="e2053-156">例如，以下是有效的查詢：</span><span class="sxs-lookup"><span data-stu-id="e2053-156">For example, the following query is valid:</span></span>

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> <span data-ttu-id="e2053-157">接下來的範例是不正確。</span><span class="sxs-lookup"><span data-stu-id="e2053-157">The next examples are not valid.</span></span> <span data-ttu-id="e2053-158">第一個範例不會使用等號，而第二個範例會錯誤地嘗試使用 **和** 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="e2053-158">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword.</span></span>

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 

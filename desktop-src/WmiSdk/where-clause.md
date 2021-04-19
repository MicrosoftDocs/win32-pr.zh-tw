---
description: 使用 WHERE 子句來縮小資料、事件或架構查詢的範圍。
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: 'WHERE 子句 (WMI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e68d8266b72f6e41e17c0b85766b7a58bb197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991935"
---
# <a name="where-clause-wmi"></a><span data-ttu-id="71325-103">WHERE 子句 (WMI) </span><span class="sxs-lookup"><span data-stu-id="71325-103">WHERE Clause (WMI)</span></span>

<span data-ttu-id="71325-104">使用 WHERE 子句來縮小資料、事件或架構查詢的範圍。</span><span class="sxs-lookup"><span data-stu-id="71325-104">Use the WHERE clause to narrow the scope of a data, event, or schema query.</span></span> <span data-ttu-id="71325-105">如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="71325-105">For more information, see [Querying with WQL](querying-with-wql.md).</span></span> <span data-ttu-id="71325-106">WHERE 子句是由屬性或關鍵字、運算子和常數所組成。</span><span class="sxs-lookup"><span data-stu-id="71325-106">The WHERE clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="71325-107">所有 WHERE 子句都必須指定其中一個預先定義的運算子，其中包含在 Windows Management Instrumentation (WMI) 查詢語言 (WQL) 中。</span><span class="sxs-lookup"><span data-stu-id="71325-107">All WHERE clauses must specify one of the predefined operators that are included in the Windows Management Instrumentation (WMI) Query Language (WQL).</span></span> <span data-ttu-id="71325-108">您可以使用下列其中一種形式，將 WHERE 子句附加至 SELECT 語句：</span><span class="sxs-lookup"><span data-stu-id="71325-108">You can append the WHERE clause to the SELECT statement using one of the following forms:</span></span>


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



<span data-ttu-id="71325-109">其中 \* 是查詢的專案，類別是要查詢的類別，而常數、運算子和屬性則是要使用的常數、運算子和屬性或關鍵字。</span><span class="sxs-lookup"><span data-stu-id="71325-109">where \* is the item queried about, class is the class in which to query, and constant, operator, and property are the constant, operator, and property or keyword to use.</span></span> <span data-ttu-id="71325-110">如需 SELECT 語句的詳細資訊，請參閱 [資料查詢的 Select 語句](select-statement-for-data-queries.md)、 [事件查詢的 select](select-statement-for-event-queries.md)語句，或 [架構查詢的 select 語句](select-statement-for-schema-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="71325-110">For more information about the SELECT statement, see [SELECT Statement for Data Queries](select-statement-for-data-queries.md), [SELECT Statement for Event Queries](select-statement-for-event-queries.md), or [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="71325-111">常數的值必須是屬性的正確類型。</span><span class="sxs-lookup"><span data-stu-id="71325-111">The value of the constant must be of the correct type for the property.</span></span> <span data-ttu-id="71325-112">此外，運算子必須在有效的 [WQL 運算子](wql-operators.md)清單中。</span><span class="sxs-lookup"><span data-stu-id="71325-112">Moreover, the operator must be among the list of valid [WQL operators](wql-operators.md).</span></span> <span data-ttu-id="71325-113">屬性名稱或常數必須出現在 WHERE 子句中運算子的任一邊。</span><span class="sxs-lookup"><span data-stu-id="71325-113">Either a property name or a constant must appear on either side of the operator in the WHERE clause.</span></span>

<span data-ttu-id="71325-114">在 WHERE 子句中，您可以使用字串常值（例如 "NTFS"）。</span><span class="sxs-lookup"><span data-stu-id="71325-114">You may use string literals, such as "NTFS", in a WHERE clause.</span></span> <span data-ttu-id="71325-115">如果您想要在字串中包含下列特殊字元，您必須先在字元前面加上反斜線 (，以將字元轉義 \) ：</span><span class="sxs-lookup"><span data-stu-id="71325-115">If you wish to include the following special characters in your string, you must first escape the character by prefixing the character with a backslash (\):</span></span>

-   <span data-ttu-id="71325-116">反斜線 (\\\)</span><span class="sxs-lookup"><span data-stu-id="71325-116">backslash (\\\)</span></span>
-   <span data-ttu-id="71325-117">雙引號 (\\ ") </span><span class="sxs-lookup"><span data-stu-id="71325-117">double quotes (\\")</span></span>
-   <span data-ttu-id="71325-118">單引號 (\\ ' ) </span><span class="sxs-lookup"><span data-stu-id="71325-118">single quotes (\\')</span></span>

<span data-ttu-id="71325-119">不能使用任意算術運算式。</span><span class="sxs-lookup"><span data-stu-id="71325-119">Arbitrary arithmetic expressions cannot be used.</span></span> <span data-ttu-id="71325-120">例如，下列查詢只會傳回代表 NTFS 磁片磁碟機之 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的實例：</span><span class="sxs-lookup"><span data-stu-id="71325-120">For example, the following query returns only the instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class that represent NTFS drives:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



<span data-ttu-id="71325-121">屬性名稱不能出現在運算子的兩邊。</span><span class="sxs-lookup"><span data-stu-id="71325-121">Property names cannot appear on both sides of the operator.</span></span> <span data-ttu-id="71325-122">下列查詢是無效查詢的範例：</span><span class="sxs-lookup"><span data-stu-id="71325-122">The following query is an example of an invalid query:</span></span>


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



<span data-ttu-id="71325-123">針對 WHERE 子句中類別描述項的大部分用法，WMI 會將查詢標示為無效，並傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="71325-123">For most uses of class descriptors in a WHERE clause, WMI flags the query as invalid and returns an error.</span></span> <span data-ttu-id="71325-124">不過，請針對 WMI 中 **object** 類型的屬性使用點 (. ) 運算子。</span><span class="sxs-lookup"><span data-stu-id="71325-124">However, use the dot (.) operator for properties of type **object** in WMI.</span></span> <span data-ttu-id="71325-125">例如，如果屬性是 MyClass 的有效屬性且為型別 **物件**，則下列查詢會是有效的：</span><span class="sxs-lookup"><span data-stu-id="71325-125">For example, the following query is valid if Prop is a valid property of MyClass and is type **object**:</span></span>

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

<span data-ttu-id="71325-126">比較測試一律不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="71325-126">Comparison tests are always case-insensitive.</span></span> <span data-ttu-id="71325-127">也就是說，下列三個語句全都評估為 **TRUE**：</span><span class="sxs-lookup"><span data-stu-id="71325-127">That is, the following three statements all evaluate to **TRUE**:</span></span>


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



<span data-ttu-id="71325-128">您可以建立包含布林資料類型的查詢，但唯一有效的布林運算元類型為 =、！ = 和 <> 類型。</span><span class="sxs-lookup"><span data-stu-id="71325-128">You can construct a query that includes Boolean data types, but the only valid Boolean operand types are the =, != and <> types.</span></span> <span data-ttu-id="71325-129">**TRUE** 值等於數位1，而 **FALSE** 值等於數位0。</span><span class="sxs-lookup"><span data-stu-id="71325-129">The value **TRUE** is equivalent to the number 1, and the value **FALSE** is equivalent to the number 0.</span></span> <span data-ttu-id="71325-130">下列範例是比較布林值與 **TRUE** 或 **FALSE** 值的查詢。</span><span class="sxs-lookup"><span data-stu-id="71325-130">The following examples are of queries that compare a Boolean value against the values **TRUE** or **FALSE**.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp = 1
SELECT * FROM MyClass WHERE BoolProp = TRUE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
SELECT * FROM MyClass WHERE BoolProp = 0
SELECT * FROM MyClass WHERE BoolProp = FALSE
SELECT * FROM MyClass WHERE BoolProp != 1
SELECT * FROM MyClass WHERE BoolProp != FALSE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
```



<span data-ttu-id="71325-131">下列範例是嘗試使用無效運算元的無效查詢。</span><span class="sxs-lookup"><span data-stu-id="71325-131">The following examples are of invalid queries that attempt to use invalid operands.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



<span data-ttu-id="71325-132">您可以使用邏輯運算子和括弧子運算式，在 WHERE 子句中結合多個屬性、運算子和常數群組。</span><span class="sxs-lookup"><span data-stu-id="71325-132">Multiple groups of properties, operators, and constants can be combined in a WHERE clause using logical operators and parenthetical subexpressions.</span></span> <span data-ttu-id="71325-133">每個群組都必須與 AND、OR 或 NOT [運算子](wql-operators.md) 聯結，如下列查詢所示。</span><span class="sxs-lookup"><span data-stu-id="71325-133">Each group must be joined with the AND, OR, or NOT [operators](wql-operators.md) as is shown in the following queries.</span></span> <span data-ttu-id="71325-134">第一個查詢會使用設定為 C 或 D 的 **Name** 屬性，來抓取 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)類別的所有實例：</span><span class="sxs-lookup"><span data-stu-id="71325-134">The first query retrieves all instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class with the **Name** property set to either C or D:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



<span data-ttu-id="71325-135">第二個查詢只有在有特定數量的可用空間，且具有 NTFS 檔案系統時，才會取得名為 "C：" 或 "D：" 的磁片：</span><span class="sxs-lookup"><span data-stu-id="71325-135">The second query retrieves disks named "C:" or "D:" only if they have a certain amount of free space remaining and have NTFS file systems:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



<span data-ttu-id="71325-136">此範例顯示使用 WHERE 子句的架構查詢。</span><span class="sxs-lookup"><span data-stu-id="71325-136">This example shows a schema query using the WHERE clause.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



<span data-ttu-id="71325-137">類別中繼類別會將 \_ 此識別為架構查詢，呼叫此屬性的屬性會 \_ \_ 識別查詢的目標類別，而[ISA 運算子](isa-operator-for-schema-queries.md)會要求目標類別之子類別的定義。</span><span class="sxs-lookup"><span data-stu-id="71325-137">The class meta\_class identifies this as a schema query, the property called \_\_this identifies the target class of the query and the [ISA operator](isa-operator-for-schema-queries.md) requests definitions for the subclasses of the target class.</span></span> <span data-ttu-id="71325-138">因此，上述查詢會傳回 myClassName 類別的定義和其所有子類別的定義。</span><span class="sxs-lookup"><span data-stu-id="71325-138">Therefore, the preceding query returns the definition for the myClassName class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="71325-139">下列範例是使用 [語句 associators of](associators-of-statement.md) 搭配 WHERE 的資料查詢：</span><span class="sxs-lookup"><span data-stu-id="71325-139">The following example is a data query using the [ASSOCIATORS OF statement](associators-of-statement.md) with WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



<span data-ttu-id="71325-140">下一個範例顯示使用 ASSOCIATORS OF 和 WHERE 的架構查詢：</span><span class="sxs-lookup"><span data-stu-id="71325-140">The next example shows a schema query using ASSOCIATORS OF and WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="71325-141">下列範例是使用 [語句參考](references-of-statement.md) 和 WHERE 的資料查詢：</span><span class="sxs-lookup"><span data-stu-id="71325-141">The following example is a data query using the [REFERENCES OF statement](references-of-statement.md) and WHERE:</span></span>


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



<span data-ttu-id="71325-142">最後一個範例是使用的參考和位置的架構查詢：</span><span class="sxs-lookup"><span data-stu-id="71325-142">This last example is a schema query using REFERENCES OF and WHERE:</span></span>


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="71325-143">除了 WMI [DATETIME](date-and-time-format.md) 格式之外，WQL WHERE 子句還支援數個其他的日期和時間格式：</span><span class="sxs-lookup"><span data-stu-id="71325-143">In addition to the WMI [DATETIME](date-and-time-format.md) format, the WQL WHERE clause supports several other date and time formats:</span></span>

-   [<span data-ttu-id="71325-144">WQL-支援的日期格式</span><span class="sxs-lookup"><span data-stu-id="71325-144">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
-   [<span data-ttu-id="71325-145">WQL-支援的時間格式</span><span class="sxs-lookup"><span data-stu-id="71325-145">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)

 

 

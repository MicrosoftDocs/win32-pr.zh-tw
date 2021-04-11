---
description: 架構關聯查詢使用與資料關聯查詢中所使用的相同語句：的 ASSOCIATORS OF 和參考。
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: 架構關聯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0c3b753bf4657c66a635319bab7dbe435a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194699"
---
# <a name="schema-associations"></a><span data-ttu-id="7453a-103">架構關聯</span><span class="sxs-lookup"><span data-stu-id="7453a-103">Schema Associations</span></span>

<span data-ttu-id="7453a-104">架構關聯查詢使用與資料關聯查詢中所使用的相同語句：的 ASSOCIATORS OF 和參考。</span><span class="sxs-lookup"><span data-stu-id="7453a-104">Schema association queries use the same statements as are used in data association queries: ASSOCIATORS OF and REFERENCES OF.</span></span> <span data-ttu-id="7453a-105">不過，使用資料關聯查詢時，會傳回類別實例，並使用架構關聯查詢來傳回可參與關聯關聯性的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="7453a-105">However, with data association queries, class instances are returned, and with schema association queries, names of classes that can participate in association relationships are returned.</span></span> <span data-ttu-id="7453a-106">例如，使用架構查詢來尋找參考來源類別的架構中定義的所有關聯類別。</span><span class="sxs-lookup"><span data-stu-id="7453a-106">For example, use a schema query to find all of the association classes defined in the schema that reference a source class.</span></span>

<span data-ttu-id="7453a-107">架構關聯查詢的 ASSOCIATORS OF 和語句參考的語法，與下列例外狀況的資料關聯查詢相同：</span><span class="sxs-lookup"><span data-stu-id="7453a-107">The syntax for the ASSOCIATORS OF and REFERENCES OF statements is the same for schema association queries as it is for data association queries with the following exceptions:</span></span>

-   <span data-ttu-id="7453a-108">來源物件是類別，而不是實例。</span><span class="sxs-lookup"><span data-stu-id="7453a-108">The source object is a class rather than an instance.</span></span>
-   <span data-ttu-id="7453a-109">還有一個額外的關鍵字 **SchemaOnly**，它會將查詢識別為套用至架構，而不是資料。</span><span class="sxs-lookup"><span data-stu-id="7453a-109">There is an additional keyword, **SchemaOnly**, which identifies the query as applying to a schema rather than to data.</span></span>
-   <span data-ttu-id="7453a-110">**ClassDefsOnly** 關鍵字無效。</span><span class="sxs-lookup"><span data-stu-id="7453a-110">The **ClassDefsOnly** keyword is not valid.</span></span>

<span data-ttu-id="7453a-111">下列範例顯示架構查詢的語句 ASSOCIATORS OF 完整語法。</span><span class="sxs-lookup"><span data-stu-id="7453a-111">The following example shows the complete syntax of the ASSOCIATORS OF statement for a schema query.</span></span> <span data-ttu-id="7453a-112">如需詳細的語法，請參閱 [語句 associators of](associators-of-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="7453a-112">For detailed syntax, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>


```sql
ASSOCIATORS OF {SourceClass} WHERE 
    AssocClass = AssocClassName
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
    SchemaOnly
```



<span data-ttu-id="7453a-113">下列範例顯示的查詢會傳回 **通訊協定** 和 **驅動程式** 類別，這是兩個參考來源類別的類別。</span><span class="sxs-lookup"><span data-stu-id="7453a-113">The following example shows a query that returns the **Protocol** and **Driver** classes, the two classes that refer to the source class.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



<span data-ttu-id="7453a-114">下列查詢只會傳回 **驅動程式** 類別，因為 **AssocClass** 關鍵字所放置的限制。</span><span class="sxs-lookup"><span data-stu-id="7453a-114">The following query returns only the **Driver** class because of the restriction placed by the **AssocClass** keyword.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



<span data-ttu-id="7453a-115">架構查詢語句參考的完整語法如下所示。</span><span class="sxs-lookup"><span data-stu-id="7453a-115">The complete syntax of the REFERENCES OF statement for a schema query is as follows.</span></span> <span data-ttu-id="7453a-116">如需詳細的語法，請參閱 [語句的參考](references-of-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="7453a-116">For detailed syntax, see [REFERENCES OF Statement](references-of-statement.md).</span></span>


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> <span data-ttu-id="7453a-117">架構關聯查詢可能會傳回重複的物件。</span><span class="sxs-lookup"><span data-stu-id="7453a-117">Schema association queries may return duplicate objects.</span></span>

 

<span data-ttu-id="7453a-118">例如，下列查詢會在列舉 **根 \\ cimv2** 命名空間中的類別時，傳回 CIM 的「執行程式類型」多次。 [**\_**](/windows/desktop/CIMWin32Prov/cim-computersystem)</span><span class="sxs-lookup"><span data-stu-id="7453a-118">For example, the following query will return the class [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) several times when enumerating classes in the **root\\cimv2** namespace.</span></span>


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 

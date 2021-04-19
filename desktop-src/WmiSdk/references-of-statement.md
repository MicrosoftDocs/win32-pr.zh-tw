---
description: 語句的參考會捕獲參考特定來源實例的所有關聯實例。
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: 語句的參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979762"
---
# <a name="references-of-statement"></a><span data-ttu-id="20528-103">語句的參考</span><span class="sxs-lookup"><span data-stu-id="20528-103">REFERENCES OF Statement</span></span>

<span data-ttu-id="20528-104">語句的參考會捕獲參考特定來源實例的所有關聯實例。</span><span class="sxs-lookup"><span data-stu-id="20528-104">The REFERENCES OF statement retrieves all association instances that refer to a particular source instance.</span></span> <span data-ttu-id="20528-105">語句的參考與語法中的語句 ASSOCIATORS OF 類似。</span><span class="sxs-lookup"><span data-stu-id="20528-105">The REFERENCES OF statement is similar to the ASSOCIATORS OF statement in its syntax.</span></span> <span data-ttu-id="20528-106">不過，它不會取出端點實例，而是會抓取中間的關聯實例。</span><span class="sxs-lookup"><span data-stu-id="20528-106">However, rather than retrieving endpoint instances, it retrieves the intervening association instances.</span></span>

<span data-ttu-id="20528-107">WHERE 子句的參考可以包含下列一或多個預先定義的關鍵字和其值：</span><span class="sxs-lookup"><span data-stu-id="20528-107">The REFERENCES OF WHERE clause can include one or more of the following predefined keywords and their values:</span></span>


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



<span data-ttu-id="20528-108">若要指定來源物件，請使用任何有效的物件路徑進行 SourceObject。</span><span class="sxs-lookup"><span data-stu-id="20528-108">To specify a source object, use any valid object path for SourceObject.</span></span> <span data-ttu-id="20528-109">如同 SELECT 語句，WHERE 子句是選擇性的，並且用來進一步定義查詢。</span><span class="sxs-lookup"><span data-stu-id="20528-109">As with the SELECT statement, the WHERE clause is optional and is used to further define the query.</span></span> <span data-ttu-id="20528-110">也就是說，下列語句完全有效：</span><span class="sxs-lookup"><span data-stu-id="20528-110">That is, the following statement is perfectly valid:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



<span data-ttu-id="20528-111">**ClassDefsOnly** 關鍵字表示語句會傳回類別定義物件的結果集，而非關聯類別的實際實例。</span><span class="sxs-lookup"><span data-stu-id="20528-111">The **ClassDefsOnly** keyword indicates that the statement returns a result set of class definition objects rather than actual instances of the association classes.</span></span> <span data-ttu-id="20528-112">這些物件包含參考來源物件之實例所屬類別的定義。</span><span class="sxs-lookup"><span data-stu-id="20528-112">These objects contain definitions of classes to which the instances that reference the source object belong.</span></span> <span data-ttu-id="20528-113">例如，下列語句會傳回 **AdapterDriver** 和 **AdapterProtocol** 類別的定義：</span><span class="sxs-lookup"><span data-stu-id="20528-113">For example, the following statement returns definitions for the **AdapterDriver** and **AdapterProtocol** classes:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



<span data-ttu-id="20528-114">**RequiredQualifier** 關鍵字指出傳回的關聯物件必須包含指定的限定詞。</span><span class="sxs-lookup"><span data-stu-id="20528-114">The **RequiredQualifier** keyword indicates that the returned association objects must include the specified qualifier.</span></span> <span data-ttu-id="20528-115">**RequiredQualifier** 關鍵字可以用來在結果集中包含關聯的特定實例。</span><span class="sxs-lookup"><span data-stu-id="20528-115">The **RequiredQualifier** keyword can be used to include particular instances of associations in the result set.</span></span> <span data-ttu-id="20528-116">例如，下列語句會傳回關聯實例，其中包含名為 **AdapterTag** 的辨識符號：</span><span class="sxs-lookup"><span data-stu-id="20528-116">For example, the following statement returns association instances that include a qualifier called **AdapterTag**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



<span data-ttu-id="20528-117">**ResultClass** 關鍵字指出傳回的關聯物件必須屬於或衍生自指定的類別。</span><span class="sxs-lookup"><span data-stu-id="20528-117">The **ResultClass** keyword indicates that the returned association objects must belong to or be derived from the specified class.</span></span> <span data-ttu-id="20528-118">例如，下列語句會傳回 **AdapterDriver** 類別或 **AdapterDriver** 子類別的關聯：</span><span class="sxs-lookup"><span data-stu-id="20528-118">For example, the following statement returns associations of the **AdapterDriver** class or subclasses of **AdapterDriver**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



<span data-ttu-id="20528-119">**ClassDefsOnly** 和 **ResultClass** 關鍵字是互斥的。</span><span class="sxs-lookup"><span data-stu-id="20528-119">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="20528-120">一起使用它們會導致不正確查詢錯誤。</span><span class="sxs-lookup"><span data-stu-id="20528-120">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="20528-121">**Role** 關鍵字表示傳回的關聯只是來源物件扮演特定角色的關聯。</span><span class="sxs-lookup"><span data-stu-id="20528-121">The **Role** keyword indicates that the returned associations are only those in which the source object plays a particular role.</span></span> <span data-ttu-id="20528-122">角色是由指定的屬性所定義，即 [ref](references.md)類型的參考屬性。 **Role** 關鍵字適用于在某些情況下，某些物件在某些情況下可扮演某個角色的關聯性，以及其他在階層式關聯中的角色。</span><span class="sxs-lookup"><span data-stu-id="20528-122">The role is defined by the specified property, a reference property of type [ref](references.md). The **Role** keyword is useful in associations where a certain object can play one role in some cases and another role in others, such as in hierarchical associations.</span></span> <span data-ttu-id="20528-123">例如， **role** 關鍵字可以用來抓取來源物件扮演父系角色的所有關聯。</span><span class="sxs-lookup"><span data-stu-id="20528-123">The **Role** keyword can be used to retrieve all of the associations in which the source object plays the role of parent, for example.</span></span> <span data-ttu-id="20528-124">下列語句說明用來抓取關聯的語法，此關聯具有將來源物件參考為父系的 **父** 屬性：</span><span class="sxs-lookup"><span data-stu-id="20528-124">The following statement illustrates the syntax for retrieving associations that have a **parent** property referencing the source object as the parent:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> <span data-ttu-id="20528-125">複雜的查詢不能使用 "And" 或 "Or" 來分隔 ASSOCIATORS OF 和語句參考的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="20528-125">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and REFERENCES OF statements.</span></span> <span data-ttu-id="20528-126">此外，等號是唯一可搭配這些查詢中的關鍵字使用的有效運算子。</span><span class="sxs-lookup"><span data-stu-id="20528-126">Furthermore, the equal sign is the only valid operator that can be used with the keywords in these queries.</span></span> <span data-ttu-id="20528-127">例如，以下是有效的查詢：</span><span class="sxs-lookup"><span data-stu-id="20528-127">For example, the following query is valid:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> <span data-ttu-id="20528-128">接下來的範例是不正確。</span><span class="sxs-lookup"><span data-stu-id="20528-128">The next examples are not valid.</span></span> <span data-ttu-id="20528-129">第一個範例不會使用等號，而第二個範例會錯誤地嘗試使用 **和** 關鍵字：</span><span class="sxs-lookup"><span data-stu-id="20528-129">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 




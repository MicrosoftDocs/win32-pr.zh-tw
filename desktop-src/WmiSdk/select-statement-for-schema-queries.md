---
description: 架構資料查詢會使用 SELECT 語句，其語法與資料查詢類似。
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: 架構查詢的 SELECT 語句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9f3f9ae8cc11a94d4d868e36af56ee7dffd2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194698"
---
# <a name="select-statement-for-schema-queries"></a><span data-ttu-id="7c560-103">架構查詢的 SELECT 語句</span><span class="sxs-lookup"><span data-stu-id="7c560-103">SELECT Statement for Schema Queries</span></span>

<span data-ttu-id="7c560-104">架構資料查詢會使用 SELECT 語句，其語法與 [資料查詢](select-statement-for-data-queries.md)類似。</span><span class="sxs-lookup"><span data-stu-id="7c560-104">Schema data queries use the SELECT statement with a syntax similar to that for [data queries](select-statement-for-data-queries.md).</span></span> <span data-ttu-id="7c560-105">差別在於使用稱為「中繼類別」的特殊類別 \_ ，這會將查詢識別為架構查詢。</span><span class="sxs-lookup"><span data-stu-id="7c560-105">The difference is the use of a special class called "meta\_class", which identifies the query as a schema query.</span></span>

<span data-ttu-id="7c560-106">下列範例會要求目前命名空間內的所有類別定義。</span><span class="sxs-lookup"><span data-stu-id="7c560-106">The following example requests all class definitions that are within the current namespace.</span></span>


```sql
SELECT * FROM meta_class
```



<span data-ttu-id="7c560-107">架構查詢僅支援 " \* "。</span><span class="sxs-lookup"><span data-stu-id="7c560-107">Schema queries only support "\*".</span></span> <span data-ttu-id="7c560-108">為了縮小傳回的定義範圍，提供者可以加入指定特定類別的 WHERE 子句。</span><span class="sxs-lookup"><span data-stu-id="7c560-108">To narrow the scope of the definitions returned, a provider can add a WHERE clause that specifies a particular class.</span></span>

<span data-ttu-id="7c560-109">下列範例示範如何加入 WHERE 子句來指定特定類別。</span><span class="sxs-lookup"><span data-stu-id="7c560-109">The following example shows how to add a WHERE clause to specify a particular class.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



<span data-ttu-id="7c560-110">**\_ \_ 所謂的** 特殊屬性會識別架構查詢的目標類別。</span><span class="sxs-lookup"><span data-stu-id="7c560-110">The special property called **\_\_this** identifies the target class for a schema query.</span></span> <span data-ttu-id="7c560-111">請注意，ISA 運算子必須搭配 **\_ \_ 這個** 屬性使用，才能要求目標類別子類別的定義。</span><span class="sxs-lookup"><span data-stu-id="7c560-111">Note that the ISA operator must be used with the **\_\_this** property to request definitions for the subclasses of the target class.</span></span> <span data-ttu-id="7c560-112">上述查詢會傳回 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的定義和其所有子類別的定義。</span><span class="sxs-lookup"><span data-stu-id="7c560-112">The preceding query returns the definition for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="7c560-113">下列範例顯示如何使用 **\_ \_ 類別** 系統屬性來要求單一類別的類別定義。</span><span class="sxs-lookup"><span data-stu-id="7c560-113">The following example shows how to request a class definition for a single class by using the **\_\_Class** system property.</span></span>


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



<span data-ttu-id="7c560-114">此查詢相當於呼叫 [**iwbemservices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 方法，並將物件路徑參數設定為 "Win32 \_ LogicalDisk"。</span><span class="sxs-lookup"><span data-stu-id="7c560-114">This query is equivalent to calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or the [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) method with the object path parameter set to "Win32\_LogicalDisk".</span></span>

<span data-ttu-id="7c560-115">下列 VBScript 程式碼範例會捕獲最上層 WMI 類別的所有子類別。</span><span class="sxs-lookup"><span data-stu-id="7c560-115">The following VBScript code sample retrieves all child classes of a top level WMI class.</span></span> <span data-ttu-id="7c560-116">\_ \_ 時代 WMI 系統屬性會保存類別衍生自最上層類別的名稱，您可以使用此名稱來取得衍生自最上層類別之命名空間中的所有類別，包括該類別。</span><span class="sxs-lookup"><span data-stu-id="7c560-116">The \_\_Dynasty WMI system property holds the name of the top-level class from which a class is derived, which you can use to retrieve all classes in a namespace derived from a top level class, including that class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Dynasty = 'Win32_CurrentTime'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="7c560-117">下列 VBScript 會抓取 WMI 類別的直屬子類別。</span><span class="sxs-lookup"><span data-stu-id="7c560-117">The following VBScript retrieves an immediate child classes for a WMI class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Superclass = 'Cim_DataFile'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="7c560-118">下列 VBScript 會抓取最上層類別。</span><span class="sxs-lookup"><span data-stu-id="7c560-118">The following VBScript retrieves top level classes.</span></span> <span data-ttu-id="7c560-119">針對 WMI 命名空間中的所有最上層類別， \_ \_ 超級類別系統屬性為 Null。</span><span class="sxs-lookup"><span data-stu-id="7c560-119">For all the top level classes in a WMI namespace, the \_\_Superclass system property is Null.</span></span> <span data-ttu-id="7c560-120">因此，您可以藉由搜尋 Null 超類別來取得最上層類別。</span><span class="sxs-lookup"><span data-stu-id="7c560-120">Therefore, it is possible to retrieve the top level classes by searching for a Null superclass.</span></span>


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 

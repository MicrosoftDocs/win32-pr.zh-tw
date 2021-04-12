---
description: 下列主題描述如何取得動態建立之原始或格式化資料物件的線上程式設計檔。
ms.assetid: B3CD7E2C-9FCF-42FB-8713-01A696E905B0
ms.tgt_platform: multiple
title: 取得原始和格式化效能資料物件的檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ab9cf66aa4536da25102511fdcbcab6bdd5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320672"
---
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a><span data-ttu-id="63b23-103">取得原始和格式化效能資料物件的檔</span><span class="sxs-lookup"><span data-stu-id="63b23-103">Retrieving Documentation for Raw and Formatted Performance Data Objects</span></span>

<span data-ttu-id="63b23-104">下列主題描述如何取得動態建立之原始或格式化資料物件的線上程式設計檔。</span><span class="sxs-lookup"><span data-stu-id="63b23-104">The following topic describes how to retrieve the on-line programming documentation for a dynamically-created raw or formatted data object.</span></span>

<span data-ttu-id="63b23-105">WMI 包含許多可追蹤效能的物件。</span><span class="sxs-lookup"><span data-stu-id="63b23-105">WMI contains a number of objects that track performance.</span></span> <span data-ttu-id="63b23-106">從 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 衍生的類別包含原始或「未經處理」效能資料，而且 [效能計數器提供者](performance-counter-provider.md)支援這些資料。</span><span class="sxs-lookup"><span data-stu-id="63b23-106">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contain raw, or "uncooked" performance data, and are supported by the [Performance Counter provider](performance-counter-provider.md).</span></span> <span data-ttu-id="63b23-107">相反地，從 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 衍生的類別會包含 "處理後" 或格式化的資料，並受到 [格式化效能 Data Provider](formatted-performance-data-provider.md)的支援。</span><span class="sxs-lookup"><span data-stu-id="63b23-107">In contrast, classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contain "cooked", or formatted data, and are supported by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="63b23-108">不過，這兩個提供者都支援許多動態建立的子類別。</span><span class="sxs-lookup"><span data-stu-id="63b23-108">However, both providers support a number of dynamically-created child classes.</span></span> <span data-ttu-id="63b23-109">由於屬性是在執行時間加入，因此這些類別可能包含未記載的屬性。</span><span class="sxs-lookup"><span data-stu-id="63b23-109">Because the properties are added at run-time, these classes may contain undocumented properties.</span></span> <span data-ttu-id="63b23-110">您可以使用下列程式碼來識別特定動態建立類別所擁有的屬性。</span><span class="sxs-lookup"><span data-stu-id="63b23-110">You can use the following code to identify what properties a given dynamically-created class has.</span></span>

<span data-ttu-id="63b23-111">**取出動態建立之類別的描述**</span><span class="sxs-lookup"><span data-stu-id="63b23-111">**To retrieve a description of a dynamically-created class**</span></span>

1.  <span data-ttu-id="63b23-112">建立專案的實例，並將修改過的辨識符號設定為 true。</span><span class="sxs-lookup"><span data-stu-id="63b23-112">Create an instance of the item, and set the amended qualifier to true.</span></span>

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  <span data-ttu-id="63b23-113">取出類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="63b23-113">Retrieve the properties of the class.</span></span>

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  <span data-ttu-id="63b23-114">顯示內容。</span><span class="sxs-lookup"><span data-stu-id="63b23-114">Display the properties.</span></span>

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

<span data-ttu-id="63b23-115">下列程式碼會取得指定之 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 物件的屬性描述。</span><span class="sxs-lookup"><span data-stu-id="63b23-115">The following code retrieves the property descriptions for the specified [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) object.</span></span>


```PowerShell
$osClass = New-Object System.Management.ManagementClass Win32_PerfFormattedData_APPPOOLCountersProvider_APPPOOLWAS  
$osClass.Options.UseAmendedQualifiers = $true  
  
# Get the Properties in the class  
$properties = $osClass.Properties  
"This class has {0} properties as follows:" -f $properties.count  
  
  
# display the Property name, description, type, qualifiers and instance values  
  
foreach ($property in $properties) {  
"Property Name: {0}" -f $property.Name  
"Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
"Type:          {0}" -f $property.Type  
"-------"  
}
```



 

 

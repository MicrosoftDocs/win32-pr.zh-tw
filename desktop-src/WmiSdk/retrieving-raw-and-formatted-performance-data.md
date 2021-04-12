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
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a>取得原始和格式化效能資料物件的檔

下列主題描述如何取得動態建立之原始或格式化資料物件的線上程式設計檔。

WMI 包含許多可追蹤效能的物件。 從 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 衍生的類別包含原始或「未經處理」效能資料，而且 [效能計數器提供者](performance-counter-provider.md)支援這些資料。 相反地，從 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 衍生的類別會包含 "處理後" 或格式化的資料，並受到 [格式化效能 Data Provider](formatted-performance-data-provider.md)的支援。

不過，這兩個提供者都支援許多動態建立的子類別。 由於屬性是在執行時間加入，因此這些類別可能包含未記載的屬性。 您可以使用下列程式碼來識別特定動態建立類別所擁有的屬性。

**取出動態建立之類別的描述**

1.  建立專案的實例，並將修改過的辨識符號設定為 true。

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  取出類別的屬性。

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  顯示內容。

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

下列程式碼會取得指定之 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 物件的屬性描述。


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



 

 

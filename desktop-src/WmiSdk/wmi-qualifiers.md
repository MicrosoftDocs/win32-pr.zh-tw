---
description: WMI 有數種類型的類別和屬性限定詞。 限定詞也可以有修改的類別。
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: WMI 限定詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b14dc8f1f73571fc2c449e55c30034f86c2453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192049"
---
# <a name="wmi-qualifiers"></a>WMI 限定詞

WMI 有數種類型的類別和屬性 [*限定詞*](gloss-q.md)。 限定詞也可以 [*有修改的*](gloss-f.md)類別。 以下是在 WMI 中使用的限定詞和類別類型。

每個辨識符號的名稱都會顯示其資料類型，以及是否可以將限定詞套用至類別、實例、屬性或方法的指標。 針對在 [中繼限定詞](meta-qualifiers.md)) 下討論的 **關聯** (，有一個隱含的使用規則，也就是 meta 限定詞也必須存在。 例如， **匯總** 限定詞的隱含使用規則是， **關聯** 限定詞也必須存在。



| 限定詞類型                              | Description                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [元](meta-qualifiers.md)                 | 藉由闡明類別或屬性宣告的實際使用方式，來改善中繼結構的定義。                          |
| [選擇性](optional-qualifiers.md)         | 解決所有符合 CIM 規範的情況下不常見的情況。                                                                 |
| [限定詞類別](qualifier-flavors.md)  | 提供限定詞的詳細資訊，例如衍生類別或實例是否可以覆寫辨識符號的原始值。 |
| [標準](standard-qualifiers.md)         | 支援所有 CIM 相容的實作為必須處理的描述。                                                         |
| [WMI 特定](wmi-specific-qualifiers.md) | 描述 WMI 特定的限定詞，例如效能計數器類別限定詞。                                                   |



 

如需將限定詞套用至 WMI 類別的詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md)。 若要瞭解如何檢查現有 WMI 類別的限定詞，請參閱下列範例程式碼。

## <a name="example"></a>範例

下列來自 [TechNet 資源庫](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7)的 PowerShell 程式碼說明如何從 WMI 類別取出限定詞。


```PowerShell
Function Get-WMIClassesWithQualifiers 
{ 
 Param([string]$qualifier = "dynamic", 
  [string]$namespace = "root\cimv2") 
 $classes = Gwmi -list -namespace $namespace 
 foreach($class in $classes) 
 { 
  $query = "select * from meta_class where __this isa ""$($class.name)"" " 
  $a = gwmi -Query $query -Namespace $namespace |  
  select -Property __class, qualifiers 
   if($a.qualifiers | % { $_ | ? { $_.name -match "$qualifier" }}) 
    { $a.__class } 
  } #end foreach $class 
} 
```



 

 




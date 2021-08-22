---
description: MOF 參考關鍵字字組描述物件路徑，並對應至 VT \_ BSTR Automation 型別。
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: " (WMI) 的參考"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea004a4d0a1cf160d387b07e9c9d7ac85eaaaf21851bd315ecd1bb4ba6f2b49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050456"
---
# <a name="references-wmi"></a> (WMI) 的參考

MOF **參考** 關鍵字字組描述物件路徑，並對應至 VT \_ BSTR Automation 型別。 物件路徑可以是伺服器和命名空間的完整路徑，或相同命名空間中另一個物件的相對路徑。 您可以使用 **ref** 關鍵字來將兩個或多個類別連結在一起。 WMI 支援兩種類型的物件路徑，用來定義 WMI 內的一般或特定路徑。

**參考** 關鍵字的主要目的是要減少完全存在於 WMI 儲存機制中的物件之間的傳輸時間和編碼。 您也可以使用 **ref** 關鍵字來建立兩個類別之間的關聯。 如需詳細資訊，請參閱宣告 [關聯類別](declaring-an-association-class.md)。 如果參考的專案位於相同的 MOF 檔案內，請使用別名來初始化 **參考** 值。 如需詳細資訊，請參閱 [建立別名](creating-an-alias.md)。

> [!Note]  
> 當 **ref** 關鍵字套用至索引鍵屬性時，您可以透過物件字串值來區分物件參考，而不是以取值的值來區分。

 

MOF 支援弱式型別和強型別物件路徑的概念。 弱式類型的物件路徑指向未指定類別的物件，並使用 **ref** 關鍵字搭配 [object](object.md) 關鍵字。 強型別物件指向特定類別的物件，並使用 **ref** 搭配類別名稱。 下列範例說明可指向任何類別或類別實例的弱式型別 **RefToAnyClass** 參考，以及只能指向 **ClassX** 類別或實例的 **RefToClassX** 參考：

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

下列範例說明兩個實例，以及參考先前實例的關聯物件：

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 




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
# <a name="mof-arrays"></a>MOF 陣列

陣列是具有相同資料類型之資料值的索引清單，您可以參考這些資料值。 除了字串和數值陣列，MOF 還支援内嵌物件和參考的陣列。

下列規則會定義 MOF 陣列：

-   屬性識別碼之後所用的括弧會指定類別定義中的陣列。

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   所有陣列都必須是一維的。
-   陣列可無限制或具有明確的大小。

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    WMI 會將系結和無限制的陣列實作為 **SAFEARRAY** 結構，讓 WMI 在執行時間改變數組維度。 當您宣告明確大小的陣列時，WMI 會將大小儲存為辨識符號，並將大小視為建議的最大大小。 不過，WMI 可以視需要擴充大小。 變更明確的大小不會影響實際的資料。

-   陣列的初始化方式是在逗號分隔清單中指定適當類型的值。

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   參考的陣列會宣告為物件路徑字串的陣列。

    宣告物件路徑字串時，請勿在物件路徑的元素之間放置空白字元。 下列範例說明如何宣告物件路徑參考。

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

-   您可以使用陣列做為方法的參數，但不能做為輸入或輸入輸出參數的傳回值。
-   陣列中的所有元素都會建立為相同類型的值。

    如果陣列的元素屬於 **物件** 類型，則您可以將任何類型的物件放在陣列中。 另一方面，如果您宣告特定類型的物件，則 WMI 只允許該類別的物件或陣列中的子類別。 下列範例顯示包含使用 **物件** 類型的陣列宣告。

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

 

 




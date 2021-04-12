---
description: 如同受控物件格式 (MOF) 的許多其他技術，將限定詞套用至您的程式碼是相當簡單的程式。
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: 套用辨識符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695827"
---
# <a name="applying-a-qualifier"></a>套用辨識符號

如同受控物件格式 (MOF) 的許多其他技術，將限定詞套用至您的程式碼是相當簡單的程式。

唯一真正的挑戰是 WMI 強制執行之命名慣例的下列限制：

-   辨識符號可以描述類別、實例、屬性、方法或方法參數。
-   辨識符號名稱不能有開頭或結尾的底線。
-   限定詞名稱的開頭不能是數位。
-   辨識符號名稱不能包含特殊字元，例如 & \* @！ ~ \\ /.
-   所有限定詞名稱都不區分大小寫。
-   您無法重新定義標準的 WMI 限定詞或任何在「DMTF CIM」規格中描述的限定詞。
-   未明確宣告辨識符號類型。

    如果您未宣告辨識符號類型，WMI 會將類型假設為布林值 **TRUE**。 否則，會以您宣告的辨識符號值為基礎的 WMI 類型限定詞。

-   建立您自己的限定詞時，您應該在您的架構名稱之前加上您的辨識符號名稱。

    這項規則的目的是要避免與新的限定詞混淆。

-   您可以建立同質的限定詞陣列。

    下列程式碼範例示範如何使用以大括弧括住的值來指定限定詞陣列。

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   WMI 不支援未列在參考中的 automation 類型，例如 VT \_ Null。 如需詳細資訊，請參閱 [MOF 資料類型](mof-data-types.md)。

下列程式可協助您使用 c + +，將限定詞加入至屬性。

**使用 c + + 套用限定詞**

-   將限定詞套用至 [**IWbemQualifierSet：:P**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) ui 方法的呼叫。

    您可以使用 [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) 的其他方法來取出或刪除現有的限定詞。

下列程式可協助您將限定詞套用至 MOF 檔案。

**使用 MOF 描述具有辨識符號的關鍵字或識別碼**

-   在限定詞所描述的關鍵字或識別碼之前，將限定詞放在括弧中。

    下列程式碼範例顯示如何使用限定詞。

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    下列範例說明適當的限定詞位置。

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 




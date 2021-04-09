---
description: 關聯類別是一種特殊類型的類別，可定義兩個其他類別之間的關聯性。
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: 宣告關聯類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027236"
---
# <a name="declaring-an-association-class"></a>宣告關聯類別

關聯類別是一種特殊類型的類別，可定義兩個其他類別之間的關聯性。

下列程式描述如何使用 MOF 程式碼建立關聯類別。

**使用 MOF 程式碼建立關聯類別**

1.  將 **關聯** 限定詞指派給您的類別。

    雖然您可以使用關聯辨識符號來建立具有物件或類別參考的類別，但使用 **關聯** 辨識符號並不只會讓它清楚地指出您的類別是關聯類別，但最佳做法是確保您的類別會完整地做為關聯類別。

2.  在類別內建立兩個參考，描述您想要使用 **ref** 型別來建立關聯的兩個物件實例。

    參考會藉由包含物件的路徑，系結關聯中的兩個物件。 雖然並非必要，但也請使用參考屬性做為索引鍵屬性。

    雖然您可以建立完整或命名空間相關的參考，但 WMI 對於跨命名空間的參考只有有限的支援。 具體而言，只有靜態定義的物件可以跨命名空間界限彼此參考;動態支援的物件無法彼此參考。

    如有必要，請使用 **HasClassRef** 和 **Classref** 限定詞搭配 **物件 ref** 類型，以參考類別。

    WMI 支援對實例使用一個 **ref** 參考點，而另一個 **物件** 參考指向類別。 在此情況下，您的關聯類別會描述將實例系結至類別的關聯。

    下列程式碼範例說明搭配 **物件** 類型使用 **HasClassRef** 和 **Classref** 的語法。

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    在上述範例中， **ep1** 參考可指向 **MyEndpoint** 類別或 **OtherContainer** 類別的類別定義。 請注意，雖然您必須弱型別參考類別，但您無法將 **Classref** 限定詞本身的型別弱：這麼做會大幅降低 WMI 查詢引擎的效率。 弱式類型是使用 **object** 關鍵字和 **ref** 資料類型來建立可包含任何資料類型的參考。 若要成功使用 **HasClassRef**，您必須設定相關的限定詞類別，以傳播至所有實例和子類別。

3.  視需要建立任何其他屬性。

    下列程式碼範例顯示 WMI 目前不支援具有少於或等於兩個參考屬性的關聯類別。

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  完成時，使用 MOF 編譯器編譯您的 MOF 程式碼。

    如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

步驟3中的程式碼範例會定義 **MyAssocClass** 關聯類別。 **MyAssocClass** 類別會定義 **ClassX** 和 **一些優質** 之間的關聯性。 **PathToClassX** 和 **PathToClassY** 屬性包含要關聯之類別實例的物件路徑。 關鍵字 **ToInstance** 是數個類別旗標的其中一個，WMI 會定義這些旗標來提供使用限定詞的相關資訊。 **ToInstance** 關鍵字指出 WMI 應該將 **關聯** 辨識符號傳播至 association 類別的所有實例。 藉由檢查此實例限定詞，用戶端軟體可以判斷實例是否屬於關聯類別，而不需要取得類別定義來尋找 **關聯** 辨識符號。 如需詳細資訊，請參閱使用限定詞類別和[參考](references.md)[描述限定詞](describing-a-qualifier-with-a-qualifier-flavor.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 




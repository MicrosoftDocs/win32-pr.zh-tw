---
title: 編碼樣式慣例
description: 此範例系列使用編碼樣式慣例來協助清楚且一致。
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684273"
---
# <a name="coding-style-conventions"></a>編碼樣式慣例

此範例系列使用編碼樣式慣例來協助清楚且一致。 使用「匈牙利文」標記法慣例。 這些已成為 Win32 程式設計中常見的編碼作法。 其中包括變數前置詞標記法，可為變數名稱提供變數類型的建議。

下表列出常見的首碼。



| 前置詞 | 描述                         |
|--------|-------------------------------------|
| a      | Array                               |
| b      | BOOL (int)                           |
| c      | Char                                |
| Cb     | 位元組計數                      |
| 鉻     | 色彩參考值               |
| 殘雪     | X (短) 的計數                  |
| dw     | DWORD (不帶正負號的 long)                |
| f      | 旗標 (通常會有多個位值)  |
| fn     | 函式                            |
| G\_    | 全球                              |
| h      | Handle                              |
| i      | 整數                             |
| l      | long                                |
| lp     | Long 指標                        |
| m\_    | 類別的資料成員              |
| n      | Short 整數                           |
| p      | Pointer                             |
| s      | String                              |
| sz     | 以零結尾的字串              |
| tm     | 文字度量                         |
| u      | 不帶正負號的 int                        |
| ul     | 不帶正負號的 long (ULONG)                |
| w      | WORD (不帶正負號的短)                |
| x、y    | x、y 座標 (短)             |



 

這些通常會結合，如下所示。



| 前置片語合 | Description                                             |
|--------------------|---------------------------------------------------------|
| pszMyString        | 字串的指標。                                  |
| m \_ pszMyString     | 字串的指標，該字串為類別的資料成員。 |



 

下表列出其他慣例。



| 慣例       | Description                                              |
|------------------|----------------------------------------------------------|
| CMyClass         | C + + 類別名稱的前置詞 ' C '。                          |
| COMyObjectClass  | COM 物件類別名稱的前置詞 ' CO '。                  |
| CFMyClassFactory | COM class factory 名稱的前置詞 ' CF '。                 |
| IMyInterface     | COM 介面類別別名稱的前置詞 ' I '。                |
| CImpIMyInterface | COM 介面實類別的前置詞 ' CImpI '。 |



 

此範例系列中會使用批註標頭區塊的一些一致慣例，如下所示。

## <a name="file-header"></a>檔案標頭

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a>純文字批註區塊

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a>類別宣告標頭

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a>類別方法定義標頭

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a>Unexported 或區域函數

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a>匯出的函式定義標頭

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a>COM 介面聲明標頭

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a>COM 物件類別宣告標頭

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

所有這些批註區塊慣例都有一致的開始和結束權杖字串。 這項一致性支援以某種方式自動處理標頭。 例如，您可以撰寫 AWK 腳本，將函式標頭篩選成個別的文字檔，然後做為規格檔的基礎。 同樣地，Microsoft 開發人員網路開發程式庫 CD-ROM (目前提供的工具，就像是不支援的 AUTODUCK 公用程式一樣) 可以用來處理這些標頭中的批註區塊。

下表列出範例教學課程中所使用的開始和結束權杖字串。



| Token | 描述                      |
|-------|----------------------------------|
| /\*+  | 檔案標頭開始                |
| +\*/  | 檔案標頭結束                  |
| /\*-  | 純文字批註區塊標頭開始 |
| -\*/  | 純文字批註區塊標頭結束   |
| /\*C  | 類別標頭開始               |
| C\*/  | 類別標頭結束                 |
| /\*M  | 方法標頭開始              |
| M\*/  | 方法標頭結束                |
| /\*F  | 函式標頭開始            |
| F\*/  | 函式標頭結束              |
| /\*我  | 介面標頭開始           |
| 我\*/  | 介面標頭結束             |
| /\*輸出  | COM 物件類別標頭開始    |
| 輸出\*/  | COM 物件類別標頭結束      |



 

這些標頭也可以用來做為快速掃描原始程式檔的視覺提示。 如果您在編輯器中設定搜尋字串，然後「重複最後搜尋」來快速找出這些標頭，它們也能方便您快速取得某些來源位置。

例如，搜尋字串 "M + M" 會找到方法標頭的開頭，而 "M-M" 將會找出實際方法定義/執行程式碼的開頭。

 

 





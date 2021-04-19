---
description: 每個符合 DXSAS 的效果都必須定義一個具有全域語義的單一全域效果參數（最小值）。
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: 全域參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971936"
---
# <a name="global-parameter"></a>全域參數

每個符合 DXSAS 的效果都必須定義一個具有全域語義的單一全域效果參數（最小值）。 全域參數也可以使用一或多個選擇性批註。 語法如下：


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



其中：

-   VariableName 是使用者指定的 ASCII 文字字串變數名稱。
-   SasGlobal 是將此參數識別為 global DXSAS 參數的語義關鍵字。
-   SasVersion 是唯一需要的批註。
-   OptionalAnnotations 可包含下列各項：
    -   [SasEffectAuthor](#saseffectauthor)
    -   [SasEffectAuthoringSoftware](#saseffectauthoringsoftware)
    -   [SasEffectCategory](#saseffectcategory)
    -   [SasEffectCompany](#saseffectcompany)
    -   [SasEffectDescription](#saseffectdescription)
    -   [SasEffectHelp](#saseffecthelp)
    -   [SasEffectRevision](#saseffectrevision)

## <a name="sasversion"></a>SasVersion

唯一必要的注釋是 SasVersion。 其宣告如下：


```
int3 SasVersion = { major, minor, revision };
```



其中：

-   「主要」表示 DXSAS 的主要版本。 DXSAS 的主要版本可以包含所定義的一組語義和注釋的變更。 您可以新增和移除語義和注釋，而且通常不保證與先前版本的回溯相容性。
-   [次要] 表示 SAS 次要版本。 DXSAS 的次要版本可以包含新的語義或批註的加入。 此外，在 DXSAS 標準中，可以將語義和注釋標示為已淘汰。 主機應用程式仍然必須支援已被取代的語法和注釋，但是使用這類語義或批註時，可能會發出警告診斷。 次要版本可回溯相容于先前的版本。
-   修訂表示 DXSAS 修訂。 DXSAS 的修訂僅作為修正 bug、移除不明確和精簡標準的方法。 標準版的修訂與舊版的回溯相容性。

目前的版本為1.0.0。 此批註沒有預設值。

## <a name="saseffectauthor"></a>SasEffectAuthor

這會宣告建立效果的人員。 其宣告如下：


```
string SasEffectAuthor = "value";
```



其中 value 是識別效果作者的字串。 預設為空字串。

## <a name="saseffectauthoringsoftware"></a>SasEffectAuthoringSoftware

這會宣告此效果所撰寫的軟體。 其宣告如下：


```
string SasEffectAuthoringSoftware = "value";
```



其中 value 是識別效果撰寫軟體的字串。 預設為空字串。

## <a name="saseffectcategory"></a>SasEffectCategory

這會宣告效果類別目錄。 其宣告如下：


```
string SasEffectCategory = "value";
```



其中 value 是識別效果類別目錄的字串。 預設為空字串。 類別是透過類似路徑的值來表示，使用正斜線作為分隔符號。 效果只能屬於一個類別，因為沒有任何語法可在單一 SasEffectCategory 值內的多個路徑中表示包含。 主應用程式不會將這個批註的值視為區分大小寫。

## <a name="saseffectcompany"></a>SasEffectCompany

這會宣告建立效果的公司。 其宣告如下：


```
string SasEffectCompany = "value";
```



其中的值是可識別擁有效果之公司名稱的字串。 預設為空字串。

## <a name="saseffectdescription"></a>SasEffectDescription

這會描述效果。 其宣告如下：


```
string SasEffectDescription = "value";
```



其中的值是描述效果的字串。 預設為空字串。

## <a name="saseffecthelp"></a>SasEffectHelp

這是一個說明字串，可在每次要求相關效果的說明時向使用者顯示。 其宣告如下：


```
string SasEffectHelp = "value";
```



其中的值是當使用者要求協助時，可以顯示的字串。 預設為空字串。

## <a name="saseffectrevision"></a>SasEffectRevision

此批註可讓工具和使用者記錄相關效果檔案的修訂編號。 例如，使用者可以在此注釋的值中插入適當的關鍵字，以在其最愛的修訂控制軟體中叫用關鍵字替代。 其宣告如下：


```
string SasEffectRevision = "value";
```



其中值是可識別效果修訂的字串。 預設為空字串。

## <a name="examples"></a>範例

以下是只使用單一必要注釋的範例：


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



以下是使用必要注釋和數個選用注釋的範例：


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX 標準注釋和語義參考](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 




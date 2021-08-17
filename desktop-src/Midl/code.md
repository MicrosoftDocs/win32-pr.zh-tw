---
title: code 屬性
description: '\ Code \ ACF 屬性會產生遠端函式的用戶端 stub 程式碼。'
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- code 屬性 MIDL
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d94f4f764fb25e5e2a5a43d1cdbe76f5288901846c2291daa4497947a486f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991812"
---
# <a name="code-attribute"></a>code 屬性

**\[ Code \]** ACF 屬性會為遠端函式產生用戶端 stub 程式碼。

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*ACF-介面-屬性* 
</dt> <dd>

指定套用至整個介面的一或多個屬性清單。 有效的屬性包括 [**\[ auto \_ 句 \] 柄**](auto-handle.md)或 [**\[ 隱含 \_ \] 控制碼**](implicit-handle.md)，以及程式 **\[ 代碼 \]**、 [**\[ 了 nocode \]**](nocode.md)或 [**\[ optimize \]**](optimize.md)。 當有兩個或多個介面屬性存在時，它們必須以逗號分隔。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> <dt>

*檔案名-清單* 
</dt> <dd>

指定一或多個 C 標頭檔名稱的清單（以逗號分隔）。 您必須提供完整的檔案名，包括副檔名。

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

指定套用至指定類型的一或多個屬性清單（以逗號分隔）。 有效的型別屬性包括將 [**\[ \] 配置**](allocate.md)和 [**\[ 表示 \_ 為 \]**](represent-as.md)。

</dd> <dt>

*typename* 
</dt> <dd>

指定 IDL 檔案中定義的類型。 ACF 中的 Type 屬性只能套用至 IDL 檔案中先前定義的類型。

</dd> <dt>

*ACF 函式-屬性* 
</dt> <dd>

指定套用至整個函式的零或多個屬性，例如 [**\[ 通訊 \_ 狀態 \]**](comm-status.md)。 函數屬性以方括弧括住。 以逗號分隔多個函式屬性。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定 IDL 檔案中所定義的函式名稱。

</dd> <dt>

*ACF-參數-屬性* 
</dt> <dd>

指定適用于參數的 ACF 屬性。 請注意，您可以將零個、一個或多個屬性套用至參數。 以逗號分隔多個參數屬性。 ACF 參數屬性以方括弧括住。

</dd> <dt>

*參數-名稱* 
</dt> <dd>

指定 IDL 檔案中定義之函式的參數。 函數的每個參數都必須以相同的順序指定，並且與 IDL 檔案中定義的名稱相同。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ Code \]** 屬性可以出現在 ACF 標頭中，或套用至個別的函式。

當程式 **\[ 代碼 \]** 屬性出現在 ACF 標頭時，會針對沒有 [**\[ 了 nocode \]**](nocode.md)函數屬性的所有遠端函式產生用戶端 stub 程式碼。 您可以藉由將 **\[ 了 nocode \]** 屬性指定為函數屬性，來覆寫個別函式標頭中的程式 **\[ 代碼 \]** 屬性。

當程式 **\[ 代碼 \]** 屬性出現在遠端函式的屬性清單時，就會為函式產生用戶端 stub 程式碼。 當下列情況時，不會產生用戶端 stub 程式碼：

-   ACF 標頭包含 [**\[ 了 nocode \]**](nocode.md)屬性。
-   [**\[ 了 nocode \]**](nocode.md)屬性會套用至函數。
-   [**\[ Local \]**](local.md)屬性會套用至介面檔中的函式。

程式 **\[ 代碼 \]** 或 [**\[ 了 nocode \]**](nocode.md)可以出現在 [介面] 或 [函式] 屬性清單中，但您選擇的只會在清單中顯示一次。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**分配**](allocate.md)
</dt> <dt>

[**自動 \_ 處理**](auto-handle.md)
</dt> <dt>

[**通訊 \_ 狀態**](comm-status.md)
</dt> <dt>

[**隱含 \_ 控制碼**](implicit-handle.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[**了 nocode**](nocode.md)
</dt> <dt>

[**優化**](optimize.md)
</dt> <dt>

[**表示 \_ 為**](represent-as.md)
</dt> </dl>

 

 




